---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704705"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx::D efaultCharacterChange

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Notifica a una aplicación cliente cuando cambia el carácter predeterminado.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

Identificador único del carácter.

</dd> </dl>

Cuando el usuario cambia el carácter asignado como carácter predeterminado del usuario, el servidor envía este evento a los clientes que han cargado el carácter predeterminado. El evento devuelve el identificador único (GUID) del carácter con formato con llaves y guiones, que se define cuando el carácter se crea con el editor de caracteres del agente de Microsoft.

Cuando aparece el nuevo carácter, se da por supuesto que tiene el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).

## <a name="see-also"></a>Consulte también

[**IAgent:: Load**](iagent--load.md)


 

 




