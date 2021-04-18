---
description: El método AddGroup agrega un grupo a la escala de tiempo.
ms.assetid: c7fc3b59-5852-4a3c-b9bf-f87e659819b5
title: 'IAMTimeline:: AddGroup (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.AddGroup
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0de10defd5e7aa840322599fb32104f1dc5bb5a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679387"
---
# <a name="iamtimelineaddgroup-method"></a><span data-ttu-id="e473c-103">IAMTimeline:: AddGroup (método)</span><span class="sxs-lookup"><span data-stu-id="e473c-103">IAMTimeline::AddGroup method</span></span>

> [!Note]  
> <span data-ttu-id="e473c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e473c-104">\[Deprecated.</span></span> <span data-ttu-id="e473c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e473c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e473c-106">El `AddGroup` método agrega un grupo a la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e473c-106">The `AddGroup` method adds a group to the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="e473c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e473c-107">Syntax</span></span>


```C++
HRESULT AddGroup(
   IAMTimelineObj *pGroup
);
```



## <a name="parameters"></a><span data-ttu-id="e473c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e473c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e473c-109">*pGroup*</span><span class="sxs-lookup"><span data-stu-id="e473c-109">*pGroup*</span></span> 
</dt> <dd>

<span data-ttu-id="e473c-110">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del grupo.</span><span class="sxs-lookup"><span data-stu-id="e473c-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e473c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e473c-111">Return value</span></span>

<span data-ttu-id="e473c-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e473c-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e473c-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e473c-113">Return code</span></span>                                                                                   | <span data-ttu-id="e473c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e473c-114">Description</span></span>                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="e473c-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e473c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e473c-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e473c-116">Success.</span></span><br/>                           |
| <dl> <span data-ttu-id="e473c-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e473c-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e473c-118">Se ha superado el número máximo de grupos.</span><span class="sxs-lookup"><span data-stu-id="e473c-118">Maximum number of groups exceeded.</span></span><br/> |
| <dl> <span data-ttu-id="e473c-119"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="e473c-119"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="e473c-120">El objeto no es un grupo.</span><span class="sxs-lookup"><span data-stu-id="e473c-120">The object is not a group.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="e473c-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e473c-121">Remarks</span></span>

<span data-ttu-id="e473c-122">Actualmente, las escalas de tiempo admiten un máximo de 32 grupos.</span><span class="sxs-lookup"><span data-stu-id="e473c-122">Currently, timelines support a maximum of 32 groups.</span></span>

> [!Note]  
> <span data-ttu-id="e473c-123">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e473c-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e473c-124">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e473c-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e473c-125">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e473c-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e473c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e473c-126">Requirements</span></span>



| <span data-ttu-id="e473c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="e473c-127">Requirement</span></span> | <span data-ttu-id="e473c-128">Value</span><span class="sxs-lookup"><span data-stu-id="e473c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e473c-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e473c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e473c-130"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e473c-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e473c-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e473c-131">Library</span></span><br/> | <dl> <span data-ttu-id="e473c-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e473c-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e473c-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="e473c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e473c-134">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="e473c-134">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="e473c-135">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e473c-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




