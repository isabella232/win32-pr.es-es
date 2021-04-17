---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714379"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) define una interfaz que extiende la interfaz [**IAgentCommands**](iagentcommands.md) .

**Métodos en orden de Vtable**



| Métodos IAgentCommandsEx                                                             | Descripción                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Establece el comando predeterminado para el menú emergente del carácter.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Devuelve el comando predeterminado del menú emergente del carácter.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Establece el identificador del tema de ayuda contextual de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Devuelve el identificador del tema de ayuda contextual de un objeto de [**comando**](/windows/desktop/lwef/the-command-object) .                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Establece la fuente que se va a usar en el menú emergente del carácter.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Devuelve la fuente utilizada en el menú emergente del carácter.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Establece el tamaño de fuente que se va a usar en el menú emergente del carácter.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Devuelve el tamaño de fuente utilizado en el menú emergente del carácter.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Establece el título de la voz para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) del carácter.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Devuelve el título de la voz para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) del carácter.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Agrega un objeto [**Command**](/windows/desktop/lwef/the-command-object) a una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) . |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Habilita la gramática de voz para los comandos globales del agente.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Devuelve si la gramática de voz para los comandos globales del agente está habilitada.                                     |



 

 

 