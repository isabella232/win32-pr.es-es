---
title: Propiedad TTSModeID
description: Propiedad TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269238"
---
# <a name="ttsmodeid-property"></a>Propiedad TTSModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el modo del motor TTS utilizado para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). TTSModeID* *  \[  =  *ModeID*\]



| Parte     | Descripción                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expresión de cadena que corresponde al identificador de modo de un motor de voz. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad determina el identificador del modo de motor de TTS (texto a voz) de la salida hablada de un carácter. El identificador de modo de un motor TTS es una cadena con formato definida por el proveedor de voz que identifica de forma única el modo del motor. Para obtener más información, consulte [acceso a un motor de voz en el código](accessing-a-speech-engine-in-your-code.md).

Al establecer esta propiedad, se invalida el intento del servidor de cargar un motor basado en la configuración de TTS compilada del carácter y la configuración de [**LanguageID**](languageid-property.md) actual del carácter. Sin embargo, si especifica un identificador de modo para un motor que no está instalado o si el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft (**AudioOutput. Enabled = False**), el servidor genera un error.

Si no se establece (o no correctamente) un identificador de modo TTS para el carácter, el servidor comprueba si la configuración de modo TTS compilado del carácter coincide con la configuración de [**LanguageID**](languageid-property.md) del carácter y si el motor TTS asociado está instalado. Si es así, el modo TTS utilizado por el carácter para la salida hablada y esta propiedad devuelve ese identificador de modo. Si no es así, el servidor solicita un motor de voz SAPI compatible que coincida con el **LanguageID** del carácter, así como el sexo y el conjunto de edad para el identificador del modo compilado del carácter. Si no ha establecido el **ididioma** del carácter, su **LanguageID** es el idioma del usuario actual. Si no se puede encontrar ningún motor coincidente, la consulta de esta propiedad devuelve una cadena vacía para el identificador de modo del motor. Del mismo modo, si consulta esta propiedad cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft (**AudioOutput. Enabled = False**), el valor será una cadena vacía.

Si se consulta o se establece esta propiedad, se cargará el motor asociado (si aún no está cargado). Sin embargo, si el motor especificado en la configuración de TTS compilada del carácter está instalado y coincide con la configuración de identificador de idioma del carácter, el motor se cargará cuando se cargue el carácter.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

> [!Note]  
> Esta propiedad también devuelve la cadena vacía si no tiene instalado ningún soporte de sonido compatible en el sistema.

 

> [!Note]  
> Se puede producir un error en la configuración de **TTSModeID** si no está instalado Speech.dll y el motor especificado no coincide con la configuración de modo TTS compilado del carácter.

 

> [!Note]  
> Normalmente, la consulta de esta propiedad no devuelve un error. Sin embargo, si el motor de voz tarda mucho tiempo en cargarse, puede recibir un error que indica que la consulta ha superado el tiempo de espera.

 

## <a name="see-also"></a>Consulte también

[**LanguageID (propiedad)**](languageid-property.md)


 

 




