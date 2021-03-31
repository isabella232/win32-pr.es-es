---
title: Interfaz IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Use la interfaz IBackgroundCopyFile2 para especificar un nuevo nombre remoto para el archivo y recuperar la lista de intervalos que se van a descargar.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interfaz IBackgroundCopyFile2
- Interfaz IBackgroundCopyFile2, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079284"
---
# <a name="ibackgroundcopyfile2-interface"></a><span data-ttu-id="2cf35-105">Interfaz IBackgroundCopyFile2</span><span class="sxs-lookup"><span data-stu-id="2cf35-105">IBackgroundCopyFile2 interface</span></span>

<span data-ttu-id="2cf35-106">Use la interfaz **IBackgroundCopyFile2** para especificar un nuevo nombre remoto para el archivo y recuperar la lista de intervalos que se van a descargar.</span><span class="sxs-lookup"><span data-stu-id="2cf35-106">Use the **IBackgroundCopyFile2** interface to specify a new remote name for the file and retrieve the list of ranges to download.</span></span>

<span data-ttu-id="2cf35-107">La interfaz **IBackgroundCopyFile2** hereda de la interfaz [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf35-107">The **IBackgroundCopyFile2** interface inherits from the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface.</span></span>

<span data-ttu-id="2cf35-108">Para obtener un puntero de interfaz **IBackgroundCopyFile2** , llame al método **IBackgroundCopyFile:: QueryInterface** mediante __uuidof (IBackgroundCopyFile2) para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="2cf35-108">To get an **IBackgroundCopyFile2** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile2) for the interface identifier.</span></span> <span data-ttu-id="2cf35-109">Use el puntero de la interfaz **IBackgroundCopyFile2** para llamar a los métodos [**IBackgroundCopyFile**](ibackgroundcopyfile.md) y **IBackgroundCopyFile2** .</span><span class="sxs-lookup"><span data-stu-id="2cf35-109">Use the **IBackgroundCopyFile2** interface pointer to call both the [**IBackgroundCopyFile**](ibackgroundcopyfile.md) and **IBackgroundCopyFile2** methods.</span></span>

## <a name="members"></a><span data-ttu-id="2cf35-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2cf35-110">Members</span></span>

<span data-ttu-id="2cf35-111">La interfaz **IBackgroundCopyFile2** hereda de [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span><span class="sxs-lookup"><span data-stu-id="2cf35-111">The **IBackgroundCopyFile2** interface inherits from [**IBackgroundCopyFile**](ibackgroundcopyfile.md).</span></span> <span data-ttu-id="2cf35-112">**IBackgroundCopyFile2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2cf35-112">**IBackgroundCopyFile2** also has these types of members:</span></span>

-   [<span data-ttu-id="2cf35-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="2cf35-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2cf35-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2cf35-114">Methods</span></span>

<span data-ttu-id="2cf35-115">La interfaz **IBackgroundCopyFile2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2cf35-115">The **IBackgroundCopyFile2** interface has these methods.</span></span>



| <span data-ttu-id="2cf35-116">Método</span><span class="sxs-lookup"><span data-stu-id="2cf35-116">Method</span></span>                                                             | <span data-ttu-id="2cf35-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cf35-117">Description</span></span>                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="2cf35-118">**GetFileRanges**</span><span class="sxs-lookup"><span data-stu-id="2cf35-118">**GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md) | <span data-ttu-id="2cf35-119">Recupera la matriz de intervalos que desea descargar de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="2cf35-119">Retrieves the array of ranges that you want to download from the URL.</span></span><br/> |
| [<span data-ttu-id="2cf35-120">**SetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="2cf35-120">**SetRemoteName**</span></span>](ibackgroundcopyfile2-setremotename-method.md) | <span data-ttu-id="2cf35-121">Cambia el nombre remoto a una nueva dirección URL.</span><span class="sxs-lookup"><span data-stu-id="2cf35-121">Changes the remote name to a new URL.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="2cf35-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cf35-122">Requirements</span></span>



| <span data-ttu-id="2cf35-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cf35-123">Requirement</span></span> | <span data-ttu-id="2cf35-124">Value</span><span class="sxs-lookup"><span data-stu-id="2cf35-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cf35-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf35-125">Minimum supported client</span></span><br/> | <span data-ttu-id="2cf35-126">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cf35-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2cf35-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cf35-127">Minimum supported server</span></span><br/> | <span data-ttu-id="2cf35-128">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="2cf35-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2cf35-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cf35-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cf35-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2cf35-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2cf35-131">IDL</span><span class="sxs-lookup"><span data-stu-id="2cf35-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2cf35-132"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2cf35-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2cf35-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2cf35-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="2cf35-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2cf35-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2cf35-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cf35-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cf35-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cf35-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2cf35-137">IID</span><span class="sxs-lookup"><span data-stu-id="2cf35-137">IID</span></span><br/>                      | <span data-ttu-id="2cf35-138">IID_IBackgroundCopyFile2 se define como 83E81B93-0873-474D-8A8C-F2018B1A939C</span><span class="sxs-lookup"><span data-stu-id="2cf35-138">IID_IBackgroundCopyFile2 is defined as 83E81B93-0873-474D-8A8C-F2018B1A939C</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2cf35-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cf35-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cf35-140">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="2cf35-140">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> </dl>

 

 





