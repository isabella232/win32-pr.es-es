---
title: Interfaz IDeliveryOptimizationJob2
description: 'Más información acerca de: interfaz IDeliveryOptimizationJob2'
keywords:
- Interfaz IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13f5a32b4ddccc203bcae7d6674c4713069355cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714851"
---
# <a name="ideliveryoptimizationjob2-interface"></a><span data-ttu-id="9cacc-104">Interfaz IDeliveryOptimizationJob2</span><span class="sxs-lookup"><span data-stu-id="9cacc-104">IDeliveryOptimizationJob2 interface</span></span>

<span data-ttu-id="9cacc-105">IDeliveryOptimizationJob2 permite agregar un solo archivo al trabajo de descarga y recuperar el archivo inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="9cacc-105">The IDeliveryOptimizationJob2 enables adding a single file to the download job, and retrieving the file immediately.</span></span> <span data-ttu-id="9cacc-106">Esta interfaz también admite la configuración y la obtención de propiedades de trabajo opcionales.</span><span class="sxs-lookup"><span data-stu-id="9cacc-106">This interface also supports setting and getting optional job properties.</span></span>

## <a name="members"></a><span data-ttu-id="9cacc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9cacc-107">Members</span></span>

<span data-ttu-id="9cacc-108">La interfaz **IDeliveryOptimizationJob2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9cacc-108">The **IDeliveryOptimizationJob2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9cacc-109">**IDeliveryOptimizationJob2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9cacc-109">**IDeliveryOptimizationJob2** also has these types of members:</span></span>

- [<span data-ttu-id="9cacc-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9cacc-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9cacc-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9cacc-111">Methods</span></span>

<span data-ttu-id="9cacc-112">La interfaz **IDeliveryOptimizationJob2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9cacc-112">The **IDeliveryOptimizationJob2** interface has these methods.</span></span>

| <span data-ttu-id="9cacc-113">Método</span><span class="sxs-lookup"><span data-stu-id="9cacc-113">Method</span></span>                                              | <span data-ttu-id="9cacc-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cacc-114">Description</span></span>                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="9cacc-115">**AddFile**</span><span class="sxs-lookup"><span data-stu-id="9cacc-115">**AddFile**</span></span>](ideliveryoptimizationjob2-addfile.md) | <span data-ttu-id="9cacc-116">El método AddFile agrega un solo archivo a un trabajo existente.</span><span class="sxs-lookup"><span data-stu-id="9cacc-116">The AddFile method adds a single file to an existing DO job.</span></span>         |
| [<span data-ttu-id="9cacc-117">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="9cacc-117">**GetProperty**</span></span>](ideliveryoptimizationjob2-getproperty.md) | <span data-ttu-id="9cacc-118">El método AddFile agrega un solo archivo a un trabajo existente.</span><span class="sxs-lookup"><span data-stu-id="9cacc-118">The AddFile method adds a single file to an existing DO job.</span></span> |
| [<span data-ttu-id="9cacc-119">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="9cacc-119">**SetProperty**</span></span>](ideliveryoptimizationjob2-setproperty.md) | <span data-ttu-id="9cacc-120">Este método no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9cacc-120">This method is unused.</span></span>                                       |

## <a name="requirements"></a><span data-ttu-id="9cacc-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cacc-121">Requirements</span></span>

| <span data-ttu-id="9cacc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cacc-122">Requirement</span></span> | <span data-ttu-id="9cacc-123">Value</span><span class="sxs-lookup"><span data-stu-id="9cacc-123">Value</span></span> |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9cacc-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cacc-124">Minimum supported client</span></span> | <span data-ttu-id="9cacc-125">Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="9cacc-125">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="9cacc-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cacc-126">Minimum supported server</span></span> | <span data-ttu-id="9cacc-127">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="9cacc-127">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="9cacc-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cacc-128">Header</span></span>                   | <span data-ttu-id="9cacc-129">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="9cacc-129">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="9cacc-130">IDL</span><span class="sxs-lookup"><span data-stu-id="9cacc-130">IDL</span></span>                      | <span data-ttu-id="9cacc-131">DeliveryOptimization. idl</span><span class="sxs-lookup"><span data-stu-id="9cacc-131">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="9cacc-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9cacc-132">Library</span></span>                  | <span data-ttu-id="9cacc-133">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="9cacc-133">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="9cacc-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cacc-134">DLL</span></span>                      | <span data-ttu-id="9cacc-135">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="9cacc-135">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="9cacc-136">IID</span><span class="sxs-lookup"><span data-stu-id="9cacc-136">IID</span></span>                      | <span data-ttu-id="9cacc-137">IID_IDeliveryOptimizationJob2 se define como 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span><span class="sxs-lookup"><span data-stu-id="9cacc-137">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |
