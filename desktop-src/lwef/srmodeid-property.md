---
title: Propiedad SRModeID
description: Propiedad SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465727"
---
# <a name="srmodeid-property"></a>Propiedad SRModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el motor de reconocimiento de voz que usa el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent***. Characters("**_CharacterID_*_"). SRModeID_ *  \[  =  *ModeID*\]



| Parte     | Descripción                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expresión de cadena que corresponde al identificador de modo de un motor de voz. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad determina el motor de reconocimiento de voz utilizado por el carácter para la entrada de voz. El identificador de modo de un motor de reconocimiento de voz es una cadena con formato definida por el proveedor de voz que identifica de forma única el motor. Para obtener más información, vea [Acceso a un motor de voz en el código.](accessing-a-speech-engine-in-your-code.md)

Si especifica un identificador de modo para un motor de voz que no está instalado, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades de Microsoft Agent) o si el idioma del motor de voz especificado no coincide con la configuración de [**LanguageID**](languageid-property.md) del carácter, el servidor genera un error.

Si consulta esta propiedad y aún no ha establecido (correctamente) el motor de reconocimiento de voz, el servidor devuelve el identificador de modo del motor que devuelve SAPI en función de la configuración de [**LanguageID**](languageid-property.md) del carácter. Si no ha establecido el **LanguageID** del carácter, el Agente devuelve el identificador de modo del motor que devuelve SAPI en función de la configuración predeterminada del identificador de idioma del usuario. Si no hay ningún motor que coincida, el servidor devuelve una cadena vacía (""). La consulta de esta propiedad no requiere que [**SpeechInput.Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) esté establecido en **True.** Sin embargo, si consulta la propiedad cuando la entrada de voz está deshabilitada, el servidor devuelve una cadena vacía.

Cuando la entrada de voz está habilitada (en la ventana Opciones avanzadas de caracteres), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) e iniciará los servicios de voz. Es decir, la clave de escucha está disponible y se puede mostrar la sugerencia de escucha. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en Opciones avanzadas de caracteres). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia los servicios de voz.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en los requisitos de Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el Agente .

> [!Note]  
> Esta propiedad también devuelve la cadena vacía si no tiene ninguna compatibilidad de sonido compatible instalada en el sistema.

 

> [!Note]  
> La consulta de esta propiedad no suele devolver un error. Sin embargo, si el motor de voz tarda un tiempo anómalo en cargarse, es posible que reciba un error que indica que se ha producido un tiempo de espera de la consulta.

 

## <a name="see-also"></a>Consulte también

[**LanguageID, propiedad**](languageid-property.md)


 

 




