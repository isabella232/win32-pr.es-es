---
title: WS_SECURITY_CONTEXT (WebServices.h)
description: Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34f201c40e3079a3c26ced97e2664679f04ccec6b7804844dd305422abadfdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192361"
---
# <a name="ws_security_context"></a>CONTEXTO DE SEGURIDAD DE WS \_ \_

Tipo opaco que se usa para hacer referencia a un [objeto de contexto de seguridad](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Comentarios

Este objeto no es seguro para subprocesos. Para obtener más información, vea [Seguridad para subprocesos.](thread-safety.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>WebServices.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Contexto de seguridad](security-context.md)
</dt> <dt>

[Seguridad para subprocesos](thread-safety.md)
</dt> </dl>

 

 





