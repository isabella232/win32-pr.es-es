---
description: Evento de cambio del catálogo de Winsock para una operación de restablecimiento del catálogo de Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3c9a638d962db908b24387d7baeb2f34d4e09ece561fdd1796a8a44930a5dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051293"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ RESET

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows filtering platform](../fwp/windows-filtering-platform-start-page.md).

 

El **evento WINSOCK \_ WS2HELP \_ LSP \_ RESET** es un evento de cambio del catálogo de Winsock para una operación de restablecimiento del catálogo de Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Catálogo* 
</dt> <dd>

Catálogo de Winsock (32 o 64 bits) que se va a restablecer. Se trata de un valor entero que es 32 o 64.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **evento WINSOCK \_ WS2HELP \_ LSP \_ RESET** se sigue para una operación del proveedor de servicios en capas (LSP) de Winsock cuando se restablece el catálogo de Winsock.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control del seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles del seguimiento de cambios del catálogo de Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
