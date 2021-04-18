---
description: Requisitos para las aplicaciones de Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisitos para las aplicaciones de Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717389"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a><span data-ttu-id="5829e-103">Requisitos para las aplicaciones de Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="5829e-103">Requirements for Windows Media DRM-Enabled Applications</span></span>

<span data-ttu-id="5829e-104">Para crear una aplicación habilitada para Windows Media Digital Rights Management (DRM), debe tener los encabezados y las bibliotecas que se describen en la sección [requisitos generales para el desarrollo de aplicaciones](general-requirements-for-application-development.md) de este documento.</span><span class="sxs-lookup"><span data-stu-id="5829e-104">To create a Windows Media Digital Rights Management (DRM)-enabled application, you must have the headers and libraries described in the [General Requirements for Application Development](general-requirements-for-application-development.md) section of this document.</span></span> <span data-ttu-id="5829e-105">Además, la aplicación deberá proporcionar propiedades adicionales en la información del cliente al abrir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5829e-105">In addition, the application will need to supply additional properties in the client information when opening the device.</span></span>

<span data-ttu-id="5829e-106">En la tabla siguiente se describen las dos propiedades adicionales necesarias para habilitar las transferencias de contenido protegidas con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="5829e-106">The two additional properties that are required to enable Windows Media DRM-protected content transfers are described in the following table.</span></span>



| <span data-ttu-id="5829e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5829e-107">Property</span></span>                                      | <span data-ttu-id="5829e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5829e-108">Description</span></span>                              |
|-----------------------------------------------|------------------------------------------|
| <span data-ttu-id="5829e-109">\_clave privada de la \_ \_ aplicación WMDRM \_ \_ del cliente de WPD</span><span class="sxs-lookup"><span data-stu-id="5829e-109">WPD\_CLIENT\_WMDRM\_APPLICATION\_PRIVATE\_KEY</span></span> | <span data-ttu-id="5829e-110">Especifica la clave privada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5829e-110">Specifies the application's private key.</span></span> |
| <span data-ttu-id="5829e-111">\_certificado de \_ \_ aplicación WMDRM del cliente \_ de WPD</span><span class="sxs-lookup"><span data-stu-id="5829e-111">WPD\_CLIENT\_WMDRM\_APPLICATION\_CERTIFICATE</span></span>  | <span data-ttu-id="5829e-112">Especifica el certificado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5829e-112">Specifies the application's certificate.</span></span> |



 

<span data-ttu-id="5829e-113">Estas propiedades se deben proporcionar en la información del cliente de la aplicación cuando el dispositivo se abre con el método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) .</span><span class="sxs-lookup"><span data-stu-id="5829e-113">These properties must be supplied in the application's client information when the device is opened with the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.</span></span> <span data-ttu-id="5829e-114">Cuando se proporcionan estas propiedades, la API de WPD permite las transferencias de contenido protegidas.</span><span class="sxs-lookup"><span data-stu-id="5829e-114">When these properties are supplied, the WPD API allows protected content transfers.</span></span> <span data-ttu-id="5829e-115">Si la aplicación ha proporcionado un certificado y una clave privada, la API creará un canal seguro para transferir el contenido de WMDRM protegido al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5829e-115">If the application has provided a certificate and private key, the API will create a secure channel to transfer protected WMDRM content to the device.</span></span>

