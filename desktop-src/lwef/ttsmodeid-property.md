---
title: Propiedad TTSModeID
description: Propiedad TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6852f203f5df716df6cfc5962f9cfa911d8fc1a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241220"
---
# <a name="ttsmodeid-property"></a>Propiedad TTSModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el modo de motor de TTS utilizado para el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Caracteres ("**_CharacterID_*_"). TTSModeID_ *  \[  =  *ModeID*\]



| Parte     | Descripción                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expresión de cadena que corresponde al identificador de modo de un motor de voz. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta propiedad determina el identificador de modo de motor TTS (texto a voz) para la salida hablada de un carácter. El identificador de modo de un motor de TTS es una cadena con formato definida por el proveedor de voz que identifica de forma única el modo del motor. Para obtener más información, vea [Acceso a un motor de voz en el código](accessing-a-speech-engine-in-your-code.md).

Al establecer esta propiedad se invalida el intento del servidor de cargar un motor en función de la configuración de TTS compilada del carácter y la configuración de [**LanguageID**](languageid-property.md) actual del carácter. Sin embargo, si especifica un identificador de modo para un motor que no está instalado o si el usuario ha deshabilitado la salida de voz en la hoja de propiedades de Microsoft Agent **(AudioOutput.Enabled = False),** el servidor genera un error.

Si no establece (o no ha establecido correctamente) un identificador de modo TTS para el carácter, el servidor comprueba si la configuración del modo TTS compilado del carácter coincide con la configuración de [**LanguageID**](languageid-property.md) del carácter y si el motor de TTS asociado está instalado. Si es así, el modo TTS usado por el carácter para la salida hablada y esta propiedad devuelve ese identificador de modo. Si no es así, el servidor solicita un motor de voz SAPI compatible que coincida con el **LanguageID** del carácter, así como el género y la edad establecidos para el identificador de modo compilado del carácter. Si no ha establecido el **LanguageID** del carácter, su **LanguageID** es el idioma de usuario actual. Si no se encuentra ningún motor que coincida, al consultar esta propiedad se devuelve una cadena vacía para el identificador de modo del motor. De forma similar, si consulta esta propiedad cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades de Microsoft Agent (**AudioOutput.Enabled = False),** el valor será una cadena vacía.

Al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado). Sin embargo, si el motor especificado en la configuración de TTS compilada del carácter está instalado y coincide con la configuración del identificador de idioma del carácter, el motor se cargará cuando se cargue el carácter.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en los requisitos de Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

> [!Note]  
> Esta propiedad también devuelve la cadena vacía si no tiene ninguna compatibilidad de sonido compatible instalada en el sistema.

 

> [!Note]  
> Se puede producir un error al establecer **TTSModeID** si Speech.dll no está instalado y el motor que especifique no coincide con la configuración del modo TTS compilado del carácter.

 

> [!Note]  
> La consulta de esta propiedad no suele devolver un error. Sin embargo, si el motor de voz tarda un tiempo anómalo en cargarse, es posible que reciba un error que indica que se ha producido un tiempo de espera de la consulta.

 

## <a name="see-also"></a>Consulte también

[**LanguageID, propiedad**](languageid-property.md)


 

 




