---
description: 'El método SplitAt2 divide el objeto en el momento especificado. Este método es equivalente a IAMTimelineSplittable:: SplitAt, pero toma un valor REFTIME.'
ms.assetid: 33d240db-4ef8-455a-81a6-633ee12837c2
title: 'IAMTimelineSplittable:: SplitAt2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c0f941469983f2eaebf0363797fb54a81388bc51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679175"
---
# <a name="iamtimelinesplittablesplitat2-method"></a><span data-ttu-id="8ebb0-104">IAMTimelineSplittable:: SplitAt2 (método)</span><span class="sxs-lookup"><span data-stu-id="8ebb0-104">IAMTimelineSplittable::SplitAt2 method</span></span>

> [!Note]  
> <span data-ttu-id="8ebb0-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-105">\[Deprecated.</span></span> <span data-ttu-id="8ebb0-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8ebb0-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="8ebb0-107">El `SplitAt2` método divide el objeto en el momento especificado.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-107">The `SplitAt2` method splits the object at the specified time.</span></span> <span data-ttu-id="8ebb0-108">Este método es equivalente a [**IAMTimelineSplittable:: SplitAt**](iamtimelinesplittable-splitat.md), pero toma un valor [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="8ebb0-108">This method is equivalent to [**IAMTimelineSplittable::SplitAt**](iamtimelinesplittable-splitat.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ebb0-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ebb0-109">Syntax</span></span>


```C++
HRESULT SplitAt2(
   REFTIME Time
);
```



## <a name="parameters"></a><span data-ttu-id="8ebb0-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ebb0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ebb0-111">*Time*</span><span class="sxs-lookup"><span data-stu-id="8ebb0-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="8ebb0-112">Hora en la que se va a dividir el objeto, en segundos, con respecto al inicio de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-112">Time at which to split the object, relative to the start of the timeline, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ebb0-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ebb0-113">Return value</span></span>

<span data-ttu-id="8ebb0-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ebb0-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="8ebb0-115">Entre los valores posibles figuran los siguientes:</span><span class="sxs-lookup"><span data-stu-id="8ebb0-115">Possible values include the following:</span></span>



| <span data-ttu-id="8ebb0-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ebb0-116">Return code</span></span>                                                                                   | <span data-ttu-id="8ebb0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ebb0-117">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8ebb0-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-118"><dt>**S\_FALSE**</dt></span></span> </dl>       | <span data-ttu-id="8ebb0-119">Nada para dividir.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-119">Nothing to split.</span></span><br/>                       |
| <dl> <span data-ttu-id="8ebb0-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ebb0-121">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-121">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="8ebb0-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8ebb0-123">El objeto no existe en este momento.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-123">The object does not exist at this time.</span></span><br/> |
| <dl> <span data-ttu-id="8ebb0-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ebb0-125">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-125">Insufficient memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8ebb0-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ebb0-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ebb0-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="8ebb0-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="8ebb0-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="8ebb0-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="8ebb0-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ebb0-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ebb0-130">Requirements</span></span>



| <span data-ttu-id="8ebb0-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ebb0-131">Requirement</span></span> | <span data-ttu-id="8ebb0-132">Value</span><span class="sxs-lookup"><span data-stu-id="8ebb0-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ebb0-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ebb0-133">Header</span></span><br/>  | <dl> <span data-ttu-id="8ebb0-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="8ebb0-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ebb0-135">Library</span></span><br/> | <dl> <span data-ttu-id="8ebb0-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ebb0-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ebb0-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ebb0-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ebb0-138">**Interfaz IAMTimelineSplittable**</span><span class="sxs-lookup"><span data-stu-id="8ebb0-138">**IAMTimelineSplittable Interface**</span></span>](iamtimelinesplittable.md)
</dt> <dt>

[<span data-ttu-id="8ebb0-139">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="8ebb0-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




