---
title: Obtención de información de perfil en la reproducción
description: Obtención de información de perfil en la reproducción
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows SDK de formato multimedia, perfiles
- Formato de sistemas avanzados (ASF), perfiles
- ASF (formato de sistemas avanzados), perfiles
- Formato de sistemas avanzados (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- Formato de sistemas avanzados (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- streams,getting profile information at playback
- perfiles, obtener información en la reproducción
- exclusión mutua, obtener información de perfil durante la reproducción
- uso compartido de ancho de banda, obtención de información de perfil en la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0f9386301b426adb3c4c425ac9329309c7e45146e312cc41df0bd1c453d485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839925"
---
# <a name="getting-profile-information-at-playback"></a>Obtención de información de perfil en la reproducción

La información del perfil utilizado para crear un archivo se almacena en la sección de encabezado del archivo. Ambos objetos de lector pueden acceder a la información del perfil desde el encabezado de archivo. Hay varias razones por las que es posible que desee acceder a los datos del perfil desde el lector. Normalmente, deberá recuperar información sobre secuencias, objetos de exclusión mutua y objetos de uso compartido de ancho de banda.

Tanto el objeto de lector asincrónico como el objeto de lector sincrónico se pueden consultar para la [**interfaz IWMProfile.**](iwmprofile.md) Ningún cambio realizado en la información del perfil puede afectar al archivo del lector. Para obtener más información sobre el acceso a la información de perfil, vea [Trabajar con perfiles.](working-with-profiles.md)

## <a name="stream-information"></a>Transmisión de información

A veces es importante saber cómo se configura una secuencia. Cuando se recuperan propiedades de medios de cualquiera de los objetos de lector, se obtienen las propiedades de las salidas. Las propiedades de salida describen cómo el lector va a entregar los datos sin comprimir de una secuencia, no cómo se configura la secuencia en el archivo ASF.

Al recibir muestras de secuencias sin comprimir desde cualquier objeto de lector, debe usar la información de perfil para identificar el formato de los datos comprimidos. Esto es especialmente importante si va a escribir la secuencia comprimida en otro archivo ASF.

También debe acceder a la información de la secuencia cuando se usa la recompresión inteligente para transcodificar una secuencia de audio a una velocidad de bits inferior.

Es posible que desee determinar si una secuencia se escribió mediante la codificación de velocidad de bits variable (VBR). No se puede acceder a ninguna información de VBR desde la **interfaz IWMProfile** de cualquier objeto de lector. Esto se debe a que la información de VBR no se almacena en el archivo después de la codificación. Puede determinar si una secuencia se creó mediante la codificación VBR obteniendo un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) del objeto lector y llamando a [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). Debe especificar el número de secuencia y pasar g \_ wszIsVBR como nombre del atributo.

## <a name="mutual-exclusion-information"></a>Información de exclusión mutua

Si desea crear una aplicación de lectura que use la exclusión mutua, querrá acceder a la información sobre los objetos de exclusión mutua incluidos en el perfil. Para todos los tipos de exclusión mutua excepto la velocidad de bits, la aplicación de lectura es responsable de cualquier cambio de flujo necesario. Para cambiar de flujo, debe saber qué secuencias son.

## <a name="bandwidth-sharing-information"></a>Información de uso compartido de ancho de banda

Los objetos de uso compartido de ancho de banda que se incluyen en un perfil solo se incluyen con fines informativos. Ni el objeto de escritor ni ninguno de los objetos de lector realiza ninguna acción como resultado del uso compartido de ancho de banda de los datos. Si desea usar el uso compartido de ancho de banda en la aplicación de lectura, debe acceder a la información de uso compartido de ancho de banda desde los datos del perfil.

> [!Note]  
> No toda la información del perfil utilizado para crear un archivo está presente en el encabezado del archivo. Como regla general, los datos que se usan solo en el momento de la codificación no se conservan en el archivo. Esto incluye la configuración de entrada que se estableció mediante el método [**IWMWriterAdvanced2::SetInputSetting,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) así como las propiedades establecidas mediante el método [**IWMPropertyVault::SetProperty.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




