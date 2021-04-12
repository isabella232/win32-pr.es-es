---
title: Método IBackgroundCopyFile GetProgress (Deliveryoptimization. h)
description: Recupera información sobre el progreso de la transferencia de archivos.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Método GetProgress
- Método GetProgress, interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, método GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490265"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="72b25-106">IBackgroundCopyFile:: GetProgress (método)</span><span class="sxs-lookup"><span data-stu-id="72b25-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="72b25-107">Recupera información sobre el progreso de la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="72b25-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72b25-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="72b25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="72b25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b25-110">*pProgress* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="72b25-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72b25-111">Estructura cuyos miembros indican el progreso de la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="72b25-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="72b25-112">Para obtener más información sobre el tipo de información de progreso disponible, vea la estructura [**BG_FILE_PROGRESS**](bg-file-progress.md) .</span><span class="sxs-lookup"><span data-stu-id="72b25-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b25-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="72b25-113">Return value</span></span>

<span data-ttu-id="72b25-114">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="72b25-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b25-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b25-115">Requirements</span></span>



| <span data-ttu-id="72b25-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b25-116">Requirement</span></span> | <span data-ttu-id="72b25-117">Value</span><span class="sxs-lookup"><span data-stu-id="72b25-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b25-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72b25-118">Minimum supported client</span></span><br/> | <span data-ttu-id="72b25-119">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="72b25-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="72b25-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72b25-120">Minimum supported server</span></span><br/> | <span data-ttu-id="72b25-121">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="72b25-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="72b25-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72b25-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b25-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="72b25-124">IDL</span><span class="sxs-lookup"><span data-stu-id="72b25-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72b25-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="72b25-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72b25-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="72b25-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="72b25-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72b25-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b25-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72b25-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="72b25-130">IID</span><span class="sxs-lookup"><span data-stu-id="72b25-130">IID</span></span><br/>                      | <span data-ttu-id="72b25-131">IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="72b25-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="72b25-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="72b25-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b25-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="72b25-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="72b25-134">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="72b25-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="72b25-135">**IBackgroundCopyJob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="72b25-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





