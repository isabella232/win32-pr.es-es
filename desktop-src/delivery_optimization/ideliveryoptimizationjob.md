---
title: Interfaz IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Use la interfaz IDeliveryOptimizationJob para descargar intervalos de un archivo.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interfaz IDeliveryOptimizationJob
- Interfaz IDeliveryOptimizationJob, descrita
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150277"
---
# <a name="ideliveryoptimizationjob-interface"></a><span data-ttu-id="8a4cb-105">Interfaz IDeliveryOptimizationJob</span><span class="sxs-lookup"><span data-stu-id="8a4cb-105">IDeliveryOptimizationJob interface</span></span>

<span data-ttu-id="8a4cb-106">Use la interfaz **IDeliveryOptimizationJob** para descargar intervalos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="8a4cb-106">Use the **IDeliveryOptimizationJob** interface to download ranges of a file.</span></span>

## <a name="members"></a><span data-ttu-id="8a4cb-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a4cb-107">Members</span></span>

<span data-ttu-id="8a4cb-108">La interfaz **IDeliveryOptimizationJob** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8a4cb-108">The **IDeliveryOptimizationJob** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8a4cb-109">**IDeliveryOptimizationJob** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8a4cb-109">**IDeliveryOptimizationJob** also has these types of members:</span></span>

- [<span data-ttu-id="8a4cb-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a4cb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8a4cb-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8a4cb-111">Methods</span></span>

<span data-ttu-id="8a4cb-112">La interfaz **IDeliveryOptimizationJob** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="8a4cb-112">The **IDeliveryOptimizationJob** interface has these methods.</span></span>



| <span data-ttu-id="8a4cb-113">Método</span><span class="sxs-lookup"><span data-stu-id="8a4cb-113">Method</span></span>                                                                  | <span data-ttu-id="8a4cb-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a4cb-114">Description</span></span>                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a4cb-115">**AddFileWithRanges**</span><span class="sxs-lookup"><span data-stu-id="8a4cb-115">**AddFileWithRanges**</span></span>](ideliveryoptimizationjob-addfilewithranges.md) | <span data-ttu-id="8a4cb-116">Agrega un archivo a un trabajo de descarga y especifica los intervalos del archivo que desea descargar.</span><span class="sxs-lookup"><span data-stu-id="8a4cb-116">Adds a file to a download job and specifies the ranges of the file you want to download.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8a4cb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a4cb-117">Requirements</span></span>



| <span data-ttu-id="8a4cb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a4cb-118">Requirement</span></span> | <span data-ttu-id="8a4cb-119">Value</span><span class="sxs-lookup"><span data-stu-id="8a4cb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a4cb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a4cb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8a4cb-121">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a4cb-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8a4cb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a4cb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8a4cb-123">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="8a4cb-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8a4cb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a4cb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a4cb-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a4cb-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a4cb-126">IDL</span><span class="sxs-lookup"><span data-stu-id="8a4cb-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8a4cb-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8a4cb-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8a4cb-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8a4cb-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a4cb-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a4cb-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8a4cb-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a4cb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a4cb-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a4cb-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8a4cb-132">IID</span><span class="sxs-lookup"><span data-stu-id="8a4cb-132">IID</span></span><br/>                      | <span data-ttu-id="8a4cb-133">IID_IDeliveryOptimizationJob se define como EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="8a4cb-133">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span><br/>         |



 

