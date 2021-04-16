---
description: El método SpliceWithNext une el objeto de origen a otro objeto de origen.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'IAMTimelineSrc:: SpliceWithNext (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690079"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="30b56-103">IAMTimelineSrc:: SpliceWithNext (método)</span><span class="sxs-lookup"><span data-stu-id="30b56-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="30b56-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="30b56-104">\[Deprecated.</span></span> <span data-ttu-id="30b56-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="30b56-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="30b56-106">El `SpliceWithNext` método une el objeto de origen a otro objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="30b56-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="30b56-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30b56-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="30b56-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="30b56-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30b56-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="30b56-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="30b56-110">Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) del objeto de origen que se va a combinar con el origen actual.</span><span class="sxs-lookup"><span data-stu-id="30b56-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30b56-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="30b56-111">Return value</span></span>

<span data-ttu-id="30b56-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="30b56-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="30b56-113">Entre los posibles valores devueltos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="30b56-113">Possible return values include the following:</span></span>



| <span data-ttu-id="30b56-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="30b56-114">Return code</span></span>                                                                                   | <span data-ttu-id="30b56-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="30b56-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30b56-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="30b56-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="30b56-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="30b56-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="30b56-119">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="30b56-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="30b56-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="30b56-121">El objeto especificado por el parámetro *pNext* no es un objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="30b56-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="30b56-122"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="30b56-123">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="30b56-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="30b56-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30b56-124">Remarks</span></span>

<span data-ttu-id="30b56-125">Tal y como se implementa actualmente, este método descarta cualquier efecto en *pNext*.</span><span class="sxs-lookup"><span data-stu-id="30b56-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="30b56-126">Para que este método se ejecute correctamente, *pNext* debe ser un marco de coincidencia del objeto de origen actual, definido como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="30b56-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="30b56-127">Debe compartir el mismo archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="30b56-127">It must share the same source file.</span></span>
-   <span data-ttu-id="30b56-128">La hora de inicio del medio debe ser igual a la hora de detención del medio del origen actual.</span><span class="sxs-lookup"><span data-stu-id="30b56-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="30b56-129">La velocidad de reproducción debe ser la misma.</span><span class="sxs-lookup"><span data-stu-id="30b56-129">The playback rate must be the same.</span></span> <span data-ttu-id="30b56-130">La velocidad de reproducción es la duración multimedia dividida por la duración de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="30b56-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="30b56-131">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="30b56-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="30b56-132">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="30b56-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="30b56-133">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="30b56-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30b56-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30b56-134">Requirements</span></span>



| <span data-ttu-id="30b56-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="30b56-135">Requirement</span></span> | <span data-ttu-id="30b56-136">Value</span><span class="sxs-lookup"><span data-stu-id="30b56-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30b56-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="30b56-137">Header</span></span><br/>  | <dl> <span data-ttu-id="30b56-138"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="30b56-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30b56-139">Library</span></span><br/> | <dl> <span data-ttu-id="30b56-140"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30b56-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30b56-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="30b56-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30b56-142">**Interfaz IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="30b56-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="30b56-143">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="30b56-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




