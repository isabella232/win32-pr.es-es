---
title: WS_SECURITY_CONTEXT (WebServices.h)
description: Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266732"
---
# <a name="ws_security_context"></a>CONTEXTO DE SEGURIDAD DE WS \_ \_

Tipo opaco que se usa para hacer referencia a un [objeto de contexto de seguridad](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Observaciones

Este objeto no es seguro para subprocesos. Para obtener más información, vea [Seguridad para subprocesos.](thread-safety.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>WebServices.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Contexto de seguridad](security-context.md)
</dt> <dt>

[Seguridad para subprocesos](thread-safety.md)
</dt> </dl>

 

 





