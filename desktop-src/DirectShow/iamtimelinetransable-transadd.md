---
description: El método TransAdd agrega una transición al objeto. Un objeto puede tener varias transiciones, pero no deben superponerse en el tiempo. Las transiciones deben estar dentro de los límites de tiempo del objeto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable:: TransAdd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690992"
---
# <a name="iamtimelinetransabletransadd-method"></a><span data-ttu-id="b0795-105">IAMTimelineTransable:: TransAdd (método)</span><span class="sxs-lookup"><span data-stu-id="b0795-105">IAMTimelineTransable::TransAdd method</span></span>

> [!Note]  
> <span data-ttu-id="b0795-106">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="b0795-106">\[Deprecated.</span></span> <span data-ttu-id="b0795-107">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b0795-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b0795-108">El `TransAdd` método agrega una transición al objeto.</span><span class="sxs-lookup"><span data-stu-id="b0795-108">The `TransAdd` method adds a transition to the object.</span></span> <span data-ttu-id="b0795-109">Un objeto puede tener varias transiciones, pero no deben superponerse en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="b0795-109">An object can have multiple transitions, but they must not overlap in time.</span></span> <span data-ttu-id="b0795-110">Las transiciones deben estar dentro de los límites de tiempo del objeto.</span><span class="sxs-lookup"><span data-stu-id="b0795-110">Transitions must fall within the time boundaries of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0795-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0795-111">Syntax</span></span>


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a><span data-ttu-id="b0795-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0795-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0795-113">*pTrans*</span><span class="sxs-lookup"><span data-stu-id="b0795-113">*pTrans*</span></span> 
</dt> <dd>

<span data-ttu-id="b0795-114">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la transición que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="b0795-114">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the transition to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0795-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0795-115">Return value</span></span>

<span data-ttu-id="b0795-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b0795-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b0795-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b0795-117">Return code</span></span>                                                                                   | <span data-ttu-id="b0795-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0795-118">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="b0795-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b0795-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b0795-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="b0795-120">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b0795-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b0795-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b0795-122">No se puede insertar la transición.</span><span class="sxs-lookup"><span data-stu-id="b0795-122">Cannot insert the transition.</span></span><br/>              |
| <dl> <span data-ttu-id="b0795-123"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="b0795-123"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="b0795-124">*pTrans* no es un puntero a una transición.</span><span class="sxs-lookup"><span data-stu-id="b0795-124">*pTrans* is not a pointer to a transition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0795-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0795-125">Remarks</span></span>

<span data-ttu-id="b0795-126">Si la transición se superpone a una transición existente, el método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="b0795-126">If the transition overlaps an existing transition, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="b0795-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="b0795-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b0795-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0795-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b0795-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b0795-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b0795-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0795-130">Requirements</span></span>



| <span data-ttu-id="b0795-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0795-131">Requirement</span></span> | <span data-ttu-id="b0795-132">Value</span><span class="sxs-lookup"><span data-stu-id="b0795-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0795-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0795-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b0795-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0795-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b0795-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0795-135">Library</span></span><br/> | <dl> <span data-ttu-id="b0795-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0795-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0795-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0795-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0795-138">**Interfaz IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="b0795-138">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="b0795-139">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="b0795-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




