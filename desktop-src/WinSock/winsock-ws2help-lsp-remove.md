---
description: Evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: Evento WINSOCK_WS2HELP_LSP_REMOVE
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
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697476"
---
# <a name="winsock_ws2help_lsp_remove-event"></a>\_Evento de \_ eliminación de LSP de Winsock WS2HELP \_

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El evento de eliminación de **\_ \_ LSP \_ de Winsock WS2HELP** es un evento de cambio de catálogo Winsock para una operación de eliminación de un proveedor de servicios por capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre del LSP* 
</dt> <dd>

Nombre del LSP obtenido del miembro **szProtocol** de la estructura de información de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.

</dd> <dt>

*Catálogo* 
</dt> <dd>

El catálogo Winsock (32 bits o 64 bits) en el que se va a quitar el LSP. Es un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

El nombre de archivo del módulo de la aplicación que realiza la llamada Remove de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte Winsock del que se va a quitar el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a quitar.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento de eliminación de **\_ \_ LSP \_ de Winsock WS2HELP** para una operación de eliminación de LSP cuando se quita una entrada de protocolo del catálogo de Winsock.

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

 

 
