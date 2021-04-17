---
description: Evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Evento WINSOCK_WS2HELP_LSP_RESET
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
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697475"
---
# <a name="winsock_ws2help_lsp_reset-event"></a>\_Evento de \_ restablecimiento de LSP de WS2HELP de Winsock \_

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El evento de **\_ restablecimiento de \_ LSP \_ de Winsock WS2HELP** es un evento de cambio de catálogo Winsock para una operación de restablecimiento del catálogo Winsock.


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Catálogo* 
</dt> <dd>

Catálogo Winsock (32 bits o 64 bits) que se va a restablecer. Es un valor entero que es 32 o 64.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento **Winsock \_ WS2HELP \_ LSP \_ RESET** para una operación de proveedor de servicios por capas (LSP) de Winsock cuando se restablece el catálogo Winsock.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Control de seguimiento de Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Seguimiento de Winsock](winsock-tracing.md)
</dt> <dt>

[Niveles de seguimiento de Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalles de seguimiento de cambios de catálogo Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
