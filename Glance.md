![GLANCE LOGO](https://gitlab.in2p3.fr/uploads/-/system/project/avatar/6720/OpenStack_Project_Glance_mascot.png)

# GLANCE OPENSTACK (IMAGE MANAGER)

> This markdown fouces on definitions, configurations and use cases of **GLACNCE RESOURCE** the image manager of OPEN STACK similar to AWS Amazon Machine Image.

## TABLE OF CONTENT

1. **Introduction to GLANCE**
2. **Uploading Images via Web Interface (HORIZON)**
3. **Uploading Images via OPENSTACK Command Line Utility**
4. **Common Issues & Resolves**
5. **OFFICIAL DOCUMENTATION & REFERENCES**

### Introduction to GLANCE

_Definition_ : **GLANCE** is the image service component that manages the Virtual Machine Images for the user allowing them to manage and register the images.

#### Key Features of GLANCE

- **IMAGE REPOSITORY** : Stores VM images which can be used as templates to create new instances.
- **FORMATS SUPPORT** : Supports multiple image formats. Example ova, iso, qcow2, raw etc.
- **Integration with Other Services** : Integrates with other OpenStack services like Nova, Cinder, Swift enabling seamless deployment.

### Uploading Images via Web Interface (HORIZON)

> This section focuses on uploading images using the **HORIZON SERVICE** web interface of OPEN STACK for managing and monitoring the resources.

##### STEPS

1. Login to the **Horizon Interface** with `admin : admin` as `username : password`

![Horizon Login Panel](/images/general/login.png)

2. Navigate to the Images section under the Compute Services.

![Glance Image Manager](/images/glance-gui/glance.png)

3. Now click on the Create image to to upload your image.

![Glance Image Manager](/images/glance-gui/image-upload.png)

4. Fill out the necessary details about your image

![Configuring Your Image](/images/glance-gui/configurations.png)

5. Click on next and click on create image, that should start uploading you image.

![Uploading Image](/images/glance-gui/create-image.png)

6. Once the image is created it will be visible in the web console.

![Image Uploaded](/images/glance-gui/created-image.png)

> **IMPORTANT : To download and convert your image file into supported format of GLANCE GUI in this case .iso use the commands below.**

`wget https://cloud-images.ubuntu.com/jammy/20241002/jammy-server-cloudimg-s390x.img`

> To download the .img file from ubuntu cloud web service

`dd if=jammy-server-cloudimg-s390x.img of=ubuntu.iso`

`dd if=<your-image-file.img of=<your-output-file.iso>`

> To convert your .img into .iso
