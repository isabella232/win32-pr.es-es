---
title: Interfaz IDODownload
description: Se usa para iniciar y administrar una descarga.
keywords:
- Interfaz IDODownload
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359016"
---
# <a name="idodownload-interface"></a><span data-ttu-id="47eb1-104">Interfaz IDODownload</span><span class="sxs-lookup"><span data-stu-id="47eb1-104">IDODownload interface</span></span>

<span data-ttu-id="47eb1-105">La interfaz **IDODownload** se usa para iniciar y administrar una descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="47eb1-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="47eb1-106">Methods</span></span>

<span data-ttu-id="47eb1-107">La interfaz **IDODownload** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="47eb1-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="47eb1-108">Método</span><span class="sxs-lookup"><span data-stu-id="47eb1-108">Method</span></span> | <span data-ttu-id="47eb1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="47eb1-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="47eb1-110">IDODownload:: ABORT</span><span class="sxs-lookup"><span data-stu-id="47eb1-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="47eb1-111">Anula la descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-111">Aborts the download.</span></span> |
| [<span data-ttu-id="47eb1-112">IDODownload:: Finalize</span><span class="sxs-lookup"><span data-stu-id="47eb1-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="47eb1-113">Finaliza la descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="47eb1-114">IDODownload:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="47eb1-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="47eb1-115">Recupera un puntero a un **valor de tipo Variant** que contiene una propiedad de descarga específica.</span><span class="sxs-lookup"><span data-stu-id="47eb1-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="47eb1-116">IDODownload:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="47eb1-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="47eb1-117">Recupera un puntero a una estructura de **DO_DOWNLOAD_STATUS** que refleja el estado actual de la descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="47eb1-118">IDODownload::P ause</span><span class="sxs-lookup"><span data-stu-id="47eb1-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="47eb1-119">Pausa la descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-119">Pauses the download.</span></span> |
| [<span data-ttu-id="47eb1-120">IDODownload:: SetProperty</span><span class="sxs-lookup"><span data-stu-id="47eb1-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="47eb1-121">Establece una propiedad de descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-121">Sets a download property.</span></span> |
| [<span data-ttu-id="47eb1-122">IDODownload:: Start</span><span class="sxs-lookup"><span data-stu-id="47eb1-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="47eb1-123">Inicia o reanuda una descarga.</span><span class="sxs-lookup"><span data-stu-id="47eb1-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="47eb1-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47eb1-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="47eb1-125">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="47eb1-125">**Minimum supported client**</span></span> | <span data-ttu-id="47eb1-126">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="47eb1-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="47eb1-127">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="47eb1-127">**Minimum supported server**</span></span> | <span data-ttu-id="47eb1-128">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="47eb1-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="47eb1-129">**Header**</span><span class="sxs-lookup"><span data-stu-id="47eb1-129">**Header**</span></span> | <span data-ttu-id="47eb1-130">Do. h</span><span class="sxs-lookup"><span data-stu-id="47eb1-130">Do.h</span></span> |