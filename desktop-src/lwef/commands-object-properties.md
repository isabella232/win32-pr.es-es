---
title: Propiedades del objeto Commands
description: Propiedades del objeto Commands
ms.assetid: 889a56b2-0b6d-4df8-a313-7553371e4413
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4493b1e146a011434f7a0324a4008031a575d2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077588"
---
# <a name="commands-object-properties"></a>Propiedades del objeto Commands

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

El servidor admite las siguientes propiedades para la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) :

-   [**Caption**](caption-property-cmds.md)
-   [**Contabiliza**](count-property.md)
-   [**DefaultCommand**](defaultcommand-property.md)
-   [**FontName**](fontname-property.md)
-   [**FontSize**](fontsize-property.md)
-   [**GlobalVoiceCommandsEnabled**](globalvoicecommandsenabled-property.md)
-   [**IDDelContextoDeAyuda**](helpcontextid-property.md)
-   [**Visible**](visible-property-cso.md)
-   [**Voz**](voice-property.md)
-   [**VoiceCaption**](voicecaption-property.md)

Una entrada para la colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) puede aparecer en el menú emergente y en la ventana comandos de voz para un carácter. Para que esta entrada aparezca en el menú emergente, establezca su propiedad [**título**](caption-property-cmds.md) . Para incluir la entrada en la ventana comandos de voz, establezca su propiedad [**VoiceCaption**](voicecaption-property.md) . (Para mantener la compatibilidad con versiones anteriores, si no hay ningún **VoiceCaption**, se usa la configuración del **título** )

En la tabla siguiente se resume el modo en que las propiedades de un objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) afectan a la presentación de la entrada:



| Propiedad Caption                                                                                                                                                                                                                                            | Propiedad Voice-Caption | Propiedad Voice | Propiedad visible | Aparece en el menú emergente del carácter | Aparece en la ventana comandos de voz |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|----------------|------------------|------------------------------------|----------------------------------|
| Sí                                                                                                                                                                                                                                                         | Sí                    | Sí            | True             | Sí, usar título                 | Sí, uso de VoiceCaption          |
| Sí                                                                                                                                                                                                                                                         | Sí                    | No             | True             | Sí, usar título                 | No                               |
| Sí                                                                                                                                                                                                                                                         | Sí                    | Sí            | False            | No                                 | Sí, uso de VoiceCaption          |
| Sí                                                                                                                                                                                                                                                         | Sí                    | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sí                    | Sí            | True             | No                                 | Sí, uso de VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sí                    | Sí            | False            | No                                 | Sí, uso de VoiceCaption          |
| No                                                                                                                                                                                                                                                          | Sí                    | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | Sí                    | No             | False            | No                                 | No                               |
| Sí                                                                                                                                                                                                                                                         | No1                    | Sí            | True             | Sí, usar título                 | Sí, usar título               |
| Sí                                                                                                                                                                                                                                                         | No                     | No             | True             | Sí                                | No                               |
| Sí                                                                                                                                                                                                                                                         | No                     | Sí            | False            | No                                 | Sí, usar título               |
| Sí                                                                                                                                                                                                                                                         | No                     | No             | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sí            | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | Sí            | False            | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | True             | No                                 | No                               |
| No                                                                                                                                                                                                                                                          | No                     | No             | False            | No                                 | No                               |
|  Si el valor de la propiedad es NULL. En algunos lenguajes de programación, una cadena vacía no puede interpretarse igual que una cadena nula.  El comando sigue siendo accesible mediante voz y aparece en la ventana comandos de voz como "(comando sin definir)".<br/> |                        |                |                  |                                    |                                  |



 

 

