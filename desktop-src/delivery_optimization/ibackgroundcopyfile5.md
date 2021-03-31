---
title: Interfaz IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Use esta interfaz para obtener o establecer las propiedades genéricas de las transferencias de archivos de optimización de entrega (DO).
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150206"
---
# <a name="ibackgroundcopyfile5-interface"></a><span data-ttu-id="e1999-105">Interfaz IBackgroundCopyFile5</span><span class="sxs-lookup"><span data-stu-id="e1999-105">IBackgroundCopyFile5 interface</span></span>

<span data-ttu-id="e1999-106">Use esta interfaz para obtener o establecer las propiedades genéricas de las transferencias de archivos de optimización de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="e1999-106">Use this interface to get or set generic properties of Delivery Optimization (DO) file transfers.</span></span>

<span data-ttu-id="e1999-107">Para obtener un puntero de interfaz **IBackgroundCopyFile5** , llame al método **IBackgroundCopyFile:: QueryInterface** mediante __uuidof (IBackgroundCopyFile5) para el identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="e1999-107">To get an **IBackgroundCopyFile5** interface pointer, call the **IBackgroundCopyFile::QueryInterface** method using __uuidof(IBackgroundCopyFile5) for the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="e1999-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1999-108">Members</span></span>

<span data-ttu-id="e1999-109">La interfaz **IBackgroundCopyFile5** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e1999-109">The **IBackgroundCopyFile5** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e1999-110">**IBackgroundCopyFile5** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e1999-110">**IBackgroundCopyFile5** also has these types of members:</span></span>

-   [<span data-ttu-id="e1999-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1999-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e1999-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e1999-112">Methods</span></span>

<span data-ttu-id="e1999-113">La interfaz **IBackgroundCopyFile5** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e1999-113">The **IBackgroundCopyFile5** interface has these methods.</span></span>



| <span data-ttu-id="e1999-114">Método</span><span class="sxs-lookup"><span data-stu-id="e1999-114">Method</span></span>                                                  | <span data-ttu-id="e1999-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1999-115">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="e1999-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="e1999-116">**GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md) | <span data-ttu-id="e1999-117">Obtiene el valor de una propiedad BackgroundCopyFile genérica.</span><span class="sxs-lookup"><span data-stu-id="e1999-117">Gets the value of a generic BackgroundCopyFile property.</span></span><br/> |
| [<span data-ttu-id="e1999-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="e1999-118">**SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md) | <span data-ttu-id="e1999-119">Establece el valor de una propiedad BackgroundCopyFile genérica.</span><span class="sxs-lookup"><span data-stu-id="e1999-119">Sets the value of a generic BackgroundCopyFile property.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e1999-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1999-120">Requirements</span></span>



| <span data-ttu-id="e1999-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1999-121">Requirement</span></span> | <span data-ttu-id="e1999-122">Value</span><span class="sxs-lookup"><span data-stu-id="e1999-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1999-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1999-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e1999-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1999-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1999-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1999-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e1999-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="e1999-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e1999-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1999-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1999-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1999-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="e1999-129">IDL</span><span class="sxs-lookup"><span data-stu-id="e1999-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e1999-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e1999-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="e1999-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1999-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e1999-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1999-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="e1999-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1999-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1999-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1999-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="e1999-135">IID</span><span class="sxs-lookup"><span data-stu-id="e1999-135">IID</span></span><br/>                      | <span data-ttu-id="e1999-136">IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="e1999-136">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e1999-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1999-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1999-138">**IBackgroundCopyFile**</span><span class="sxs-lookup"><span data-stu-id="e1999-138">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="e1999-139">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="e1999-139">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

