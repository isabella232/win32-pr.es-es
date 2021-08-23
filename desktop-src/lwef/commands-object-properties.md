---
title: Propiedades del objeto Commands
description: Propiedades del objeto Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b9e8f8e6e7b44697891cd567fce8ca0f5db13a0142936b5cf48bdb52721392
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716545"
---
# <a name="commands-object-properties"></a>Propiedades del objeto Commands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

El servidor admite las siguientes propiedades para la [**colección Commands:**](/windows/desktop/lwef/the-commands-collection-object)

-   [**Caption**](caption-property-cmds.md)
-   [**Contar**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**HelpContextID**](helpcontextid-property.md)
-   [**Visible**](visible-property-cso.md)
-   [**Voz**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Puede aparecer una entrada [**para la**](/windows/desktop/lwef/the-commands-collection-object) colección Comandos en el menú emergente y en la ventana Comandos de voz de un carácter. Para que esta entrada aparezca en el menú emergente, establezca su [**propiedad Caption.**](caption-property-cmds.md) Para incluir la entrada en la ventana Comandos de voz, establezca su [**propiedad VoiceCaption.**](voicecaption-property.md) (Para la compatibilidad con versiones anteriores, si no hay **voiceCaption**, se usa la **opción Título)**

En la tabla siguiente se resume cómo las propiedades de un [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) afectan a la presentación de la entrada:



| Propiedad Caption                                                                                                                                                                                                                                            | Voice-Caption propiedad | Propiedad Voice | Propiedad Visible | Aparece en el menú emergente del carácter | Aparece en la ventana Comandos de voz |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sí                                                                                                                                                                                                                                                         | Sí                    | Sí            | Verdadero             | Sí, mediante título                 | Sí, con VoiceCaption          |
| Sí                                                                                                                                                                                                                                                         | Sí                    | No             | Verdadero             | Sí, mediante título                 | No                               |
| Sí                                                                                                                                                                                                                                                         | Sí                    | Sí            | False            | No                                 | Sí, con VoiceCaption          |
| Sí                                                                                                                                                                                                                                                         | Sí                    | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sí                    | Sí            | True             | No                                 | Sí, con VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sí                    | Sí            | False            | No                                 | Sí, con VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sí                    | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sí                    | No             | False            | No                                 | No                               |
| Sí                                                                                                                                                                                                                                                         | No1                    | Sí            | Verdadero             | Sí, mediante título                 | Sí, mediante título               |
| Sí                                                                                                                                                                                                                                                         | No                     | No             | True             | Sí                                | No                               |
| Sí                                                                                                                                                                                                                                                         | No                     | Sí            | False            | No                                 | Sí, mediante título               |
| Sí                                                                                                                                                                                                                                                         | No                     | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sí            | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sí            | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | False            | No                                 | No                               |
|  Si el valor de la propiedad es NULL. En algunos lenguajes de programación, es posible que una cadena vacía no se interprete como la misma que una cadena nula.  El comando sigue siendo accesible por voz y aparece en la ventana Comandos de voz como "(command undefined)".<br/> |                        |                |                  |                                    |                                  |



 

 

