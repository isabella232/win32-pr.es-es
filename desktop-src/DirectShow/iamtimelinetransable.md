---
description: La interfaz IAMTimelineTransable agrega transiciones a un objeto en los servicios de edición de DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interfaz IAMTimelineTransable (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690989"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="fdded-103">Interfaz IAMTimelineTransable</span><span class="sxs-lookup"><span data-stu-id="fdded-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="fdded-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="fdded-104">\[Deprecated.</span></span> <span data-ttu-id="fdded-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fdded-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fdded-106">La `IAMTimelineTransable` interfaz agrega transiciones a un objeto en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="fdded-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="fdded-107">Esta interfaz la expone cualquier objeto que puede tener transiciones aplicadas, incluidas las pistas, las composiciones y los grupos.</span><span class="sxs-lookup"><span data-stu-id="fdded-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="fdded-108">Un objeto que implementa esta interfaz puede tener cualquier número de transiciones, pero las transiciones no deben superponerse en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="fdded-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="fdded-109">Audio no admite transiciones.</span><span class="sxs-lookup"><span data-stu-id="fdded-109">Audio does not support transitions.</span></span> <span data-ttu-id="fdded-110">Los objetos dentro de los grupos de audio pueden exponer la `IAMTimelineTransable` interfaz, pero la aplicación no debe agregarles transiciones.</span><span class="sxs-lookup"><span data-stu-id="fdded-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="fdded-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fdded-111">Members</span></span>

<span data-ttu-id="fdded-112">La interfaz **IAMTimelineTransable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fdded-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="fdded-113">**IAMTimelineTransable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fdded-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="fdded-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="fdded-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fdded-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="fdded-115">Methods</span></span>

<span data-ttu-id="fdded-116">La interfaz **IAMTimelineTransable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fdded-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="fdded-117">Método</span><span class="sxs-lookup"><span data-stu-id="fdded-117">Method</span></span>                                                          | <span data-ttu-id="fdded-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdded-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdded-119">**GetNextTrans**</span><span class="sxs-lookup"><span data-stu-id="fdded-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="fdded-120">Recupera la primera transición que aparece en el momento especificado o posterior.</span><span class="sxs-lookup"><span data-stu-id="fdded-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="fdded-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="fdded-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="fdded-122">Recupera la primera transición que aparece en el momento especificado o posterior, con el tiempo dado como valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="fdded-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="fdded-123">**GetTransAtTime**</span><span class="sxs-lookup"><span data-stu-id="fdded-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="fdded-124">Recupera la transición más cercana a la hora especificada.</span><span class="sxs-lookup"><span data-stu-id="fdded-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="fdded-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="fdded-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="fdded-126">Recupera la transición más cercana al tiempo especificado, dado como un valor **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="fdded-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="fdded-127">**TransAdd**</span><span class="sxs-lookup"><span data-stu-id="fdded-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="fdded-128">Agrega una transición al objeto.</span><span class="sxs-lookup"><span data-stu-id="fdded-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="fdded-129">**TransGetCount**</span><span class="sxs-lookup"><span data-stu-id="fdded-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="fdded-130">Recupera el número de transiciones de este objeto.</span><span class="sxs-lookup"><span data-stu-id="fdded-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="fdded-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fdded-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fdded-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="fdded-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fdded-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="fdded-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fdded-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="fdded-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fdded-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fdded-135">Requirements</span></span>



| <span data-ttu-id="fdded-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdded-136">Requirement</span></span> | <span data-ttu-id="fdded-137">Value</span><span class="sxs-lookup"><span data-stu-id="fdded-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdded-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fdded-138">Header</span></span><br/>  | <dl> <span data-ttu-id="fdded-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdded-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fdded-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fdded-140">Library</span></span><br/> | <dl> <span data-ttu-id="fdded-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdded-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
