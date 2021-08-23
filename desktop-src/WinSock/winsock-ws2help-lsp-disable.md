---
description: Evento de cambio de catálogo de Winsock para una operación de deshabilitación del proveedor de servicios en capas (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE evento
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
ms.openlocfilehash: 578479710856e149760202699be13d4b30b50709f6ea9b389e055793a8b0ca94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733141"
---
# <a name="winsock_ws2help_lsp_disable-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows de filtrado.](../fwp/windows-filtering-platform-start-page.md)

 

El **evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE** es un evento de cambio de catálogo de Winsock para una operación de deshabilitación del proveedor de servicios en capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de LSP* 
</dt> <dd>

Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**\_ INFO de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está deshabilitando.

</dd> <dt>

*Catálogo* 
</dt> <dd>

Catálogo de Winsock (32 o 64 bits) donde se deshabilita el LSP. Se trata de un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

Nombre de archivo del módulo de la aplicación que realiza la llamada de deshabilitación de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte Winsock al que se está deshabilitando el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

Miembro **dwCatalogEntryId de** la [**estructura INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está deshabilitando.

</dd> </dl>

Este evento no tiene parámetros.

## <a name="remarks"></a>Comentarios

El **evento WINSOCK \_ WS2HELP \_ LSP \_ DISABLE** se sigue para una operación de deshabilitación de LSP cuando se deshabilita una entrada de protocolo en el catálogo winsock.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 
