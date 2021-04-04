---
title: BG_FILE_PROGRESS estructura (Deliveryoptimization. h)
description: La estructura BG_FILE_PROGRESS proporciona información de progreso relacionada con archivos, como el número de bytes transferidos.
ms.assetid: 49BDFEEE-D7BF-489A-8BC1-951549B06252
keywords:
- Estructura de BG_FILE_PROGRESS
topic_type:
- apiref
api_name:
- BG_FILE_PROGRESS
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93507b8aeefa9c0ea16f70f67e221ecc4218427f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803301"
---
# <a name="bg_file_progress-structure"></a><span data-ttu-id="bddbf-104">Estructura de BG_FILE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="bddbf-104">BG_FILE_PROGRESS structure</span></span>

<span data-ttu-id="bddbf-105">La estructura **BG_FILE_PROGRESS** proporciona información de progreso relacionada con archivos, como el número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="bddbf-105">The **BG_FILE_PROGRESS** structure provides file-related progress information, such as the number of bytes transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="bddbf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bddbf-106">Syntax</span></span>


```C++
typedef struct _BG_FILE_PROGRESS {
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  BOOL   Completed;
} BG_FILE_PROGRESS;
```



## <a name="members"></a><span data-ttu-id="bddbf-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bddbf-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bddbf-108">**BytesTotal**</span><span class="sxs-lookup"><span data-stu-id="bddbf-108">**BytesTotal**</span></span>
</dt> <dd>

<span data-ttu-id="bddbf-109">Tamaño del archivo en bytes.</span><span class="sxs-lookup"><span data-stu-id="bddbf-109">Size of the file in bytes.</span></span> <span data-ttu-id="bddbf-110">Si no puede determinar el tamaño del archivo (por ejemplo, si el archivo o el servidor no existen), el valor es DO_UNKNOWN_FILE_SIZE.</span><span class="sxs-lookup"><span data-stu-id="bddbf-110">If DO cannot determine the size of the file (for example, if the file or server does not exist), the value is DO_UNKNOWN_FILE_SIZE.</span></span>

<span data-ttu-id="bddbf-111">Si va a descargar intervalos de un archivo, **bytesTotal** refleja el número total de bytes que desea descargar del archivo.</span><span class="sxs-lookup"><span data-stu-id="bddbf-111">If you are downloading ranges from a file, **BytesTotal** reflects the total number of bytes you want to download from the file.</span></span>

</dd> <dt>

<span data-ttu-id="bddbf-112">**BytesTransferred**</span><span class="sxs-lookup"><span data-stu-id="bddbf-112">**BytesTransferred**</span></span>
</dt> <dd>

<span data-ttu-id="bddbf-113">Número de bytes transferidos.</span><span class="sxs-lookup"><span data-stu-id="bddbf-113">Number of bytes transferred.</span></span>

</dd> <dt>

<span data-ttu-id="bddbf-114">**Completado**</span><span class="sxs-lookup"><span data-stu-id="bddbf-114">**Completed**</span></span>
</dt> <dd>

<span data-ttu-id="bddbf-115">En el caso de las descargas, el valor es **true** si el archivo está disponible para el usuario; de lo contrario, el valor es **false**.</span><span class="sxs-lookup"><span data-stu-id="bddbf-115">For downloads, the value is **TRUE** if the file is available to the user; otherwise, the value is **FALSE**.</span></span> <span data-ttu-id="bddbf-116">Los archivos están disponibles para el usuario después de llamar al método [**IBackgroundCopyJob:: Complete**](ibackgroundcopyjob-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="bddbf-116">Files are available to the user after calling the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="bddbf-117">Si el método **Complete** genera un error transitorio, los archivos procesados antes de que se produjera el error están disponibles para el usuario; los demás no lo son.</span><span class="sxs-lookup"><span data-stu-id="bddbf-117">If the **Complete** method generates a transient error, those files processed before the error occurred are available to the user; the others are not.</span></span> <span data-ttu-id="bddbf-118">Use el miembro **completado** para determinar si el archivo está disponible para el usuario cuando se produce un error de **finalización** .</span><span class="sxs-lookup"><span data-stu-id="bddbf-118">Use the **Completed** member to determine if the file is available to the user when **Complete** fails.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bddbf-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bddbf-119">Remarks</span></span>

<span data-ttu-id="bddbf-120">Para determinar si transfirió el archivo, puede:</span><span class="sxs-lookup"><span data-stu-id="bddbf-120">To determine if DO transferred the file, you can:</span></span>

-   <span data-ttu-id="bddbf-121">Compare **BytesTransferred** con **bytesTotal**.</span><span class="sxs-lookup"><span data-stu-id="bddbf-121">Compare **BytesTransferred** to **BytesTotal**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bddbf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bddbf-122">Requirements</span></span>



| <span data-ttu-id="bddbf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bddbf-123">Requirement</span></span> | <span data-ttu-id="bddbf-124">Value</span><span class="sxs-lookup"><span data-stu-id="bddbf-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bddbf-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bddbf-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bddbf-126">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="bddbf-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bddbf-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bddbf-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bddbf-128">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="bddbf-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bddbf-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bddbf-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bddbf-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="bddbf-130"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bddbf-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="bddbf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bddbf-132">**BG_JOB_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="bddbf-132">**BG_JOB_PROGRESS**</span></span>](bg-job-progress.md)
</dt> <dt>

[<span data-ttu-id="bddbf-133">**IBackgroundCopyFile:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="bddbf-133">**IBackgroundCopyFile::GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)
</dt> </dl>

 

 





