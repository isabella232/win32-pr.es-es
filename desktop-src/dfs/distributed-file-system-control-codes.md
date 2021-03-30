---
title: Códigos de control de Sistema de archivos distribuido
description: Sistema de archivos distribuido códigos de control DFS
ms.assetid: 1d9bebe6-f494-41e5-8a8d-51bf98eaa374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe054f87210c40da595dd731b263c485311729a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995385"
---
# <a name="distributed-file-system-control-codes"></a>Códigos de control de Sistema de archivos distribuido

A continuación se muestran los códigos de control Sistema de archivos distribuido (DFS):

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

El código de control de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) puede obtener la misma información que la función [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS. No se recomienda usar el código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** a menos que haya problemas de rendimiento.

Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

</dd> </dl>