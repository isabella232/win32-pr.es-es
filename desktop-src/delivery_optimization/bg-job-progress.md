---
title: BG_JOB_PROGRESS estructura (Deliveryoptimization. h)
description: La estructura BG_JOB_PROGRESS proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos. En el caso de los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.
ms.assetid: F07BBDDE-FD34-4779-9E17-3789A8098616
keywords:
- Estructura de BG_JOB_PROGRESS
topic_type:
- apiref
api_name:
- BG_JOB_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e45c4a2833f80644ff763fc85a6846f9858fb3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534935"
---
# <a name="bg_job_progress-structure"></a><span data-ttu-id="fa097-105">Estructura de BG_JOB_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="fa097-105">BG_JOB_PROGRESS structure</span></span>

<span data-ttu-id="fa097-106">La estructura **BG_JOB_PROGRESS** proporciona información de progreso relacionada con el trabajo, como el número de bytes y archivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="fa097-106">The **BG_JOB_PROGRESS** structure provides job-related progress information, such as the number of bytes and files transferred.</span></span> <span data-ttu-id="fa097-107">En el caso de los trabajos de carga, el progreso se aplica al archivo de carga, no al archivo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="fa097-107">For upload jobs, the progress applies to the upload file, not the reply file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa097-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fa097-108">Syntax</span></span>


```C++
typedef struct _BG_JOB_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  ULONG  FilesTotal;
  ULONG  FilesTransferred;
} BG_JOB_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="fa097-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fa097-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="fa097-110">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="fa097-110">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="fa097-111">Número total de bytes que se van a transferir para todos los archivos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="fa097-111">Total number of bytes to transfer for all files in the job.</span></span> <span data-ttu-id="fa097-112">Si el valor es BG_SIZE_UNKNOWN, no se ha determinado el tamaño total de todos los archivos del trabajo.</span><span class="sxs-lookup"><span data-stu-id="fa097-112">If the value is BG_SIZE_UNKNOWN, the total size of all files in the job has not been determined.</span></span> <span data-ttu-id="fa097-113">No establezca este valor si no puede determinar el tamaño de uno de los archivos.</span><span class="sxs-lookup"><span data-stu-id="fa097-113">DO does not set this value if it cannot determine the size of one of the files.</span></span> <span data-ttu-id="fa097-114">Por ejemplo, si el archivo o el servidor especificado no existe, no puede determinar el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="fa097-114">For example, if the specified file or server does not exist, DO cannot determine the size of the file.</span></span>

<span data-ttu-id="fa097-115">Si va a descargar intervalos del archivo, **bytesTotal** incluye el número total de bytes que desea descargar del archivo.</span><span class="sxs-lookup"><span data-stu-id="fa097-115">If you are downloading ranges from the file, **BytesTotal** includes the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="fa097-116">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="fa097-116">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="fa097-117">Número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="fa097-117">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="fa097-118">**FilesTotal**</span><span class="sxs-lookup"><span data-stu-id="fa097-118">**FilesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="fa097-119">Número total de archivos que se van a transferir para este trabajo.</span><span class="sxs-lookup"><span data-stu-id="fa097-119">Total number of files to transfer for this job.</span></span>

</dd> <dt>

<span data-ttu-id="fa097-120">**FilesTransferred**</span><span class="sxs-lookup"><span data-stu-id="fa097-120">**FilesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="fa097-121">Número de archivos transferidos.</span><span class="sxs-lookup"><span data-stu-id="fa097-121">Number of files transferred.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa097-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa097-122">Requirements</span></span>



| <span data-ttu-id="fa097-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa097-123">Requirement</span></span> | <span data-ttu-id="fa097-124">Value</span><span class="sxs-lookup"><span data-stu-id="fa097-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa097-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa097-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fa097-126">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="fa097-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="fa097-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fa097-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fa097-128">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="fa097-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fa097-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fa097-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa097-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa097-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa097-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="fa097-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa097-132">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="fa097-132">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="fa097-133">**IBackgroundCopyJob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="fa097-133">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





