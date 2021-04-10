---
title: WS_SECURITY_CONTEXT (webservices. h)
description: Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150472"
---
# <a name="ws_security_context"></a>\_contexto de seguridad de WS \_

Tipo opaco que se usa para hacer referencia a un [objeto de contexto de seguridad](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Observaciones

Este objeto no es seguro para subprocesos. Para obtener más información, vea [seguridad para subprocesos](thread-safety.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Webservices. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Contexto de seguridad](security-context.md)
</dt> <dt>

[Seguridad para subprocesos](thread-safety.md)
</dt> </dl>

 

 





