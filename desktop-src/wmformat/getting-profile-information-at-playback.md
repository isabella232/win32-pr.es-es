---
title: Obtención de información de perfil en la reproducción
description: Obtención de información de perfil en la reproducción
ms.assetid: 4ea6c063-fd53-4b5e-ac01-9e2790322ace
keywords:
- Windows Media Format SDK, perfiles
- Advanced Systems Format (ASF), perfiles
- ASF (formato de sistemas avanzados), perfiles
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- Advanced Systems Format (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- flujos, obtener información de perfil en la reproducción
- perfiles, obtener información en la reproducción
- exclusión mutua, obtención de información de perfil en la reproducción
- uso compartido de ancho de banda, obtención de información de perfil en la reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4a5c7083f7bf9e986e8a23ba2c78dfe4404942a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149092"
---
# <a name="getting-profile-information-at-playback"></a>Obtención de información de perfil en la reproducción

La información del perfil que se usa para crear un archivo se almacena en la sección de encabezado del archivo. Ambos objetos de lector pueden tener acceso a la información de perfil del encabezado de archivo. Hay varias razones por las que puede que desee tener acceso a los datos de perfil desde el lector. Normalmente, tendrá que recuperar información sobre las secuencias, los objetos de exclusión mutua y los objetos de uso compartido de ancho de banda.

Tanto el objeto lector asincrónico como el objeto lector sincrónico se pueden consultar para la interfaz [**IWMProfile**](iwmprofile.md) . Ningún cambio realizado en la información del perfil puede afectar al archivo en el lector. Para obtener más información sobre el acceso a la información de perfil, consulte [trabajar con perfiles](working-with-profiles.md).

## <a name="stream-information"></a>Información de secuencia

A veces es importante saber cómo se configura un flujo. Cuando se recuperan las propiedades de los medios de cualquiera de los objetos de lector, se obtienen las propiedades de las salidas. Las propiedades de salida describen cómo el lector va a entregar los datos sin comprimir de una secuencia, no cómo se configura el flujo en el archivo ASF.

Al recibir ejemplos de secuencias sin comprimir de cualquier objeto lector, debe usar la información del perfil para identificar el formato de los datos comprimidos. Esto es especialmente importante si va a escribir la secuencia comprimida en otro archivo ASF.

También debe tener acceso a la información de la secuencia al utilizar la recompresión inteligente para transcodificar una secuencia de audio a una velocidad de bits inferior.

Puede que desee determinar si una secuencia se escribió con codificación de velocidad de bits variable (VBR). No se puede tener acceso a ninguna información de VBR de la interfaz **IWMProfile** de cualquier objeto de lector. Esto se debe a que la información de VBR no se almacena en el archivo después de la codificación. Puede determinar si se ha creado una secuencia mediante la codificación VBR obteniendo un puntero a la interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) del objeto lector y llamando a [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname). Debe especificar el número de secuencia y pasar g \_ wszIsVBR como el nombre del atributo.

## <a name="mutual-exclusion-information"></a>Información de exclusión mutua

Si desea crear una aplicación de lectura que use la exclusión mutua, querrá tener acceso a la información sobre los objetos de exclusión mutua incluidos en el perfil. Para todos los tipos de exclusión mutua excepto la velocidad de bits, la aplicación de lectura es responsable de cualquier cambio de flujo necesario. Para cambiar de flujo, debe saber qué secuencias son.

## <a name="bandwidth-sharing-information"></a>Información de uso compartido de ancho de banda

Los objetos de uso compartido de ancho de banda que se incluyen en un perfil solo se incluyen con fines informativos. Ni el objeto de escritor ni ninguno de los objetos de lector toman ninguna acción como resultado de los datos de uso compartido de ancho de banda. Si desea utilizar el uso compartido de ancho de banda en la aplicación de lectura, debe tener acceso a la información de uso compartido de ancho de banda de los datos del perfil.

> [!Note]  
> No toda la información del perfil que se usa para crear un archivo está presente en el encabezado del archivo. Como norma general, los datos que se usan solo en el momento de la codificación no se conservan en el archivo. Esto incluye los valores de entrada que se establecieron mediante el método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , así como las propiedades establecidas con el método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMProfile**](iwmprofile.md)
</dt> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