<span data-ttu-id="5829e-116">Para obtener información acerca de la creación y distribución de aplicaciones basadas en Windows que admiten DRM de Windows Media, vea el siguiente tema sobre [licencias basadas en Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5829e-116">For information about creating and distributing Windows-based applications that support Windows Media DRM, see the following [Licensing Windows-based Applications](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) topic.</span></span>

## <a name="transferring-content"></a><span data-ttu-id="5829e-117">Transferir contenido</span><span class="sxs-lookup"><span data-stu-id="5829e-117">Transferring Content</span></span>

<span data-ttu-id="5829e-118">Para transferir contenido protegido de WMDRM, use [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="5829e-118">To transfer WMDRM protected content, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="5829e-119">Este método se puede usar para el contenido protegido y sin cifrar sin opciones adicionales.</span><span class="sxs-lookup"><span data-stu-id="5829e-119">This method can be used for both protected and clear content without additional options.</span></span> <span data-ttu-id="5829e-120">La API de WPD seleccionará automáticamente el canal protegido o desactivado, en función de si el contenido está protegido o desactivado.</span><span class="sxs-lookup"><span data-stu-id="5829e-120">The WPD API will automatically select the protected or clear channel depending on whether the content is protected or clear.</span></span> <span data-ttu-id="5829e-121">Interactúa con el proveedor de contenido seguro de WMDRM para procesar las licencias de WMDRM.</span><span class="sxs-lookup"><span data-stu-id="5829e-121">It interfaces with the WMDRM Secure Content Provider to process the WMDRM licenses.</span></span>

## <a name="transferring-known-clear-content"></a><span data-ttu-id="5829e-122">Transferencia de contenido sin cifrar conocido</span><span class="sxs-lookup"><span data-stu-id="5829e-122">Transferring Known Clear Content</span></span>

<span data-ttu-id="5829e-123">Si ha habilitado la aplicación para controlar el contenido protegido, pero sabe que un archivo específico no está protegido, puede indicar a WPD que omita el procesamiento de DRM estableciendo la **opción de API de WPD usar la opción \_ \_ \_ \_ Borrar \_ \_ flujo de datos** en true en la **IPortableDeviceValues** de entrada al llamar a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para el contenido no cifrado.</span><span class="sxs-lookup"><span data-stu-id="5829e-123">If you've enabled your application to handle protected content, but you know that a specific file is not protected, you can tell WPD to skip the DRM processing by setting **WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM** option to TRUE in the input **IPortableDeviceValues** when calling [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) for clear content.</span></span>

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a><span data-ttu-id="5829e-124">Obtener acceso a las operaciones de medición mediante IWMDRMDeviceApp</span><span class="sxs-lookup"><span data-stu-id="5829e-124">Accessing Metering Operations using IWMDRMDeviceApp</span></span>

<span data-ttu-id="5829e-125">WPD proporciona un mecanismo para tener acceso a las API de **IWMDRMDeviceApp** para las actualizaciones de licencia y la recuperación de datos de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="5829e-125">WPD provides a mechanism to access the **IWMDRMDeviceApp** APIs for license updates and metering data retrieval.</span></span> <span data-ttu-id="5829e-126">Para tener acceso a esta API a través de WPD, llame a **QueryInterface** en **IID \_ IWMDRMDeviceApp** desde la **IStream** devuelta desde [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="5829e-126">To access this API through WPD, call **QueryInterface** on **IID\_IWMDRMDeviceApp** from the **IStream** returned from [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span> <span data-ttu-id="5829e-127">Esta instancia de **IWMDRMDeviceApp** está vinculada a la conexión de **IPortableDevice** con el dispositivo compatible con WMDRM y no al contenido específico donde se obtuvo la **IStream** .</span><span class="sxs-lookup"><span data-stu-id="5829e-127">This **IWMDRMDeviceApp** instance tied to the **IPortableDevice** connection to your WMDRM-compatible device, and not the specific content where the **IStream** was obtained.</span></span> <span data-ttu-id="5829e-128">WPD encapsula internamente las API de medición y hace que sea accesible para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5829e-128">WPD internally wraps the metering APIs and makes it accessible to your application.</span></span> <span data-ttu-id="5829e-129">La aplicación debe usar la \_ \_ \_ constante PTR del dispositivo de WMDRMDEVICEAPP use WPD \_ para el parámetro *IWMDMDevice* \* .</span><span class="sxs-lookup"><span data-stu-id="5829e-129">Your application should use the WMDRMDEVICEAPP\_USE\_WPD\_DEVICE\_PTR constant for the *IWMDMDevice*\* parameter.</span></span>

<span data-ttu-id="5829e-130">En el fragmento de código siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="5829e-130">The following code snippet demonstrates this.</span></span>


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



<span data-ttu-id="5829e-131">También se aplica el mismo requisito previo a la clave privada y el certificado de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5829e-131">The same pre-requisite with the application private key and certificate applies here as well.</span></span> <span data-ttu-id="5829e-132">Si la clave o el certificado no son válidos o si el sistema WMDRM no se puede inicializar, se producirá un error en la llamada a **QueryInferface** .</span><span class="sxs-lookup"><span data-stu-id="5829e-132">If the key/certificate is invalid or if the WMDRM system fails to initialize, the **QueryInferface** call will fail.</span></span>

<span data-ttu-id="5829e-133">El método anterior para adquirir la interfaz **IWMDRMDeviceApp** del puntero **IStream** es simplemente una comodidad si la aplicación ya está realizando una transferencia de contenido protegida antes, antes de continuar con las operaciones de medición y sincronización de licencias.</span><span class="sxs-lookup"><span data-stu-id="5829e-133">The above method to acquire the **IWMDRMDeviceApp** interface from the **IStream** pointer is just a convenience if your application is already doing a prior protected content transfer, before proceeding on to do metering and license synchronization operations.</span></span>

<span data-ttu-id="5829e-134">Nuestra recomendación para la mayoría de las aplicaciones que necesitan acceder a **IWMDRMDeviceApp** consiste en inicializar **IWMDRMDeviceApp** directamente, ya que esto no requiere que la aplicación transfiera contenido protegido ni mantenga las interfaces de transferencia para realizar la sincronización de la licencia y la medición de los dispositivos. Este método necesitará el uso de las API de Windows Media Administrador de dispositivos (WMDM).</span><span class="sxs-lookup"><span data-stu-id="5829e-134">Our recommendation for most applications that need to access **IWMDRMDeviceApp** is to initialize **IWMDRMDeviceApp** directly as this does not require your application to transfer protected content or hold on to the transfer interfaces in order to do device metering and license sync. This method will require usage of Windows Media Device Manager (WMDM) APIs.</span></span> <span data-ttu-id="5829e-135">Para más información y ejemplos de código, consulte las notas del producto acceso a las [API de WMDRM desde una aplicación de WPD](../windows-portable-devices.md) en el sitio de whdc.</span><span class="sxs-lookup"><span data-stu-id="5829e-135">For details and sample code, refer to the [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) whitepaper on the WHDC site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5829e-136">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5829e-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5829e-137">**Dispositivos portátiles de Windows**</span><span class="sxs-lookup"><span data-stu-id="5829e-137">**Windows Portable Devices**</span></span>](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
