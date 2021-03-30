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
# <a name="distributed-file-system-control-codes"></a><span data-ttu-id="9b93e-103">Códigos de control de Sistema de archivos distribuido</span><span class="sxs-lookup"><span data-stu-id="9b93e-103">Distributed File System Control Codes</span></span>

<span data-ttu-id="9b93e-104">A continuación se muestran los códigos de control Sistema de archivos distribuido (DFS):</span><span class="sxs-lookup"><span data-stu-id="9b93e-104">The following are the Distributed File System (DFS) control codes:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b93e-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="9b93e-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9b93e-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span><span class="sxs-lookup"><span data-stu-id="9b93e-106">**FSCTL_DFS_GET_PKT_ENTRY_STATE**</span></span>](fsctl-dfs-get-pkt-entry-state.md)
</dt> <dd>

<span data-ttu-id="9b93e-107">El código de control de [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) puede obtener la misma información que la función [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) , pero puede proporcionar un mejor rendimiento en algunas configuraciones con latencias altas a los servidores DFS.</span><span class="sxs-lookup"><span data-stu-id="9b93e-107">The [**FSCTL_DFS_GET_PKT_ENTRY_STATE**](fsctl-dfs-get-pkt-entry-state.md) control code can get the same information as the [**NetDfsGetClientInfo**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetclientinfo) function but can provide better performance in some configurations with high latencies to the DFS servers.</span></span> <span data-ttu-id="9b93e-108">No se recomienda usar el código de control de **FSCTL_DFS_GET_PKT_ENTRY_STATE** a menos que haya problemas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9b93e-108">It is not recommended to use the **FSCTL_DFS_GET_PKT_ENTRY_STATE** control code unless there are performance issues.</span></span>

<span data-ttu-id="9b93e-109">Para realizar esta operación, llame a la función [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="9b93e-109">To perform this operation, call the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span>

</dd> </dl>