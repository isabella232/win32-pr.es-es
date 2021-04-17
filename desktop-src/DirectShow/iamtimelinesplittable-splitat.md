---
description: El método SplitAt divide el objeto en el momento especificado.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'IAMTimelineSplittable:: SplitAt (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690546"
---
# <a name="iamtimelinesplittablesplitat-method"></a><span data-ttu-id="dcf80-103">IAMTimelineSplittable:: SplitAt (método)</span><span class="sxs-lookup"><span data-stu-id="dcf80-103">IAMTimelineSplittable::SplitAt method</span></span>

> [!Note]  
> <span data-ttu-id="dcf80-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="dcf80-104">\[Deprecated.</span></span> <span data-ttu-id="dcf80-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dcf80-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="dcf80-106">El `SplitAt` método divide el objeto en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="dcf80-106">The `SplitAt` method splits the object at the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf80-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcf80-107">Syntax</span></span>


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="dcf80-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dcf80-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf80-109">*Time*</span><span class="sxs-lookup"><span data-stu-id="dcf80-109">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="dcf80-110">Hora a la que se va a dividir el objeto, en relación con el inicio de la escala de tiempo, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="dcf80-110">Time at which to split the object, relative to the start of the timeline, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf80-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dcf80-111">Return value</span></span>

<span data-ttu-id="dcf80-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dcf80-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="dcf80-113">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="dcf80-113">Possible values include the following:</span></span>



| <span data-ttu-id="dcf80-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="dcf80-114">Return code</span></span>                                                                                   | <span data-ttu-id="dcf80-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="dcf80-115">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="dcf80-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-116"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="dcf80-117">Nada para dividir.</span><span class="sxs-lookup"><span data-stu-id="dcf80-117">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="dcf80-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dcf80-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dcf80-119">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="dcf80-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dcf80-121">El objeto no existe en este momento.</span><span class="sxs-lookup"><span data-stu-id="dcf80-121">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="dcf80-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dcf80-123">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="dcf80-123">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dcf80-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcf80-124">Remarks</span></span>

<span data-ttu-id="dcf80-125">Si divide un origen, un efecto o una transición, este método crea un segundo objeto del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="dcf80-125">If you split a source, effect, or transition, this method creates a second object of the same type.</span></span> <span data-ttu-id="dcf80-126">El objeto original se trunca en el tiempo de división especificado y el nuevo objeto reemplaza la parte truncada.</span><span class="sxs-lookup"><span data-stu-id="dcf80-126">The original object is truncated at the specified split time, and the new object replaces the truncated portion.</span></span> <span data-ttu-id="dcf80-127">El nuevo objeto hereda todas las propiedades.</span><span class="sxs-lookup"><span data-stu-id="dcf80-127">The new object inherits all of the same properties.</span></span> <span data-ttu-id="dcf80-128">En un objeto de origen, el método también divide los efectos que se encuentran en el tiempo de división.</span><span class="sxs-lookup"><span data-stu-id="dcf80-128">In a source object, the method also splits any effects that fall on the split time.</span></span>

<span data-ttu-id="dcf80-129">La llamada a este método en una pista divide todos los orígenes, efectos y transiciones contenidos en la pista en el tiempo de división especificado.</span><span class="sxs-lookup"><span data-stu-id="dcf80-129">Calling this method on a track splits all the sources, effects, and transitions that are contained in the track at the specified split time.</span></span> <span data-ttu-id="dcf80-130">No crea una segunda pista. (Una pista comienza en el tiempo cero y se extiende hasta el infinito).</span><span class="sxs-lookup"><span data-stu-id="dcf80-130">It does not create a second track. (A track begins at time zero and extends to infinity.)</span></span>

<span data-ttu-id="dcf80-131">En el caso de una pista, si el tiempo de división es posterior a todo lo que hay en la pista, el método devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="dcf80-131">For a track, if the split time is later than everything in the track, the method returns S\_FALSE.</span></span> <span data-ttu-id="dcf80-132">Para cualquier otro objeto, si el tiempo de división no se encuentra en ningún lugar dentro del objeto, el método devuelve E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="dcf80-132">For any other object, if the split time does not fall anywhere within the object, the method returns E\_INVALIDARG.</span></span>

> [!Note]  
> <span data-ttu-id="dcf80-133">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="dcf80-133">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="dcf80-134">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="dcf80-134">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="dcf80-135">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="dcf80-135">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcf80-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcf80-136">Requirements</span></span>



| <span data-ttu-id="dcf80-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf80-137">Requirement</span></span> | <span data-ttu-id="dcf80-138">Value</span><span class="sxs-lookup"><span data-stu-id="dcf80-138">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf80-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dcf80-139">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf80-140"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-140"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="dcf80-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dcf80-141">Library</span></span><br/> | <dl> <span data-ttu-id="dcf80-142"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf80-142"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcf80-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcf80-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf80-144">**Interfaz IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="dcf80-144">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="dcf80-145">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="dcf80-145">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




