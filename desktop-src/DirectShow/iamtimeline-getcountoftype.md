---
description: El método GetCountOfType recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos sus elementos secundarios.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline:: GetCountOfType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653514"
---
# <a name="iamtimelinegetcountoftype-method"></a><span data-ttu-id="097a2-103">IAMTimeline:: GetCountOfType (método)</span><span class="sxs-lookup"><span data-stu-id="097a2-103">IAMTimeline::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="097a2-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="097a2-104">\[Deprecated.</span></span> <span data-ttu-id="097a2-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="097a2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="097a2-106">El `GetCountOfType` método recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="097a2-106">The `GetCountOfType` method retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span>

## <a name="syntax"></a><span data-ttu-id="097a2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="097a2-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="097a2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="097a2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097a2-109">*Grupo*</span><span class="sxs-lookup"><span data-stu-id="097a2-109">*Group*</span></span> 
</dt> <dd>

<span data-ttu-id="097a2-110">Número de índice del grupo para el que se va a recuperar el recuento.</span><span class="sxs-lookup"><span data-stu-id="097a2-110">Index number of the group for which to retrieve the count.</span></span>

</dd> <dt>

<span data-ttu-id="097a2-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="097a2-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="097a2-112">Recibe el número de objetos del tipo especificado contenidos en el grupo y todas sus pistas virtuales de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="097a2-112">Receives the number of objects of the specified type contained in the group and all of its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="097a2-113">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="097a2-113">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="097a2-114">Recibe el recuento devuelto en *pval* más el número de composiciones buscadas, incluido este.</span><span class="sxs-lookup"><span data-stu-id="097a2-114">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="097a2-115">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="097a2-115">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="097a2-116">Miembro del tipo [**\_ principal \_**](timeline-major-type.md) de la escala de tiempo, que especifica el tipo de objeto que se va a contar.</span><span class="sxs-lookup"><span data-stu-id="097a2-116">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097a2-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="097a2-117">Return value</span></span>

<span data-ttu-id="097a2-118">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="097a2-118">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="097a2-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="097a2-119">Return code</span></span>                                                                                  | <span data-ttu-id="097a2-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="097a2-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="097a2-121"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="097a2-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="097a2-122">Correcto.</span><span class="sxs-lookup"><span data-stu-id="097a2-122">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="097a2-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="097a2-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="097a2-124">Número de grupo no válido.</span><span class="sxs-lookup"><span data-stu-id="097a2-124">Invalid group number.</span></span><br/>      |
| <dl> <span data-ttu-id="097a2-125"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="097a2-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="097a2-126">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="097a2-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="097a2-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="097a2-127">Remarks</span></span>

<span data-ttu-id="097a2-128">Llamar a este método equivale a llamar a [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) en el grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="097a2-128">Calling this method is equivalent to calling [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) on the specified group.</span></span> <span data-ttu-id="097a2-129">Vea la sección Comentarios de ese método para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="097a2-129">See the Remarks section of that method for more information.</span></span>

<span data-ttu-id="097a2-130">Normalmente, una aplicación no llamará a este método.</span><span class="sxs-lookup"><span data-stu-id="097a2-130">Typically, an application will not call this method.</span></span> <span data-ttu-id="097a2-131">Lo llama internamente el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="097a2-131">It is called internally by the render engine.</span></span>

> [!Note]  
> <span data-ttu-id="097a2-132">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="097a2-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="097a2-133">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="097a2-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="097a2-134">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="097a2-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="097a2-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="097a2-135">Requirements</span></span>



| <span data-ttu-id="097a2-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="097a2-136">Requirement</span></span> | <span data-ttu-id="097a2-137">Value</span><span class="sxs-lookup"><span data-stu-id="097a2-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="097a2-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="097a2-138">Header</span></span><br/>  | <dl> <span data-ttu-id="097a2-139"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="097a2-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="097a2-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="097a2-140">Library</span></span><br/> | <dl> <span data-ttu-id="097a2-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="097a2-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097a2-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="097a2-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097a2-143">**Interfaz IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="097a2-143">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="097a2-144">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="097a2-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




