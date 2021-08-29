---
title: IAgentNotifySink VisibleState
description: IAgentNotifySink VisibleState
ms.assetid: b0346296-74e9-448f-aa6d-a9fb1e645f05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4ba168fa538cf176de57a8638d7603fd5bc6e990a1b83837ba603b3a62c4236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961515"
---
# <a name="iagentnotifysinkvisiblestate"></a>IAgentNotifySink::VisibleState

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT VisibleState(
   long dwCharID,  // character ID
   long bVisible,  // visibility flag
   long dwCause,   // cause of visible state
);                          
```

Notifica a una aplicación cliente cuándo cambia el estado de visibilidad del carácter.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificador del carácter cuyo estado de visibilidad cambia.

</dd> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Marca de visibilidad. Este valor booleano es **True cuando** el carácter se vuelve visible y **False** cuando el carácter se oculta.

</dd> <dt>

<span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*
</dt> <dd>

Causa del último cambio en el estado de visibilidad del carácter. El parámetro puede ser uno de los siguientes:



| Value                                                                   | Descripción                                                                                 |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| **const unsigned short** **NeverShown = 0;**<br/>                 | No se ha mostrado el carácter.                                                               |
| **const unsigned short** **UserHid = 1;**<br/>                    | El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz. |
| **const unsigned short** **UserShowed = 2;**<br/>                 | El usuario mostró el carácter.                                                                  |
| **const unsigned short** **ProgramHid = 3;**<br/>                 | La aplicación ocultó el carácter.                                                         |
| **const unsigned short** **ProgramShowed = 4;**<br/>              | La aplicación mostró el carácter.                                                      |
| **const unsigned short** **OtherProgramHid = 5;**<br/>            | Otra aplicación ocultó el carácter.                                                      |
| **const unsigned short** **OtherProgramShowed = 6;**<br/>         | Otra aplicación mostró el carácter.                                                   |
| **const unsigned short** **UserHidViaCharacterMenu = 7**<br/>     | El usuario ocultó el carácter con el menú emergente del carácter.                                    |
| **const unsigned short** **UserHidViaTaskbarIcon = UserHid**<br/> | El usuario ocultó el carácter con el menú emergente del icono de la barra de tareas del carácter o con la entrada de voz. |



 

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetVisible**](iagentcharacter--getvisible.md), [ **IAgentCharacter::GetVisibilityCause**](iagentcharacter--getvisibilitycause.md)


 

 





