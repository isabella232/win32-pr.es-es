---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdaf3ea460a76549112741ac77f83e10ec37cd9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780130"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indica el estado de procesamiento de inactividad automático para un carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Dirección de una variable que recibe **true** si el servidor de agente de Microsoft reproduce automáticamente animaciones de estado de **ralentí** para un carácter y **false** en caso contrario.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




