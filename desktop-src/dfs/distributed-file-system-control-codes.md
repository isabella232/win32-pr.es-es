---
title: Sistema de archivos distribuido de control
description: Sistema de archivos distribuido de control DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d0a429bdb1e203d9b89f77e951d422cf3c0cef05cd5de5de39b537bb405f6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853535"
---
# <a name="distributed-file-system-control-codes"></a>Sistema de archivos distribuido de control

Estos son los códigos de Sistema de archivos distribuido (DFS):

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

El [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control puede obtener la misma información que la función [**NetDfsGetClientInfo,**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias elevadas a los servidores DFS. No se recomienda usar el código de control **FSCTL_DFS_GET_PKT_ENTRY_STATE** a menos que haya problemas de rendimiento.

Para realizar esta operación, llame a la [**función DeviceIoControl.**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)

</dd> </dl>