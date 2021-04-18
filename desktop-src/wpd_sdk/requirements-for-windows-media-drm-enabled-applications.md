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
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisitos para las aplicaciones de Windows Media DRM-Enabled

Para crear una aplicación habilitada para Windows Media Digital Rights Management (DRM), debe tener los encabezados y las bibliotecas que se describen en la sección [requisitos generales para el desarrollo de aplicaciones](general-requirements-for-application-development.md) de este documento. Además, la aplicación deberá proporcionar propiedades adicionales en la información del cliente al abrir el dispositivo.

En la tabla siguiente se describen las dos propiedades adicionales necesarias para habilitar las transferencias de contenido protegidas con DRM de Windows Media.



| Propiedad                                      | Descripción                              |
|-----------------------------------------------|------------------------------------------|
| \_clave privada de la \_ \_ aplicación WMDRM \_ \_ del cliente de WPD | Especifica la clave privada de la aplicación. |
| \_certificado de \_ \_ aplicación WMDRM del cliente \_ de WPD  | Especifica el certificado de la aplicación. |



 

Estas propiedades se deben proporcionar en la información del cliente de la aplicación cuando el dispositivo se abre con el método [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) . Cuando se proporcionan estas propiedades, la API de WPD permite las transferencias de contenido protegidas. Si la aplicación ha proporcionado un certificado y una clave privada, la API creará un canal seguro para transferir el contenido de WMDRM protegido al dispositivo.

Para obtener información acerca de la creación y distribución de aplicaciones basadas en Windows que admiten DRM de Windows Media, vea el siguiente tema sobre [licencias basadas en Windows](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .

## <a name="transferring-content"></a>Transferir contenido

Para transferir contenido protegido de WMDRM, use [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Este método se puede usar para el contenido protegido y sin cifrar sin opciones adicionales. La API de WPD seleccionará automáticamente el canal protegido o desactivado, en función de si el contenido está protegido o desactivado. Interactúa con el proveedor de contenido seguro de WMDRM para procesar las licencias de WMDRM.

## <a name="transferring-known-clear-content"></a>Transferencia de contenido sin cifrar conocido

Si ha habilitado la aplicación para controlar el contenido protegido, pero sabe que un archivo específico no está protegido, puede indicar a WPD que omita el procesamiento de DRM estableciendo la **opción de API de WPD usar la opción \_ \_ \_ \_ Borrar \_ \_ flujo de datos** en true en la **IPortableDeviceValues** de entrada al llamar a [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para el contenido no cifrado.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Obtener acceso a las operaciones de medición mediante IWMDRMDeviceApp

WPD proporciona un mecanismo para tener acceso a las API de **IWMDRMDeviceApp** para las actualizaciones de licencia y la recuperación de datos de disponibilidad. Para tener acceso a esta API a través de WPD, llame a **QueryInterface** en **IID \_ IWMDRMDeviceApp** desde la **IStream** devuelta desde [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Esta instancia de **IWMDRMDeviceApp** está vinculada a la conexión de **IPortableDevice** con el dispositivo compatible con WMDRM y no al contenido específico donde se obtuvo la **IStream** . WPD encapsula internamente las API de medición y hace que sea accesible para la aplicación. La aplicación debe usar la \_ \_ \_ constante PTR del dispositivo de WMDRMDEVICEAPP use WPD \_ para el parámetro *IWMDMDevice* \* .

En el fragmento de código siguiente se muestra esto.


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



También se aplica el mismo requisito previo a la clave privada y el certificado de la aplicación. Si la clave o el certificado no son válidos o si el sistema WMDRM no se puede inicializar, se producirá un error en la llamada a **QueryInferface** .

El método anterior para adquirir la interfaz **IWMDRMDeviceApp** del puntero **IStream** es simplemente una comodidad si la aplicación ya está realizando una transferencia de contenido protegida antes, antes de continuar con las operaciones de medición y sincronización de licencias.

Nuestra recomendación para la mayoría de las aplicaciones que necesitan acceder a **IWMDRMDeviceApp** consiste en inicializar **IWMDRMDeviceApp** directamente, ya que esto no requiere que la aplicación transfiera contenido protegido ni mantenga las interfaces de transferencia para realizar la sincronización de la licencia y la medición de los dispositivos. Este método necesitará el uso de las API de Windows Media Administrador de dispositivos (WMDM). Para más información y ejemplos de código, consulte las notas del producto acceso a las [API de WMDRM desde una aplicación de WPD](../windows-portable-devices.md) en el sitio de whdc.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Dispositivos portátiles de Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
