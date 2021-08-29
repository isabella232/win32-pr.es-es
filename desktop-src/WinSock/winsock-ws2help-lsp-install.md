---
description: Evento de cambio del catálogo de Winsock para una operación de instalación del proveedor de servicios en capas (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL evento
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 561dec21f08b5e8ad06ade54427789ece877d79af4c1b5412bb995b1ff25d065
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860605"
---
# <a name="winsock_ws2help_lsp_install-event"></a>Evento WINSOCK \_ WS2HELP \_ LSP \_ INSTALL

> [!Note]  
> Los proveedores de servicios por capas están en desuso. A partir de Windows 8 y Windows Server 2012, use [Windows filtering platform](../fwp/windows-filtering-platform-start-page.md).

 

El **evento WINSOCK \_ WS2HELP \_ LSP \_ INSTALL** es un evento de cambio del catálogo de Winsock para una operación de instalación del proveedor de servicios en capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre de LSP* 
</dt> <dd>

Nombre del LSP obtenido del miembro **szProtocol** de la estructura [**INFO de WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a instalar.

</dd> <dt>

*Catálogo* 
</dt> <dd>

El catálogo winsock (32 o 64 bits) donde se instala el LSP. Se trata de un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

Nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte winsock en el que se está instalando el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

Miembro **dwCatalogEntryId** de la [**estructura INFO \_ de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se va a instalar.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El **evento WINSOCK \_ WS2HELP \_ LSP \_ INSTALL** se sigue para una operación de instalación de LSP cuando se instala una entrada de protocolo en el catálogo de Winsock.

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

 

 
