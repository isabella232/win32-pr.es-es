---
title: Propiedad SRModeID
description: Propiedad SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704799"
---
# <a name="srmodeid-property"></a>Propiedad SRModeID

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el motor de reconocimiento de voz que utiliza el carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente ***. Caracteres ("*** CharacterID * *"). SRModeID* *  \[  =  *ModeID*\]



| Parte     | Descripción                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expresión de cadena que corresponde al identificador de modo de un motor de voz. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

La propiedad determina el motor de reconocimiento de voz usado por el carácter para la entrada de voz. El identificador de modo de un motor de reconocimiento de voz es una cadena con formato definida por el proveedor de voz que identifica de forma única el motor. Para obtener más información, consulte [acceso a un motor de voz en el código](accessing-a-speech-engine-in-your-code.md).

Si especifica un identificador de modo para un motor de voz que no está instalado, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades del agente de Microsoft) o si el idioma del motor de voz especificado no coincide con el valor de [**LanguageID**](languageid-property.md) del carácter, el servidor genera un error.

Si consulta esta propiedad y aún no lo ha hecho (correctamente) establecer el motor de reconocimiento de voz, el servidor devuelve el identificador de modo del motor que devuelve SAPI según la configuración de [**LanguageID**](languageid-property.md) del carácter. Si no ha establecido el **LanguageID** del carácter, el agente devuelve el ID. de modo del motor que SAPI devuelve según la configuración de ID. de idioma predeterminado del usuario. Si no hay ningún motor coincidente, el servidor devuelve una cadena vacía (""). Al consultar esta propiedad, no es necesario establecer [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) en **true**. Sin embargo, si consulta la propiedad cuando la entrada de voz está deshabilitada, el servidor devuelve una cadena vacía.

Cuando se habilita la entrada de voz (en la ventana Opciones de caracteres avanzadas), al consultar o establecer esta propiedad se cargará el motor asociado (si aún no está cargado) y se iniciarán los servicios de voz. Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible. (La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API. Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.

> [!Note]  
> Esta propiedad también devuelve la cadena vacía si no tiene instalado ningún soporte de sonido compatible en el sistema.

 

> [!Note]  
> Normalmente, la consulta de esta propiedad no devuelve un error. Sin embargo, si el motor de voz tarda mucho tiempo en cargarse, puede recibir un error que indica que la consulta ha superado el tiempo de espera.

 

## <a name="see-also"></a>Consulte también

[**LanguageID (propiedad)**](languageid-property.md)


 

 




