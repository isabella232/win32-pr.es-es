---
description: El método InsertSpace divide los objetos que existen en el momento especificado e inserta espacio entre ellos.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'IAMTimelineTrack:: InsertSpace (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690120"
---
# <a name="iamtimelinetrackinsertspace-method"></a><span data-ttu-id="24ffe-103">IAMTimelineTrack:: InsertSpace (método)</span><span class="sxs-lookup"><span data-stu-id="24ffe-103">IAMTimelineTrack::InsertSpace method</span></span>

> [!Note]  
> <span data-ttu-id="24ffe-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="24ffe-104">\[Deprecated.</span></span> <span data-ttu-id="24ffe-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24ffe-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="24ffe-106">El `InsertSpace` método divide los objetos que existen en el momento especificado e inserta espacio entre ellos.</span><span class="sxs-lookup"><span data-stu-id="24ffe-106">The `InsertSpace` method splits any objects that exist at the specified time and inserts space between them.</span></span>

## <a name="syntax"></a><span data-ttu-id="24ffe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24ffe-107">Syntax</span></span>


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="24ffe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24ffe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24ffe-109">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="24ffe-109">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="24ffe-110">Hora a la que se va a crear la división y el punto inicial del espacio insertado, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="24ffe-110">Time at which to create the split, and the starting point of the inserted space, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="24ffe-111">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="24ffe-111">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="24ffe-112">Punto final del espacio insertado, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="24ffe-112">End point of the inserted space, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24ffe-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24ffe-113">Return value</span></span>

<span data-ttu-id="24ffe-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24ffe-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="24ffe-115">Entre los posibles valores devueltos se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="24ffe-115">Possible return values include the following:</span></span>



| <span data-ttu-id="24ffe-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="24ffe-116">Return code</span></span>                                                                                   | <span data-ttu-id="24ffe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="24ffe-117">Description</span></span>                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="24ffe-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="24ffe-119">No hay ningún objeto en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="24ffe-119">There are no objects at the specified time.</span></span><br/> |
| <dl> <span data-ttu-id="24ffe-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="24ffe-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="24ffe-121">Success.</span></span><br/>                                    |
| <dl> <span data-ttu-id="24ffe-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="24ffe-123">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="24ffe-123">Invalid argument.</span></span><br/>                           |
| <dl> <span data-ttu-id="24ffe-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="24ffe-125">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="24ffe-125">Insufficient memory.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="24ffe-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="24ffe-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24ffe-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="24ffe-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="24ffe-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="24ffe-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="24ffe-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="24ffe-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24ffe-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24ffe-130">Requirements</span></span>



| <span data-ttu-id="24ffe-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="24ffe-131">Requirement</span></span> | <span data-ttu-id="24ffe-132">Value</span><span class="sxs-lookup"><span data-stu-id="24ffe-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24ffe-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="24ffe-133">Header</span></span><br/>  | <dl> <span data-ttu-id="24ffe-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="24ffe-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24ffe-135">Library</span></span><br/> | <dl> <span data-ttu-id="24ffe-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="24ffe-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24ffe-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="24ffe-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24ffe-138">**Interfaz IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="24ffe-138">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="24ffe-139">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="24ffe-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




