---
description: Tipo de datos opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 792b81516e434469750b4ddd667bf6ddb82df31f4f13f82588d281f743bc8835
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118921044"
---
# <a name="plsa_client_request"></a>SOLICITUD DE CLIENTE \_ PLSA \_

El **tipo de datos \_ PLSA CLIENT \_ REQUEST** es un tipo de datos opaco.

La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) la usa internamente para mantener la información de cliente relacionada con solicitudes individuales.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ntsecpkg.h</dt> </dl> |



 

 
