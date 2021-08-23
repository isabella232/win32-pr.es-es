---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4ff8e6dc87eb1a5fa5c3e79fe26b00d8bd3c8eb18a5fc6ca7cac22d3dfd07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976265"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

[**IAgentCommandsEx**](iagentcommandex.md) define una interfaz que extiende la [**interfaz IAgentCommands.**](iagentcommands.md)

**Métodos en orden de Vtable**



| Métodos IAgentCommandsEx                                                             | Descripción                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Establece el comando predeterminado para el menú emergente del carácter.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Devuelve el comando predeterminado del menú emergente del carácter.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Establece el identificador del tema de ayuda contextual para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Devuelve el identificador del tema de ayuda contextual para un [**objeto Command.**](/windows/desktop/lwef/the-command-object)                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Establece la fuente que se va a usar en el menú emergente del carácter.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Devuelve la fuente utilizada en el menú emergente del carácter.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Establece el tamaño de fuente que se va a usar en el menú emergente del carácter.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Devuelve el tamaño de fuente utilizado en el menú emergente del carácter.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Establece el título de voz del objeto [**Command del**](/windows/desktop/lwef/the-command-object) carácter.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Devuelve el título de voz del objeto [**Command del**](/windows/desktop/lwef/the-command-object) carácter.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Agrega un [**objeto Command**](/windows/desktop/lwef/the-command-object) a una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object)    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una [**colección Commands.**](/windows/desktop/lwef/the-commands-collection-object) |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Habilita la gramática de voz para los comandos globales del Agente.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Devuelve si la gramática de voz de los comandos globales del Agente está habilitada.                                     |



 

 

 