---
description: 'El método InsertSpace2 divide los objetos que existen en el momento especificado e inserta espacio entre ellos. Este método es equivalente a IAMTimelineTrack:: InsertSpace, pero toma valores REFTIME.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'IAMTimelineTrack:: InsertSpace2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690116"
---
# <a name="iamtimelinetrackinsertspace2-method"></a><span data-ttu-id="815da-104">IAMTimelineTrack:: InsertSpace2 (método)</span><span class="sxs-lookup"><span data-stu-id="815da-104">IAMTimelineTrack::InsertSpace2 method</span></span>

> [!Note]  
> <span data-ttu-id="815da-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="815da-105">\[Deprecated.</span></span> <span data-ttu-id="815da-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="815da-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="815da-107">El `InsertSpace2` método divide los objetos que existen en el momento especificado e inserta espacio entre ellos.</span><span class="sxs-lookup"><span data-stu-id="815da-107">The `InsertSpace2` method splits any objects that exist at the specified time and inserts space between them.</span></span> <span data-ttu-id="815da-108">Este método es equivalente a [**IAMTimelineTrack:: InsertSpace**](iamtimelinetrack-insertspace.md), pero toma valores [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="815da-108">This method is equivalent to [**IAMTimelineTrack::InsertSpace**](iamtimelinetrack-insertspace.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="815da-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="815da-109">Syntax</span></span>


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="815da-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="815da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="815da-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="815da-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="815da-112">Hora a la que se va a crear la división y el punto inicial del espacio insertado, en segundos.</span><span class="sxs-lookup"><span data-stu-id="815da-112">Time at which to create the split, and the starting point of the inserted space, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="815da-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="815da-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="815da-114">Punto final del espacio insertado, en segundos.</span><span class="sxs-lookup"><span data-stu-id="815da-114">End point of the inserted space, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="815da-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="815da-115">Return value</span></span>

<span data-ttu-id="815da-116">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="815da-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="815da-117">Entre los posibles valores devueltos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="815da-117">Possible return values include the following:</span></span>



| <span data-ttu-id="815da-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="815da-118">Return code</span></span>                                                                                   | <span data-ttu-id="815da-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="815da-119">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="815da-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="815da-120"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="815da-121">No hay ningún objeto en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="815da-121">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="815da-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="815da-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="815da-123">Correcto.</span><span class="sxs-lookup"><span data-stu-id="815da-123">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="815da-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="815da-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="815da-125">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="815da-125">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="815da-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="815da-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="815da-127">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="815da-127">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="815da-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="815da-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="815da-129">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="815da-129">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="815da-130">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="815da-130">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="815da-131">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="815da-131">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="815da-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="815da-132">Requirements</span></span>



| <span data-ttu-id="815da-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="815da-133">Requirement</span></span> | <span data-ttu-id="815da-134">Value</span><span class="sxs-lookup"><span data-stu-id="815da-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="815da-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="815da-135">Header</span></span><br/>  | <dl> <span data-ttu-id="815da-136"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="815da-136"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="815da-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="815da-137">Library</span></span><br/> | <dl> <span data-ttu-id="815da-138"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="815da-138"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="815da-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="815da-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="815da-140">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="815da-140">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="815da-141">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="815da-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




