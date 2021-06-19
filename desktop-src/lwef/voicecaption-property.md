---
title: Propiedad VoiceCaption (objeto Commands)
description: Obtenga información sobre la propiedad VoiceCaption del objeto Commands, que devuelve o establece el texto que se muestra para el objeto Commands en la ventana Comandos de voz.
ms.assetid: 2c4fa175-fc2d-4474-b15f-7e838103a435
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4a2113e0a952f253df901d192b42466fa30350
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396130"
---
# <a name="voicecaption-property-commands-object"></a>Propiedad VoiceCaption (objeto Commands)

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el texto que se muestra para el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) en la ventana Comandos de voz.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Caracteres("**_CharacterID_*_"). Cadena Commands.VoiceCaption_ *  \[  =  \]



| Parte     | Descripción                                               |
|----------|-----------------------------------------------------------|
| *string* | Expresión de cadena que se evalúa como el texto mostrado. |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Si establece la [**propiedad Voice**](voice-property.md) de la [**colección Commands,**](/windows/desktop/lwef/the-commands-collection-object) normalmente también establecerá su **propiedad VoiceCaption.** La **configuración de texto VoiceCaption** aparece en la ventana Comandos de voz cuando la aplicación cliente está activa en la entrada y el carácter está visible. Si no se establece esta propiedad, la configuración de la propiedad [**Caption**](caption-property.md) de la colección **Commands** determina el texto mostrado. Cuando no se establece la propiedad **VoiceCaption** o **Caption,** los comandos de la colección aparecen en la ventana Comandos de voz en "(undefined command)" cuando la aplicación cliente se convierte en input-active.

El **valor VoiceCaption** también determina el texto que se muestra en la sugerencia de escucha para indicar los comandos para los que escucha el carácter.

## <a name="see-also"></a>Consulte también

[Propiedad Caption](caption-property.md)


 

 
