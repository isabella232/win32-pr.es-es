---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6ad0cc7212a7e7bedbcb968f9b9d2a658f520f1a3593595ff03091b03ba32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749567"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Notifica a una aplicación cliente cuando el usuario selecciona un comando o carácter para completar el modo de Ayuda.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter para el que se completó el modo de Ayuda.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador del comando seleccionado por el usuario.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del evento, que puede ser los siguientes valores:



| Valor                                                                         | Descripción                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **CSHELPCAUSE \_ COMMAND = 1;**<br/>             | El usuario seleccionó un comando proporcionado por la aplicación.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | El usuario seleccionó el [**objeto Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | El usuario seleccionó el comando Abrir comandos de voz.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | El usuario seleccionó el comando Cerrar comandos de voz.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | El usuario seleccionó el comando *Mostrar nombreDeEquipo.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | El usuario seleccionó el comando *Hide CharacterName.*                                  |
| **const unsigned short** **CSHELPCAUSE \_ CHARACTER = 7;**<br/>           | El usuario seleccionó (hizo clic) en el carácter.                                           |



 

</dd> </dl>

Normalmente, el modo ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter. Al hacer clic en otro carácter o en otro lugar de la pantalla, no se cancela el modo de Ayuda. El cliente que establece el modo de Ayuda para el carácter puede cancelar el modo de Ayuda estableciendo [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) en **False.** (Esto no desencadena el **evento IAgentNotifySinkEx::HelpComplete).**

Cuando el usuario selecciona un comando del menú emergente del carácter en modo ayuda, el servidor quita el menú, llama a Ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento. Contextual (también conocido como What's This?) La ventana ayuda se muestra en la ubicación del puntero. Si el usuario selecciona el comando por entrada de voz, se muestra la ventana Ayuda sobre el carácter. Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.

Si el servidor devuelve *dwCommandID como* una cadena vacía (""), indica que el usuario ha seleccionado un comando proporcionado por el servidor.

Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de Ayuda.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

