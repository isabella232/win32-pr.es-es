---
title: Interfaz IDODownloadStatusCallback
description: Se usa para recibir notificaciones sobre una descarga.
keywords:
- Interfaz IDODownloadStatusCallback
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420767"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="85e2b-104">Interfaz IDODownloadStatusCallback</span><span class="sxs-lookup"><span data-stu-id="85e2b-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="85e2b-105">La interfaz **IDODownloadStatusCallback** se usa para recibir notificaciones sobre una descarga.</span><span class="sxs-lookup"><span data-stu-id="85e2b-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="85e2b-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="85e2b-106">Methods</span></span>

<span data-ttu-id="85e2b-107">La interfaz **IDODownloadStatusCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="85e2b-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="85e2b-108">Método</span><span class="sxs-lookup"><span data-stu-id="85e2b-108">Method</span></span> | <span data-ttu-id="85e2b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="85e2b-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="85e2b-110">IDODownloadStatusCallback::OnStatusChanged</span><span class="sxs-lookup"><span data-stu-id="85e2b-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="85e2b-111">Llama a la implementación de este método cada vez que cambia el estado de la descarga.</span><span class="sxs-lookup"><span data-stu-id="85e2b-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="85e2b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85e2b-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="85e2b-113">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="85e2b-113">**Minimum supported client**</span></span> | <span data-ttu-id="85e2b-114">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="85e2b-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="85e2b-115">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="85e2b-115">**Minimum supported server**</span></span> | <span data-ttu-id="85e2b-116">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="85e2b-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="85e2b-117">**Header**</span><span class="sxs-lookup"><span data-stu-id="85e2b-117">**Header**</span></span> | <span data-ttu-id="85e2b-118">Do. h</span><span class="sxs-lookup"><span data-stu-id="85e2b-118">Do.h</span></span> |