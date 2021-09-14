---
description: Tipo de datos opaco.
ms.assetid: 384dd6e0-726f-4100-a036-1cca6a332a64
title: PLSA_CLIENT_REQUEST (Ntsecpkg.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3685c3cd38843edfd4ae708a18761b6ee698c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173378"
---
# <a name="plsa_client_request"></a>SOLICITUD DE CLIENTE \_ PLSA \_

El **tipo de datos \_ PLSA CLIENT \_ REQUEST** es un tipo de datos opaco.

La [*autoridad de seguridad local*](../secgloss/l-gly.md) (LSA) la usa internamente para mantener la información de cliente relacionada con solicitudes individuales.


```C++
#include <windows.h>

typedef PVOID *PLSA_CLIENT_REQUEST;
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Ntsecpkg.h</dt> </dl> |



 

 
