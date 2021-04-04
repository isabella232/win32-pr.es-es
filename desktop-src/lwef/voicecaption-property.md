---
title: Propiedad VoiceCaption (objeto Commands)
description: Propiedad VoiceCaption
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa7d4a8ea9ff1cdd4a5792fca58231f203e21ac
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800758"
---
# <a name="voicecaption-property-commands-object"></a>Propiedad VoiceCaption (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el texto que se muestra para el objeto de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) en la ventana comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*Caracteres Agent. ***("**_CharacterID_*_"). Cadena Commands. VoiceCaption_ *  \[  =  \]



| Parte     | Descripción                                               |
|----------|-----------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto que se muestra. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si establece la propiedad [**Voice**](voice-property.md) de la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) , normalmente también establecerá su propiedad **VoiceCaption** . La configuración de texto **VoiceCaption** aparece en la ventana comandos de voz cuando la aplicación cliente es de entrada-activa y el carácter está visible. Si no se establece esta propiedad, el valor de la propiedad [**título**](caption-property.md) de la colección de **comandos** determina el texto que se muestra. Cuando no se establece la propiedad **VoiceCaption** o **Caption** , los comandos de la colección aparecen en la ventana comandos de voz en "(comando no definido)" cuando la aplicación cliente pasa a ser de entrada activa.

La configuración **VoiceCaption** también determina el texto que se muestra en la sugerencia de escucha para indicar los comandos para los que el carácter realiza escuchas.

## <a name="see-also"></a>Consulte también

[Propiedad Caption](caption-property.md)


 

 
