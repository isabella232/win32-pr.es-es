---
title: Control de eventos de adquisición de licencias
description: Control de eventos de adquisición de licencias
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows SDK de formato multimedia, control de eventos de adquisición de licencias
- Windows SDK de formato multimedia, eventos de adquisición de licencias
- Formato de sistemas avanzados (ASF), control de eventos de adquisición de licencias
- ASF (formato de sistemas avanzados), control de eventos de adquisición de licencias
- Formato de sistemas avanzados (ASF), eventos de adquisición de licencias
- ASF (formato de sistemas avanzados), eventos de adquisición de licencias
- administración de derechos digitales (DRM), control de eventos de adquisición de licencias
- DRM (administración de derechos digitales), control de eventos de adquisición de licencias
- administración de derechos digitales (DRM), eventos de adquisición de licencias
- DRM (administración de derechos digitales), eventos de adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360586"
---
# <a name="handling-license-acquisition-events"></a>Control de eventos de adquisición de licencias

Una aplicación de lector habilitada para DRM, en su método de devolución de llamada [**IWMStatusCallback::OnStatus,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) controla los cuatro eventos siguientes relacionados con el proceso de adquisición de licencias:

-   **ESTADO DE FIRMA \_ DE LICENSEURL \_ DE WMT \_**
-   **WMT \_ NO \_ RIGHTS**
-   **WMT \_ NO \_ RIGHTS \_ EX**
-   **ADQUISICIÓN DE LICENCIA DE WMT \_ \_**

**ESTADO DE FIRMA \_ DE LICENSEURL \_ DE WMT \_**

Cuando el componente DRM detecta contenido protegido por DRM versión 7, primero busca una licencia válida en el sistema local. Si no existe ninguno, evalúa la dirección URL de adquisición de licencias en el encabezado DRM del archivo y envía un evento **\_ WMT LICENSEURL \_ SIGNATURE \_ STATE** con *pValue* establecido en uno de los valores DE TRUST de [**\_ DRMLA \_ de WMT,**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) lo que indica si la dirección URL es de confianza, no es de confianza o se ha alterado. Si la dirección URL no es de confianza, la aplicación debe advertir al usuario. Si se ha alterado la dirección URL, el archivo debe considerarse dañado y la aplicación no debe navegar a la dirección URL sin emitir una advertencia fuerte al usuario.

**WMT \_ NO \_ RIGHTS**

El **evento \_ WMT NO \_ RIGHTS** solo se envía para el contenido de la versión 1 de DRM, lo que significa que la licencia debe adquirirse de forma no silenciosa. En otras palabras, el usuario debe navegar a una página web para adquirir una licencia. La dirección URL de la página se recupera como una cadena terminada en null de caracteres anchos del *parámetro pValue* del **método OnStatus.**

Si procede, una aplicación puede facilitar al usuario la navegación a la página web, ya sea abriendo Internet Explorer en un proceso independiente o hospedando el control Explorador web. Sin embargo, esto no es necesario. Como mínimo, una aplicación podría mostrar simplemente la dirección URL al usuario en un cuadro de mensaje y pedir que la pegue en la barra de direcciones de Internet Explorer. El ejemplo Audioplayer muestra el control adecuado del evento **\_ WMT NO \_ RIGHTS,** incluido cómo dar formato a la cadena de dirección URL y cómo usar el **método CreateProcess** para abrir Internet Explorer y navegar a la dirección URL especificada.

Dado que la aplicación no tiene forma de saber cuándo se ha adquirido una licencia DRM versión 1, es el usuario el que debe intentar abrir el archivo de nuevo después de adquirir la licencia.

Este mismo proceso de adquisición de licencias no silenciosas también se puede usar para las licencias de la versión 7, pero en este caso la aplicación puede llamar primero a [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition). Este método hará que el almacén de licencias local se comprueba repetidamente hasta que se encuentra la licencia del nuevo archivo. En ese momento, la aplicación recibirá un **evento WMT \_ ACQUIRE \_ LICENSE.** Para todas las licencias de la versión 7, se recomienda que las aplicaciones den a los usuarios la opción de obtener licencias de forma silenciosa o no silenciosa.

