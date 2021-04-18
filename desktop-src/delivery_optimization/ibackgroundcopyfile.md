---
title: Interfaz IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contiene información acerca de un archivo que forma parte de un trabajo. Por ejemplo, puede usar métodos IBackgroundCopyFile para recuperar los nombres locales y remotos del archivo y transferir la información de progreso.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interfaz IBackgroundCopyFile
- Interfaz IBackgroundCopyFile, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705133"
---
# <a name="ibackgroundcopyfile-interface"></a><span data-ttu-id="80e29-106">Interfaz IBackgroundCopyFile</span><span class="sxs-lookup"><span data-stu-id="80e29-106">IBackgroundCopyFile interface</span></span>

<span data-ttu-id="80e29-107">**IBackgroundCopyFile** contiene información acerca de un archivo que forma parte de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="80e29-107">**IBackgroundCopyFile** contains information about a file that is part of a job.</span></span> <span data-ttu-id="80e29-108">Por ejemplo, puede usar métodos **IBackgroundCopyFile** para recuperar los nombres locales y remotos del archivo y transferir la información de progreso.</span><span class="sxs-lookup"><span data-stu-id="80e29-108">For example, you can use **IBackgroundCopyFile** methods to retrieve the local and remote names of the file and transfer progress information.</span></span>

<span data-ttu-id="80e29-109">Para obtener un puntero de interfaz **IBackgroundCopyFile** , llame al método [**IBackgroundCopyError:: GetFile**](ibackgroundcopyerror-getfile-method.md) o al método [**IEnumBackgroundCopyFiles:: Next**](ienumbackgroundcopyfiles-next.md) .</span><span class="sxs-lookup"><span data-stu-id="80e29-109">To get an **IBackgroundCopyFile** interface pointer, call the [**IBackgroundCopyError::GetFile**](ibackgroundcopyerror-getfile-method.md) method or the [**IEnumBackgroundCopyFiles::Next**](ienumbackgroundcopyfiles-next.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="80e29-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="80e29-110">Members</span></span>

<span data-ttu-id="80e29-111">La interfaz **IBackgroundCopyFile** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80e29-111">The **IBackgroundCopyFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80e29-112">**IBackgroundCopyFile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80e29-112">**IBackgroundCopyFile** also has these types of members:</span></span>

-   [<span data-ttu-id="80e29-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="80e29-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="80e29-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="80e29-114">Methods</span></span>

<span data-ttu-id="80e29-115">La interfaz **IBackgroundCopyFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="80e29-115">The **IBackgroundCopyFile** interface has these methods.</span></span>



| <span data-ttu-id="80e29-116">Método</span><span class="sxs-lookup"><span data-stu-id="80e29-116">Method</span></span>                                                            | <span data-ttu-id="80e29-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="80e29-117">Description</span></span>                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [<span data-ttu-id="80e29-118">**GetLocalName**</span><span class="sxs-lookup"><span data-stu-id="80e29-118">**GetLocalName**</span></span>](ibackgroundcopyfile-getlocalname-method.md)   | <span data-ttu-id="80e29-119">Recupera el nombre local del archivo.</span><span class="sxs-lookup"><span data-stu-id="80e29-119">Retrieves the local name of the file.</span></span><br/>        |
| [<span data-ttu-id="80e29-120">**GetProgress**</span><span class="sxs-lookup"><span data-stu-id="80e29-120">**GetProgress**</span></span>](ibackgroundcopyfile-getprogress-method.md)     | <span data-ttu-id="80e29-121">Recupera el progreso de la transferencia de archivos.</span><span class="sxs-lookup"><span data-stu-id="80e29-121">Retrieves the progress of the file transfer.</span></span><br/> |
| [<span data-ttu-id="80e29-122">**GetRemoteName**</span><span class="sxs-lookup"><span data-stu-id="80e29-122">**GetRemoteName**</span></span>](ibackgroundcopyfile-getremotename-method.md) | <span data-ttu-id="80e29-123">Recupera el nombre remoto del archivo.</span><span class="sxs-lookup"><span data-stu-id="80e29-123">Retrieves the remote name of the file.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="80e29-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80e29-124">Requirements</span></span>



| <span data-ttu-id="80e29-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="80e29-125">Requirement</span></span> | <span data-ttu-id="80e29-126">Value</span><span class="sxs-lookup"><span data-stu-id="80e29-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80e29-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80e29-127">Minimum supported client</span></span><br/> | <span data-ttu-id="80e29-128">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="80e29-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80e29-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80e29-129">Minimum supported server</span></span><br/> | <span data-ttu-id="80e29-130">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="80e29-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="80e29-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80e29-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="80e29-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="80e29-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="80e29-133">IDL</span><span class="sxs-lookup"><span data-stu-id="80e29-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80e29-134"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80e29-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="80e29-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80e29-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="80e29-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80e29-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="80e29-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80e29-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80e29-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80e29-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="80e29-139">IID</span><span class="sxs-lookup"><span data-stu-id="80e29-139">IID</span></span><br/>                      | <span data-ttu-id="80e29-140">IID_IBackgroundCopyFile se define como 01B7BD23-FB88-4A77-8490-5891D3E4653A</span><span class="sxs-lookup"><span data-stu-id="80e29-140">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="80e29-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="80e29-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80e29-142">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="80e29-142">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="80e29-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="80e29-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> <dt>

[<span data-ttu-id="80e29-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="80e29-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="80e29-145">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="80e29-145">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

