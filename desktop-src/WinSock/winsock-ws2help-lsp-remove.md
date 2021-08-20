---
description: Evento de cambio del catálogo de Winsock para una operación de eliminación del proveedor de servicios por capas (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: b0ac13a5404dcbbfe5fb5f5d8c2a5f17d43edeb72ba135abfc7e85ad9e5227a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321597"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows de filtrado.](../fwp/windows-filtering-platform-start-page.md)

 

El **evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE** es un evento de cambio de catálogo de Winsock para una operación de eliminación del proveedor de servicios en capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de LSP* 
</dt> <dd>

Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**\_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.

</dd> <dt>

*Catálogo* 
</dt> <dd>

Catálogo de Winsock (32 o 64 bits) donde se quita el LSP. Se trata de un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

Nombre de archivo del módulo de la aplicación que realiza la llamada de eliminación de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte Winsock del que se va a quitar el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

Miembro **dwCatalogEntryId de** la [**estructura INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **evento WINSOCK \_ WS2HELP \_ LSP \_ REMOVE** se sigue para una operación de eliminación de LSP cuando se quita una entrada de protocolo del catálogo winsock.

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

 

 
