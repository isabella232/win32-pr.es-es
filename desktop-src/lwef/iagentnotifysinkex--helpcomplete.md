---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077624"
---
# <a name="iagentnotifysinkexhelpcomplete"></a>IAgentNotifySinkEx::HelpComplete

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

Notifica a una aplicación cliente cuando el usuario selecciona un comando o un carácter para completar el modo de ayuda.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter para el que se ha completado el modo de ayuda.

</dd> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificador del comando seleccionado por el usuario.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

La causa del evento, que puede ser los valores siguientes:



| Value                                                                         | Descripción                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| **const unsigned short** **CSHELPCAUSE \_ comando = 1;**<br/>             | El usuario seleccionó un comando proporcionado por la aplicación.                            |
| **const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**<br/>        | El usuario seleccionó el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente. |
| **const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**<br/>  | El usuario seleccionó el comando abrir comandos de voz.                                   |
| **const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**<br/> | El usuario seleccionó el comando cerrar comandos de voz.                                  |
| **const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**<br/>       | El usuario seleccionó el comando show *nombredecarácter* .                                  |
| **const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**<br/>       | El usuario seleccionó el comando ocultar *nombredecarácter* .                                  |
| **const unsigned short** **CSHELPCAUSE \_ carácter = 7;**<br/>           | El usuario seleccionó (hizo clic en) el carácter.                                           |



 

</dd> </dl>

Normalmente, el modo de ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter. Al hacer clic en otro carácter o en cualquier otro lugar de la pantalla, no se cancela el modo de ayuda. El cliente que establece el modo de ayuda para el carácter puede cancelar el modo de ayuda estableciendo [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) en **false**. (Esto no desencadena el evento **IAgentNotifySinkEx:: HelpComplete** ).

Cuando el usuario selecciona un comando en el menú emergente del carácter en el modo de ayuda, el servidor quita el menú, llama a ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento. La información contextual (también conocida como esto?) La ventana de ayuda se muestra en la ubicación del puntero. Si el usuario selecciona el comando por entrada de voz, se muestra la ventana de ayuda sobre el carácter. Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.

Si el servidor devuelve *dwCommandID* como una cadena vacía (""), indica que el usuario seleccionó un comando proporcionado por el servidor.

Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de ayuda.

## <a name="see-also"></a>Consulte también

[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)


 

