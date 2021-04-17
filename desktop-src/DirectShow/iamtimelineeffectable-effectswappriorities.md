---
description: El método EffectSwapPriorities cambia los niveles de prioridad de dos efectos.
ms.assetid: ff5ab294-3963-4df7-9299-ee7c7165e72f
title: 'IAMTimelineEffectable:: EffectSwapPriorities (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.EffectSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fb6a7dbee2d7f90da8f32e2a034e82df485f1ef4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691078"
---
# <a name="iamtimelineeffectableeffectswappriorities-method"></a><span data-ttu-id="5226f-103">IAMTimelineEffectable:: EffectSwapPriorities (método)</span><span class="sxs-lookup"><span data-stu-id="5226f-103">IAMTimelineEffectable::EffectSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="5226f-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="5226f-104">\[Deprecated.</span></span> <span data-ttu-id="5226f-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5226f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5226f-106">El `EffectSwapPriorities` método cambia los niveles de prioridad de dos efectos.</span><span class="sxs-lookup"><span data-stu-id="5226f-106">The `EffectSwapPriorities` method switches the priority levels of two effects.</span></span>

<span data-ttu-id="5226f-107">Dados dos valores de prioridad, este método intercambia los efectos en esas prioridades.</span><span class="sxs-lookup"><span data-stu-id="5226f-107">Given two priority values, this method swaps the effects at those priorities.</span></span> <span data-ttu-id="5226f-108">Cuando el método devuelve un resultado, el efecto que tenía en el primer nivel de prioridad está en el segundo nivel de prioridad y viceversa.</span><span class="sxs-lookup"><span data-stu-id="5226f-108">When the method returns, the effect that was at the first priority level is at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="5226f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5226f-109">Syntax</span></span>


```C++
HRESULT EffectSwapPriorities(
   long PriorityA,
   long PriorityB
);
```



## <a name="parameters"></a><span data-ttu-id="5226f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5226f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5226f-111">*Prioridada*</span><span class="sxs-lookup"><span data-stu-id="5226f-111">*PriorityA*</span></span> 
</dt> <dd>

<span data-ttu-id="5226f-112">Primer nivel de prioridad en el que se intercambian los efectos.</span><span class="sxs-lookup"><span data-stu-id="5226f-112">First priority level at which to swap effects.</span></span>

</dd> <dt>

<span data-ttu-id="5226f-113">*PriorityB*</span><span class="sxs-lookup"><span data-stu-id="5226f-113">*PriorityB*</span></span> 
</dt> <dd>

<span data-ttu-id="5226f-114">Segundo nivel de prioridad en el que se intercambian los efectos.</span><span class="sxs-lookup"><span data-stu-id="5226f-114">Second priority level at which to swap effects.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5226f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5226f-115">Return value</span></span>

<span data-ttu-id="5226f-116">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5226f-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5226f-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5226f-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5226f-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5226f-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5226f-119">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="5226f-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5226f-120">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5226f-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5226f-121">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5226f-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5226f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5226f-122">Requirements</span></span>



| <span data-ttu-id="5226f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="5226f-123">Requirement</span></span> | <span data-ttu-id="5226f-124">Value</span><span class="sxs-lookup"><span data-stu-id="5226f-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5226f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5226f-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5226f-126"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="5226f-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5226f-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5226f-127">Library</span></span><br/> | <dl> <span data-ttu-id="5226f-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5226f-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5226f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5226f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5226f-130">**Interfaz IAMTimelineEffectable**</span><span class="sxs-lookup"><span data-stu-id="5226f-130">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="5226f-131">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="5226f-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




