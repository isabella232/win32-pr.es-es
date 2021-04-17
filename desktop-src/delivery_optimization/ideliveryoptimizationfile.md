---
title: Interfaz IDeliveryOptimizationFile
description: Implemente la interfaz IDeliveryOptimizationFile para identificar el estado de un archivo específico.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interfaz IDeliveryOptimizationFile
- Interfaz IDeliveryOptimizationFile, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714569"
---
# <a name="ideliveryoptimizationfile-interface"></a><span data-ttu-id="3f7ae-105">Interfaz IDeliveryOptimizationFile</span><span class="sxs-lookup"><span data-stu-id="3f7ae-105">IDeliveryOptimizationFile interface</span></span>

<span data-ttu-id="3f7ae-106">Implemente la interfaz **IDeliveryOptimizationFile** para identificar el estado de un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-106">Implement the **IDeliveryOptimizationFile** interface to identify the status of a specific file.</span></span>

## <a name="members"></a><span data-ttu-id="3f7ae-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3f7ae-107">Members</span></span>

<span data-ttu-id="3f7ae-108">La interfaz **IDeliveryOptimizationFile** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3f7ae-108">The **IDeliveryOptimizationFile** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3f7ae-109">**IDeliveryOptimizationFile** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3f7ae-109">**IDeliveryOptimizationFile** also has these types of members:</span></span>

-   [<span data-ttu-id="3f7ae-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f7ae-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3f7ae-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3f7ae-111">Methods</span></span>

<span data-ttu-id="3f7ae-112">La interfaz **IDeliveryOptimizationFile** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-112">The **IDeliveryOptimizationFile** interface has these methods.</span></span>



| <span data-ttu-id="3f7ae-113">Método</span><span class="sxs-lookup"><span data-stu-id="3f7ae-113">Method</span></span>                                                 | <span data-ttu-id="3f7ae-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f7ae-114">Description</span></span>                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="3f7ae-115">**Getstats (**</span><span class="sxs-lookup"><span data-stu-id="3f7ae-115">**GetStats**</span></span>](ideliveryoptimizationfile-getstats.md) | <span data-ttu-id="3f7ae-116">Devuelve las estadísticas de descarga y carga de un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="3f7ae-116">Returns download and upload stats for a specific file.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="3f7ae-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f7ae-117">Requirements</span></span>

| <span data-ttu-id="3f7ae-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f7ae-118">Requirement</span></span> | <span data-ttu-id="3f7ae-119">Value</span><span class="sxs-lookup"><span data-stu-id="3f7ae-119">Value</span></span> |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3f7ae-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f7ae-120">Minimum supported client</span></span>      | <span data-ttu-id="3f7ae-121">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f7ae-121">Windows 10, version 1709 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="3f7ae-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f7ae-122">Minimum supported server</span></span>      | <span data-ttu-id="3f7ae-123">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3f7ae-123">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="3f7ae-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f7ae-124">Header</span></span>                        | <span data-ttu-id="3f7ae-125">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="3f7ae-125">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="3f7ae-126">IDL</span><span class="sxs-lookup"><span data-stu-id="3f7ae-126">IDL</span></span>                           | <span data-ttu-id="3f7ae-127">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="3f7ae-127">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="3f7ae-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3f7ae-128">Library</span></span>                       | <span data-ttu-id="3f7ae-129">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="3f7ae-129">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="3f7ae-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f7ae-130">DLL</span></span>                           | <span data-ttu-id="3f7ae-131">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="3f7ae-131">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="3f7ae-132">IID</span><span class="sxs-lookup"><span data-stu-id="3f7ae-132">IID</span></span>                           | <span data-ttu-id="3f7ae-133">IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="3f7ae-133">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span> |
