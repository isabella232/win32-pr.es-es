---
title: Anulación del registro de IAgent
description: Anulación del registro de IAgent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6101d0473e8563e8b0899e2f5d0bd2a440c31d17b4a0c142b43f47855ddf166b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976485"
---
# <a name="iagentunregister"></a>IAgent::Unregister

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Descarga los datos de caracteres para el carácter especificado de la [**colección**](/windows/desktop/lwef/the-characters-object) Characters.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

Identificador del receptor de notificación.

</dd> </dl>

Use este método cuando ya no necesite servicios de Microsoft Agent, como cuando se cierre la aplicación.

## <a name="see-also"></a>Consulte también

[**IAgent::Register**](iagent--register.md)


 

 