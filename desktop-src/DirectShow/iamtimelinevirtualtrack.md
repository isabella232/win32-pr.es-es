---
description: La interfaz IAMTimelineVirtualTrack proporciona métodos para trabajar con pistas virtuales en los servicios de edición de DirectShow (DES). Las composiciones y las pistas admiten esta interfaz.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interfaz IAMTimelineVirtualTrack (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690321"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="faa50-104">Interfaz IAMTimelineVirtualTrack</span><span class="sxs-lookup"><span data-stu-id="faa50-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="faa50-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="faa50-105">\[Deprecated.</span></span> <span data-ttu-id="faa50-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="faa50-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="faa50-107">La `IAMTimelineVirtualTrack` interfaz proporciona métodos para trabajar con pistas virtuales en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="faa50-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="faa50-108">Las composiciones y las pistas admiten esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="faa50-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="faa50-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="faa50-109">Members</span></span>

<span data-ttu-id="faa50-110">La interfaz **IAMTimelineVirtualTrack** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="faa50-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="faa50-111">**IAMTimelineVirtualTrack** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="faa50-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="faa50-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="faa50-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="faa50-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="faa50-113">Methods</span></span>

<span data-ttu-id="faa50-114">La interfaz **IAMTimelineVirtualTrack** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="faa50-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="faa50-115">Método</span><span class="sxs-lookup"><span data-stu-id="faa50-115">Method</span></span>                                                               | <span data-ttu-id="faa50-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="faa50-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="faa50-117">**SetTrackDirty**</span><span class="sxs-lookup"><span data-stu-id="faa50-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="faa50-118">No se admite.</span><span class="sxs-lookup"><span data-stu-id="faa50-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="faa50-119">**TrackGetPriority**</span><span class="sxs-lookup"><span data-stu-id="faa50-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="faa50-120">Recupera el nivel de prioridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="faa50-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="faa50-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="faa50-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="faa50-122">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="faa50-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="faa50-123">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="faa50-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="faa50-124">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="faa50-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="faa50-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="faa50-125">Requirements</span></span>



| <span data-ttu-id="faa50-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="faa50-126">Requirement</span></span> | <span data-ttu-id="faa50-127">Value</span><span class="sxs-lookup"><span data-stu-id="faa50-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="faa50-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="faa50-128">Header</span></span><br/>  | <dl> <span data-ttu-id="faa50-129"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="faa50-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="faa50-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="faa50-130">Library</span></span><br/> | <dl> <span data-ttu-id="faa50-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="faa50-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
