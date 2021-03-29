---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6013385144b82b79a0f17ae6443b094a9d9c8a4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419202"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Recupera la causa del estado visible del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Dirección de una variable que recibe la causa del último cambio de estado de visibilidad del carácter y será uno de los siguientes:



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

[**IAgentNotifySink::VisibleState**](iagentnotifysink--visiblestate.md)


 

 





