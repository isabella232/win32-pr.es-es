---
description: Evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Evento WINSOCK_WS2HELP_LSP_DISABLE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648551"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>\_Evento de \_ \_ deshabilitación de LSP de Winsock WS2HELP

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El evento **Winsock \_ WS2HELP \_ LSP \_ Disable** es un evento de cambio de catálogo Winsock para una operación de deshabilitación de un proveedor de servicios por capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre del LSP* 
</dt> <dd>

Nombre del LSP tal y como se obtiene del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.

</dd> <dt>

*Catálogo* 
</dt> <dd>

El catálogo Winsock (32 bits o 64 bits) en el que se deshabilita el LSP. Es un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

El nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte Winsock en el que se va a deshabilitar el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a deshabilitar.

</dd> </dl>

Este evento no tiene parámetros.

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento de **\_ \_ \_ deshabilitación de LSP de Winsock WS2HELP** para una operación de deshabilitación de LSP cuando una entrada de protocolo está deshabilitada en el catálogo de Winsock.

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

 

 
