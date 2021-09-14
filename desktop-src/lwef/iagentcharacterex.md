---
title: IAgentCharacterEx
description: IAgentCharacterEx
ms.assetid: 8defc836-cc54-40c7-8afc-ec90f941861b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92a9f9c39804d6b5d3ac777457fff5b7f03823c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127258028"
---
# <a name="iagentcharacterex"></a>IAgentCharacterEx

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

**IAgentCharacterEx** deriva de la [**interfaz IAgentCharacter.**](iagentcharacter.md) Incluye todos los **métodos IAgentCharacter,** así como proporciona acceso a funciones adicionales.

**Métodos en orden de Vtable**



| Métodos IAgentCharacterEx                                         | Descripción                                                                    |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)         | Muestra el menú emergente del carácter.                                    |
| [**SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md)   | Establece si el servidor muestra automáticamente el menú emergente del carácter.    |
| [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md)   | Devuelve si el servidor muestra automáticamente el menú emergente del carácter. |
| [**GetHelpFileName**](iagentcharacterex--gethelpfilename.md)     | Devuelve el nombre de archivo de ayuda del carácter.                                   |
| [**SetHelpFileName**](iagentcharacterex--sethelpfilename.md)     | Establece el nombre de archivo de ayuda del carácter.                                      |
| [**SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)         | Establece el modo de Ayuda en .                                                             |
| [**GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md)         | Devuelve si el modo de Ayuda está en.                                               |
| [**SetHelpContextID**](iagentcharacterex--sethelpcontextid.md)   | Establece helpContextID para el carácter.                                      |
| [**GetHelpContextID**](iagentcharacterex--gethelpcontextid.md)   | Devuelve el HelpContextID del carácter.                                   |
| [**GetActive**](iagentcharacterex--getactive.md)                 | Devuelve el estado activo del carácter.                                    |
| [**Escucha**](iagentcharacterex--listen.md)                       | Establece el estado de escucha del carácter.                                    |
| [**SetLanguageID**](iagentcharacterex--setlanguageid.md)         | Establece el identificador de idioma del carácter.                                        |
| [**getLanguageID**](iagentcharacterex--getlanguageid.md)         | Devuelve el identificador de idioma del carácter.                                     |
| [**getTTSModeID**](iagentcharacterex--getttsmodeid.md)           | Devuelve el identificador de modo TTS establecido para el carácter.                                 |
| [**SetTTSModeID**](iagentcharacterex--setttsmodeid.md)           | Establece el identificador de modo TTS para el carácter.                                        |
| [**getSRModeID**](iagentcharacterex--getsrmodeid.md)             | Devuelve el identificador de modo del motor de reconocimiento de voz actual.                       |
| [**setSRModeID**](iagentcharacterex--setsrmodeid.md)             | Establece el motor de reconocimiento de voz.                                            |
| [**GetGUID**](iagentcharacterex--getguid.md)                     | Devuelve el identificador del carácter.                                            |
| [**GetOriginalSize**](iagentcharacterex--getoriginalsize.md)     | Devuelve el tamaño original del marco de caracteres.                              |
| [**Pensar**](iagentcharacterex--think.md)                         | Muestra el texto especificado en el globo de "reflexión" del carácter.              |
| [**GetVersion**](iagentcharacterex--getversion.md)               | Devuelve la versión del carácter.                                          |
| [**GetAnimationNames**](iagentcharacterex--getanimationnames.md) | Devuelve los nombres de las animaciones del carácter.                         |
| [**getSRStatus**](iagentcharacterex--getsrstatus.md)             | Devuelve las condiciones necesarias para admitir la entrada de voz.                      |



 

 

 




