---
title: IAgentCharacter GetVisibilityCause
description: IAgentCharacter GetVisibilityCause
ms.assetid: 46f681de-1c99-4f90-a3fe-aae04bb75339
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdae2465ccc9e7153a0e9cc8202027137e2a7c0f07fdfb5da2a83a7c0d1ed1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962245"
---
# <a name="iagentcharactergetvisibilitycause"></a>IAgentCharacter::GetVisibilityCause

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetVisibilityCause(
   long * pdwCause  // address of variable for cause of character visible state
);
```

Recupera la causa del estado visible del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwCause"></span><span id="pdwcause"></span><span id="PDWCAUSE"></span>*pdwCause*
</dt> <dd>

Dirección de una variable que recibe la causa del último cambio de estado de visibilidad del carácter y será una de las siguientes:



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


 

 





