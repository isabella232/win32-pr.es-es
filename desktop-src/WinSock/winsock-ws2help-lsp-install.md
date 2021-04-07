---
description: Evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Evento WINSOCK_WS2HELP_LSP_INSTALL
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
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002518"
---
# <a name="winsock_ws2help_lsp_install-event"></a>Evento de instalación de WS2HELP de LSP de WINSOCK \_ \_ \_

> [!Note]  
> Los proveedores de servicios superpuestos están desusados. A partir de Windows 8 y Windows Server 2012, use la [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md).

 

El evento de instalación de **Winsock \_ WS2HELP \_ LSP \_** es un evento de cambio de catálogo Winsock para una operación de instalación de un proveedor de servicios por capas (LSP).


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre del LSP* 
</dt> <dd>

El nombre del LSP tal como se obtuvo del miembro **szProtocol** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.

</dd> <dt>

*Catálogo* 
</dt> <dd>

El catálogo Winsock (32 bits o 64 bits) en el que se está instalando el LSP. Es un valor entero que es 32 o 64.

</dd> <dt>

*Instalador* 
</dt> <dd>

El nombre de archivo del módulo de la aplicación que realiza la llamada de instalación de LSP.

</dd> <dt>

*GUID* 
</dt> <dd>

Valor GUID del proveedor de transporte Winsock en el que se está instalando el LSP.

</dd> <dt>

*Categoría* 
</dt> <dd>

El miembro **dwCatalogEntryId** de la estructura de [**\_ información de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para el LSP que se está instalando.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se realiza un seguimiento del evento de **\_ instalación de WS2HELP \_ LSP \_ de Winsock** para una operación de instalación de LSP cuando se instala una entrada de protocolo en el catálogo de Winsock.

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

 

 
