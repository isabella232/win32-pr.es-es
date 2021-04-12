---
title: Control de eventos de adquisición de licencias
description: Control de eventos de adquisición de licencias
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- SDK de Windows Media Format, control de eventos de adquisición de licencias
- SDK de Windows Media Format, eventos de adquisición de licencias
- Advanced Systems Format (ASF), control de eventos de adquisición de licencias
- ASF (Advanced Systems Format), control de eventos de adquisición de licencias
- Advanced Systems Format (ASF), eventos de adquisición de licencias
- ASF (formato de sistemas avanzados), eventos de adquisición de licencias
- Administración de derechos digitales (DRM), control de eventos de adquisición de licencias
- DRM (administración de derechos digitales), control de eventos de adquisición de licencias
- Administración de derechos digitales (DRM), eventos de adquisición de licencias
- DRM (administración de derechos digitales), eventos de adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420277"
---
# <a name="handling-license-acquisition-events"></a>Control de eventos de adquisición de licencias

Una aplicación de lector habilitada para DRM, en su método de devolución de llamada [**IWMStatusCallback::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) en el estado, controla los cuatro eventos siguientes relacionados con el proceso de adquisición de licencias:

-   **\_Estado de \_ firma de LICENSEURL de WMT \_**
-   **\_sin \_ derechos de WMT**
-   **\_no hay \_ derechos de WMT \_ ex**
-   **\_licencia de adquisición de WMT \_**

**\_Estado de \_ firma de LICENSEURL de WMT \_**

Cuando el componente DRM detecta contenido protegido por la versión 7 de DRM, primero busca una licencia válida en el sistema local. Si no existe ninguno, evalúa la dirección URL de adquisición de licencias en el encabezado DRM del archivo y envía un evento de **\_ \_ \_ Estado de firma WMT LICENSEURL** con *pValue* establecido en uno de los valores de [**\_ \_ confianza de DRMLA WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , que indica si la dirección URL es de confianza, no es de confianza o se ha alterado. Si la dirección URL no es de confianza, la aplicación debe advertir al usuario. Si la dirección URL se ha alterado, el archivo debe considerarse dañado y la aplicación no debe navegar hasta la dirección URL sin emitir una advertencia segura al usuario.

**\_sin \_ derechos de WMT**

El evento **WMT \_ no \_ Rights** solo se envía para el contenido de la versión 1 de DRM, lo que significa que la licencia debe adquirirse de forma no silenciosa. En otras palabras, el usuario debe ir a una página web para adquirir una licencia. La dirección URL de la página se recupera como una cadena terminada en NULL de caracteres anchos del parámetro *pValue* en el método de **Estado** .

Si es necesario, una aplicación puede facilitar al usuario navegar a la página web, ya sea abriendo Internet Explorer en un proceso independiente o bien hospedando el control del explorador Web. Sin embargo, esto no es necesario. Como mínimo, una aplicación podría mostrar simplemente la dirección URL del usuario en un cuadro de mensaje y pedirles que la peguen en la barra de direcciones de Internet Explorer. En el ejemplo AudioPlayer se muestra el control adecuado del evento **WMT \_ no \_ Rights** , incluido cómo dar formato a la cadena de dirección URL y cómo usar el método **CreateProcess** para abrir Internet Explorer y navegar a la dirección URL especificada.

Dado que la aplicación no tiene ninguna manera de saber cuándo se ha adquirido una licencia de DRM versión 1, es el usuario quien intenta volver a abrir el archivo después de adquirir la licencia.

Este mismo proceso de adquisición de licencias no silenciosa también puede usarse para las licencias de la versión 7, pero en este caso la aplicación puede llamar primero a [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Este método hará que el almacén de licencias local se compruebe repetidamente hasta que se encuentre la licencia del nuevo archivo. En ese momento, la aplicación recibirá un evento de **\_ \_ licencia de adquisición de WMT** . Para todas las licencias de la versión 7, se recomienda que las aplicaciones ofrezcan a los usuarios la opción de obtener licencias de forma silenciosa o no silenciosa.

**\_no hay \_ derechos de WMT \_ ex**

El evento **WMT \_ no \_ Rights \_ ex** indica que el contenido está protegido por la versión 7 de DRM y, por lo tanto, el proceso de adquisición de licencias puede continuar de forma silenciosa o no silenciosa. En general, la adquisición silenciosa de licencias es más cómoda para los usuarios finales, aunque algunas personas prefieren adquirir todas las licencias de forma no silenciosa. Cuando la adquisición de licencias requiere que el usuario envíe información personal o de pago, el proceso siempre debe realizarse de forma no silenciosa. La adquisición de licencias no silenciosas se ha descrito anteriormente en el encabezado **WMT \_ no \_ Rights** . La adquisición silenciosa continúa como sigue:

1.  Convierta el parámetro *pValue* a una estructura de [**datos de licencia de WM \_ Get \_ \_**](wm-get-license-data.md) y almacene la estructura en caso de que sea necesaria más adelante para la adquisición de licencias no silenciosa.
2.  Llame a **QueryInterface** en el objeto Reader para obtener la interfaz [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .
3.  Llame a [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) y especifique 0x1 en el parámetro *dwFlags* para indicar la adquisición del lenguaje silencioso. Se trata de una llamada asincrónica que se devuelve inmediatamente.
4.  Espere al evento **de \_ \_ licencia de adquisición de WMT** .

**\_licencia de adquisición de WMT \_**

El evento de **\_ \_ licencia de adquisición de WMT** se envía una vez completado el proceso de adquisición de licencias para una licencia de DRM versión 7. [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) hace que este evento se envíe para la adquisición silenciosa, y [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) hace que se envíe para la adquisición no silenciosa. En el controlador de eventos, convierta *pValue* en un puntero a una estructura de datos de licencia de Get de WM y examine el miembro de **recursos humanos** para determinar si la licencia se adquirió correctamente. [**\_ \_ \_**](wm-get-license-data.md) Si **HR** es igual \_ a E DRM de NS E \_ \_ no tiene \_ derechos, indica que la licencia debe adquirirse de forma no silenciosa. Las aplicaciones deben permitir que los usuarios cancelen el proceso de adquisición de licencias en cualquier momento. Esto se hace mediante una llamada a [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). Al llamar a este método, se enviará un evento de **\_ \_ licencia de adquisición WMT** con un valor **HRESULT** de la \_ adquisición de DRM S de NS \_ \_ \_ cancelada.

Si **HR** es igual \_ a NS S \_ DRM \_ License \_ adquirida, se ha adquirido la licencia y la aplicación puede intentar reproducir el archivo o copiarlo en un dispositivo o realizar la acción para la que tenía derechos solicitados.

En Windows XP, se presentó un nuevo código de error: NS \_ E \_ DRM \_ License \_ NOTACQUIRED. Este código de error se genera cuando los componentes en tiempo de ejecución de Windows Media Format en Windows XP no pueden adquirir una licencia durante la adquisición de licencias silenciosa o no silenciosa. En otras plataformas, el \_ \_ error del almacén de licencias de DRM E DRM \_ \_ \_ se devuelve normalmente cuando se produce un error en la adquisición de licencias. El nuevo código de error se ha diseñado para distinguir los errores de adquisición de licencias de otras condiciones de error en las que \_ \_ se genera un error de almacén de licencias de DRM E DRM \_ \_ \_ .

La manera recomendada de controlar estos errores cuando se devuelven después de un intento de adquisición de licencias silenciosa se muestra en el siguiente fragmento de código:


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> DRM no es compatible con la versión basada en x64 de este SDK.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos protegidos**](reading-protected-files.md)
</dt> </dl>

 

 




