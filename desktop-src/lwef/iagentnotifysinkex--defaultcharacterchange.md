---
title: IAgentNotifySinkEx DefaultCharacterChange
description: IAgentNotifySinkEx DefaultCharacterChange
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359144"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>IAgentNotifySinkEx::D efaultCharacterChange

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Notifica a una aplicación cliente cuándo cambia el carácter predeterminado.

-   No de devuelve ningún valor.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*
</dt> <dd>

Identificador único del carácter.

</dd> </dl>

Cuando el usuario cambia el carácter asignado como carácter predeterminado del usuario, el servidor envía este evento a los clientes que han cargado el carácter predeterminado. El evento devuelve el identificador único (GUID) del carácter con formato de llaves y guiones, que se define cuando el carácter se ha creado con el Editor de caracteres de Microsoft Agent.

Cuando aparece el nuevo carácter, se supone que tiene el mismo tamaño que cualquier instancia ya cargada del carácter o el carácter predeterminado anterior (en ese orden).

## <a name="see-also"></a>Consulte también

[**IAgent::Load**](iagent--load.md)


 

 




