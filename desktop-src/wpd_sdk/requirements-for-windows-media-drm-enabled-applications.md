---
description: Requisitos para Windows aplicaciones de DRM-Enabled multimedia
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisitos para Windows aplicaciones de DRM-Enabled multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571181"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisitos para Windows aplicaciones de DRM-Enabled multimedia

Para crear una aplicación habilitada para Windows Media Digital Rights Management (DRM), debe tener los [](general-requirements-for-application-development.md) encabezados y bibliotecas descritos en la sección Requisitos generales para el desarrollo de aplicaciones de este documento. Además, la aplicación deberá proporcionar propiedades adicionales en la información del cliente al abrir el dispositivo.

En la tabla siguiente se describen las dos propiedades adicionales necesarias para habilitar Windows de contenido protegido por DRM multimedia.



| Propiedad                                      | Descripción                              |
|-----------------------------------------------|------------------------------------------|
| CLAVE PRIVADA \_ DE APLICACIÓN \_ WMDRM DE CLIENTE \_ \_ \_ WPD | Especifica la clave privada de la aplicación. |
| CERTIFICADO DE APLICACIÓN WMDRM DE CLIENTE \_ \_ WPD \_ \_  | Especifica el certificado de la aplicación. |



 

Estas propiedades deben proporcionarse en la información de cliente de la aplicación cuando el dispositivo se abre con el [**método IPortableDevice::Open.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) Cuando se proporcionan estas propiedades, la API de WPD permite las transferencias de contenido protegido. Si la aplicación ha proporcionado un certificado y una clave privada, la API creará un canal seguro para transferir contenido WMDRM protegido al dispositivo.

Para obtener información sobre cómo crear y distribuir Windows basadas en aplicaciones que [](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) admiten drm multimedia de Windows, vea el siguiente tema Aplicaciones basadas en Windows licencias.

## <a name="transferring-content"></a>Transferencia de contenido

Para transferir contenido protegido de WMDRM, use [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Este método se puede usar para contenido protegido y sin opciones adicionales. La API de WPD seleccionará automáticamente el canal protegido o no, en función de si el contenido está protegido o no. Se interfaces con el proveedor de contenido seguro de WMDRM para procesar las licencias wmdrm.

## <a name="transferring-known-clear-content"></a>Transferencia de contenido claro conocido

Si ha habilitado la aplicación para controlar el contenido protegido, pero sabe que un archivo específico no está protegido, puede decir a WPD que omita el procesamiento drm estableciendo la opción DE API DE **WPD \_ USE CLEAR \_ DATA \_ \_ \_ \_ STREAM** en TRUE en la entrada **IPortableDeviceValues** al llamar a [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) para obtener contenido sin formato.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Acceso a operaciones de medición mediante IWMDRMDeviceApp

WPD proporciona un mecanismo para acceder a las API **de IWMDRMDeviceApp** para las actualizaciones de licencias y la recuperación de datos de medición. Para acceder a esta API a través de WPD, llame a **QueryInterface** en **IID \_ IWMDRMDeviceApp** desde el **IStream** devuelto desde [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Esta **instancia de IWMDRMDeviceApp** está vinculada a la conexión **IPortableDevice** al dispositivo compatible con WMDRM y no al contenido específico donde se obtuvo **el IStream.** WPD encapsula internamente las API de medición y hace que sea accesible para la aplicación. La aplicación debe usar la constante WMDRMDEVICEAPP \_ USE \_ WPD DEVICE PTR para el parámetro \_ \_ *IWMDMDevice.* \*

El siguiente fragmento de código muestra esto.


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



Aquí también se aplica el mismo requisito previo con la clave privada de la aplicación y el certificado. Si la clave o el certificado no son válidos o si el sistema WMDRM no se inicializa, se producirá un error en la llamada **a QueryInferface.**

El método anterior para adquirir la interfaz **IWMDRMDeviceApp** desde el puntero **IStream** es simplemente una comodidad si la aplicación ya está realizando una transferencia de contenido protegido anterior, antes de continuar con las operaciones de medición y sincronización de licencias.

Nuestra recomendación para la mayoría de las aplicaciones que necesitan tener acceso a **IWMDRMDeviceApp** es inicializar **IWMDRMDeviceApp** directamente, ya que esto no requiere que la aplicación transfiera contenido protegido ni se mantenga en las interfaces de transferencia para realizar la medición de dispositivos y la sincronización de licencias. Este método requerirá el uso de Windows API de Administrador de dispositivos multimedia (WMDM). Para obtener más información y código de ejemplo, consulte las [whitepapers Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) (Acceso a las API WMDRM desde una aplicación WPD) en el sitio de WHDC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Windows Dispositivos portátiles**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