**WMT \_ NO \_ RIGHTS \_ EX**

El **evento WMT \_ NO RIGHTS \_ \_ EX** indica que el contenido está protegido por DRM versión 7 y, por tanto, el proceso de adquisición de licencias puede continuar de forma silenciosa o no silenciosa. En general, la adquisición silenciosa de licencias es más conveniente para los usuarios finales, aunque algunas personas prefieren adquirir todas las licencias de forma no silenciosa. Cuando la adquisición de licencias requiere que el usuario envíe información personal o de pago, el proceso siempre debe realizarse de forma silenciosa. La adquisición de licencias no silenciosas se describe anteriormente en el **encabezado WMT \_ NO \_ RIGHTS.** La adquisición silenciosa continúa de la siguiente manera:

1.  Convierte el *parámetro pValue* en una estructura [**WM GET LICENSE \_ \_ \_ DATA**](wm-get-license-data.md) y almacena la estructura en caso de que sea necesaria más adelante para la adquisición de licencias no silenciosas.
2.  Llame **a QueryInterface** en el objeto reader para obtener [**la interfaz IWMDRMReader.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
3.  Llame [**a IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) y especifique 0x1 en el *parámetro dwFlags* para indicar la adquisición silenciosa del lenguaje. Se trata de una llamada asincrónica que se devuelve inmediatamente.
4.  Espere al evento **WMT \_ ACQUIRE \_ LICENSE.**

**ADQUISICIÓN DE LICENCIA DE WMT \_ \_**

El **evento WMT \_ ACQUIRE \_ LICENSE** se envía una vez completado el proceso de adquisición de licencias para una licencia DRM versión 7. [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) hace que este evento se envíe para la adquisición silenciosa y [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) hace que se envíe para la adquisición no silenciosa. En el controlador de eventos, convierte *pValue* en un puntero a una estructura [**WM GET LICENSE \_ \_ \_ DATA**](wm-get-license-data.md) y examina el miembro **hr** para determinar si la licencia se adquirió correctamente. Si **hr** es igual a NS E DRM NO RIGHTS, indica que la licencia debe adquirirse \_ de forma no \_ \_ \_ silenciosa. Las aplicaciones deben permitir que los usuarios cancelen el proceso de adquisición de licencias en cualquier momento. Para ello, llame a [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition). Al llamar a este método se enviará un **evento WMT \_ ACQUIRE \_ LICENSE** con un **valor HRESULT** de NS \_ S DRM ACQUIRE \_ \_ \_ CANCELLED.

Si **hr** es igual a NS S DRM LICENSE ACQUIRED, la licencia se ha adquirido y la aplicación puede intentar reproducir el archivo, copiarlo en un dispositivo o realizar cualquier acción para la que haya solicitado \_ \_ \_ \_ derechos.

En Windows XP, se introdujo un nuevo código de error: NS \_ E \_ DRM LICENSE \_ \_ NOTACQUIRED. Este código de error se genera siempre que los componentes en tiempo de ejecución de Windows Media Format en Windows XP no puedan adquirir una licencia durante la adquisición de licencias silenciosas o no silenciosas. En otras plataformas, el error del almacén de licencias de DRM de NS se \_ devuelve normalmente cuando se produce un error en la \_ \_ \_ \_ adquisición de licencias. El nuevo código de error está pensado para distinguir los errores de adquisición de licencias de otras condiciones de error en las que se genera el error del ALMACÉN DE LICENCIAS DRM de NS \_ \_ \_ \_ \_ E.

La manera recomendada de controlar estos errores cuando se devuelven después de un intento silencioso de adquisición de licencias se muestra en el siguiente fragmento de código:


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

 

 




