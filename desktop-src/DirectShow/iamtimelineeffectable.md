---
description: La interfaz IAMTimelineEffectable proporciona métodos para agregar efectos a un objeto Timeline en los servicios de edición de DirectShow (DES) y para manipular los efectos en un objeto.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interfaz IAMTimelineEffectable (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680194"
---
# <a name="iamtimelineeffectable-interface"></a><span data-ttu-id="dcf3a-103">Interfaz IAMTimelineEffectable</span><span class="sxs-lookup"><span data-stu-id="dcf3a-103">IAMTimelineEffectable interface</span></span>

> [!Note]  
> <span data-ttu-id="dcf3a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-104">\[Deprecated.</span></span> <span data-ttu-id="dcf3a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dcf3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dcf3a-106">La `IAMTimelineEffectable` interfaz proporciona métodos para agregar efectos a un objeto Timeline en los [servicios de edición de DirectShow](directshow-editing-services.md) (des) y para manipular los efectos en un objeto.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-106">The `IAMTimelineEffectable` interface provides methods for adding effects to a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES), and for manipulating the effects on an object.</span></span> <span data-ttu-id="dcf3a-107">Todos los objetos que pueden tener efectos aplicados a ellos implementan esta interfaz; Esto incluye orígenes, pistas y composiciones.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-107">All objects that can have effects applied to them implement this interface; this includes sources, tracks, and compositions.</span></span>

<span data-ttu-id="dcf3a-108">Un objeto que implementa esta interfaz puede tener cualquier número de efectos.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-108">An object that implements this interface can have any number of effects.</span></span> <span data-ttu-id="dcf3a-109">Para cada objeto, el motor de representación aplica sus efectos en orden de prioridad, empezando por el nivel de prioridad 0.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-109">For each object, the render engine applies its effects in order of priority, starting with priority level 0.</span></span>

## <a name="members"></a><span data-ttu-id="dcf3a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="dcf3a-110">Members</span></span>

<span data-ttu-id="dcf3a-111">La interfaz **IAMTimelineEffectable** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dcf3a-111">The **IAMTimelineEffectable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dcf3a-112">**IAMTimelineEffectable** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dcf3a-112">**IAMTimelineEffectable** also has these types of members:</span></span>

-   [<span data-ttu-id="dcf3a-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dcf3a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dcf3a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="dcf3a-114">Methods</span></span>

<span data-ttu-id="dcf3a-115">La interfaz **IAMTimelineEffectable** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-115">The **IAMTimelineEffectable** interface has these methods.</span></span>



| <span data-ttu-id="dcf3a-116">Método</span><span class="sxs-lookup"><span data-stu-id="dcf3a-116">Method</span></span>                                                                     | <span data-ttu-id="dcf3a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf3a-117">Description</span></span>                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="dcf3a-118">**EffectGetCount**</span><span class="sxs-lookup"><span data-stu-id="dcf3a-118">**EffectGetCount**</span></span>](iamtimelineeffectable-effectgetcount.md)             | <span data-ttu-id="dcf3a-119">Recupera el número de efectos de este objeto.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-119">Retrieves the number of effects on this object.</span></span><br/>                    |
| [<span data-ttu-id="dcf3a-120">**EffectInsBefore**</span><span class="sxs-lookup"><span data-stu-id="dcf3a-120">**EffectInsBefore**</span></span>](iamtimelineeffectable-effectinsbefore.md)           | <span data-ttu-id="dcf3a-121">Inserta un efecto en el objeto en el nivel de prioridad especificado.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-121">Inserts an effect into the object at the specified priority level.</span></span><br/> |
| [<span data-ttu-id="dcf3a-122">**EffectSwapPriorities**</span><span class="sxs-lookup"><span data-stu-id="dcf3a-122">**EffectSwapPriorities**</span></span>](iamtimelineeffectable-effectswappriorities.md) | <span data-ttu-id="dcf3a-123">Cambia los niveles de prioridad de dos efectos.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-123">Switches the priority levels of two effects.</span></span><br/>                       |
| [<span data-ttu-id="dcf3a-124">**GetEffect**</span><span class="sxs-lookup"><span data-stu-id="dcf3a-124">**GetEffect**</span></span>](iamtimelineeffectable-geteffect.md)                       | <span data-ttu-id="dcf3a-125">Recupera el efecto en el nivel de prioridad especificado.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-125">Retrieves the effect at the specified priority level.</span></span><br/>              |



 

## <a name="remarks"></a><span data-ttu-id="dcf3a-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcf3a-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dcf3a-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcf3a-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dcf3a-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dcf3a-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dcf3a-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcf3a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf3a-130">Requirements</span></span>



| <span data-ttu-id="dcf3a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf3a-131">Requirement</span></span> | <span data-ttu-id="dcf3a-132">Value</span><span class="sxs-lookup"><span data-stu-id="dcf3a-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf3a-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcf3a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf3a-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf3a-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dcf3a-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcf3a-135">Library</span></span><br/> | <dl> <span data-ttu-id="dcf3a-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf3a-136"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
