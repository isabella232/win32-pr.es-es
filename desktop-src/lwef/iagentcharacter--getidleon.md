---
title: IAgentCharacter GetIdleOn
description: IAgentCharacter GetIdleOn
ms.assetid: e5371326-33d0-4ecc-bda7-28f36f46ddeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a5ce64b39b615325a3de55c1643004cffaeecf89e2e0a024d317bb56e32d4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478379"
---
# <a name="iagentcharactergetidleon"></a>IAgentCharacter::GetIdleOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetIdleOn(
   long * pbOn  // address of idle processing flag
);
```

Indica el estado de procesamiento de inactividad automático para un carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Dirección de una variable que recibe **True si** el servidor de Microsoft Agent reproduce automáticamente animaciones de estado de **idling** para un carácter y **False** si no es así.

</dd> </dl>

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetIdleOn**](iagentcharacter--setidleon.md)


 

 




