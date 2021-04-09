---
title: Interfaz IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 admite el establecimiento y la obtención de propiedades de archivo opcionales.
keywords:
- Interfaz IDeliveryOptimizationFile2
- Interfaz IDeliveryOptimizationFile2, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079141"
---
# <a name="ideliveryoptimizationfile2-interface"></a><span data-ttu-id="8dc91-105">Interfaz IDeliveryOptimizationFile2</span><span class="sxs-lookup"><span data-stu-id="8dc91-105">IDeliveryOptimizationFile2 interface</span></span>

<span data-ttu-id="8dc91-106">**IDeliveryOptimizationFile2** admite el establecimiento y la obtención de propiedades de archivo opcionales.</span><span class="sxs-lookup"><span data-stu-id="8dc91-106">The **IDeliveryOptimizationFile2** supports setting and getting optional file properties.</span></span> 

## <a name="members"></a><span data-ttu-id="8dc91-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8dc91-107">Members</span></span>

<span data-ttu-id="8dc91-108">La interfaz **IDeliveryOptimizationFile2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8dc91-108">The **IDeliveryOptimizationFile2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8dc91-109">**IDeliveryOptimizationFile2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8dc91-109">**IDeliveryOptimizationFile2** also has these types of members:</span></span>

- [<span data-ttu-id="8dc91-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8dc91-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8dc91-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8dc91-111">Methods</span></span>

<span data-ttu-id="8dc91-112">La interfaz **IDeliveryOptimizationFile2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8dc91-112">The **IDeliveryOptimizationFile2** interface has these methods.</span></span>

| <span data-ttu-id="8dc91-113">Método</span><span class="sxs-lookup"><span data-stu-id="8dc91-113">Method</span></span>                                                 | <span data-ttu-id="8dc91-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8dc91-114">Description</span></span>                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="8dc91-115">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="8dc91-115">**GetProperty**</span></span>](ideliveryoptimizationfile2-getproperty.md)  | <span data-ttu-id="8dc91-116">Este método devuelve una única propiedad del archivo DO.</span><span class="sxs-lookup"><span data-stu-id="8dc91-116">This method returns a single property of the DO file.</span></span> |
| [<span data-ttu-id="8dc91-117">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="8dc91-117">**SetProperty**</span></span>](ideliveryoptimizationfile2-setproperty.md)  | <span data-ttu-id="8dc91-118">Este método establece una propiedad única del archivo DO.</span><span class="sxs-lookup"><span data-stu-id="8dc91-118">This method sets a single property of the DO file.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="8dc91-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8dc91-119">Requirements</span></span>

| <span data-ttu-id="8dc91-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8dc91-120">Requirement</span></span> | <span data-ttu-id="8dc91-121">Value</span><span class="sxs-lookup"><span data-stu-id="8dc91-121">Value</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8dc91-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dc91-122">Minimum supported client</span></span>      | <span data-ttu-id="8dc91-123">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="8dc91-123">Windows 10, version 1803 \[desktop apps only\]</span></span>                                    |
| <span data-ttu-id="8dc91-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8dc91-124">Minimum supported server</span></span>      | <span data-ttu-id="8dc91-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="8dc91-125">Windows Server, version 1709 \[desktop apps only\]</span></span>                                |
| <span data-ttu-id="8dc91-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8dc91-126">Header</span></span>                        | <span data-ttu-id="8dc91-127">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="8dc91-127">Deliveryoptimization.h</span></span>                                                            |
| <span data-ttu-id="8dc91-128">IDL</span><span class="sxs-lookup"><span data-stu-id="8dc91-128">IDL</span></span>                           | <span data-ttu-id="8dc91-129">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="8dc91-129">DeliveryOptimization.idl</span></span>                                                          |
| <span data-ttu-id="8dc91-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8dc91-130">Library</span></span>                       | <span data-ttu-id="8dc91-131">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="8dc91-131">Dosvc.lib</span></span>                                                                         |
| <span data-ttu-id="8dc91-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8dc91-132">DLL</span></span>                           | <span data-ttu-id="8dc91-133">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="8dc91-133">Dosvc.dll</span></span>                                                                         |
| <span data-ttu-id="8dc91-134">IID</span><span class="sxs-lookup"><span data-stu-id="8dc91-134">IID</span></span>                           | <span data-ttu-id="8dc91-135">IID_IDeliveryOptimizationFile2 se define como 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span><span class="sxs-lookup"><span data-stu-id="8dc91-135">IID_IDeliveryOptimizationFile2 is defined as 3A87296F-6EC2-4126-AB29-E3F8DC4CC390</span></span> |
