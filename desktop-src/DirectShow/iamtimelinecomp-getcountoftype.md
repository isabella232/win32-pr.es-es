---
description: El método GetCountOfType recupera el número de objetos de un tipo determinado incluido en esta composición y todas sus pistas virtuales de forma recursiva.
ms.assetid: 2d14ccf7-77bc-4095-bfb8-12a52b4b9595
title: 'IAMTimelineComp:: GetCountOfType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 69c4c582a3883feedec962bfb88b4a833be3750b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680975"
---
# <a name="iamtimelinecompgetcountoftype-method"></a><span data-ttu-id="a616c-103">IAMTimelineComp:: GetCountOfType (método)</span><span class="sxs-lookup"><span data-stu-id="a616c-103">IAMTimelineComp::GetCountOfType method</span></span>

> [!Note]  
> <span data-ttu-id="a616c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="a616c-104">\[Deprecated.</span></span> <span data-ttu-id="a616c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a616c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a616c-106">El `GetCountOfType` método recupera el número de objetos de un tipo determinado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="a616c-106">The `GetCountOfType` method retrieves the number of objects of a given type contained in this composition and all its virtual tracks, recursively.</span></span>

## <a name="syntax"></a><span data-ttu-id="a616c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a616c-107">Syntax</span></span>


```C++
HRESULT GetCountOfType(
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a><span data-ttu-id="a616c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a616c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a616c-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="a616c-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="a616c-110">Recibe el número de objetos del tipo especificado contenidos en esta composición y todas sus pistas virtuales de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="a616c-110">Receives the number of objects of the specified type contained in this composition and all its virtual tracks, recursively.</span></span>

</dd> <dt>

<span data-ttu-id="a616c-111">*pValWithComps*</span><span class="sxs-lookup"><span data-stu-id="a616c-111">*pValWithComps*</span></span> 
</dt> <dd>

<span data-ttu-id="a616c-112">Recibe el recuento devuelto en *pval* más el número de composiciones buscadas, incluido este.</span><span class="sxs-lookup"><span data-stu-id="a616c-112">Receives the count returned in *pVal* plus the number of compositions searched, including this one.</span></span>

</dd> <dt>

<span data-ttu-id="a616c-113">*MajorType*</span><span class="sxs-lookup"><span data-stu-id="a616c-113">*MajorType*</span></span> 
</dt> <dd>

<span data-ttu-id="a616c-114">Miembro del tipo [**\_ principal \_**](timeline-major-type.md) de la escala de tiempo, que especifica el tipo de objeto que se va a contar.</span><span class="sxs-lookup"><span data-stu-id="a616c-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type, specifying the type of object to count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a616c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a616c-115">Return value</span></span>

<span data-ttu-id="a616c-116">Devuelve \_ si es correcto, o bien el puntero E, de \_ lo contrario.</span><span class="sxs-lookup"><span data-stu-id="a616c-116">Returns S\_OK if successful, or E\_POINTER otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a616c-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a616c-117">Remarks</span></span>

<span data-ttu-id="a616c-118">Normalmente, una aplicación no llamará a este método.</span><span class="sxs-lookup"><span data-stu-id="a616c-118">Typically, an application will not call this method.</span></span> <span data-ttu-id="a616c-119">Lo llama el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="a616c-119">It is called by the render engine.</span></span>

<span data-ttu-id="a616c-120">Si cuenta las composiciones, el valor devuelto en *pval* es cero y el valor devuelto en *pValWithComps* es el número de composiciones.</span><span class="sxs-lookup"><span data-stu-id="a616c-120">If you count compositions, the value returned in *pVal* is zero and the value returned in *pValWithComps* is the number of compositions.</span></span> <span data-ttu-id="a616c-121">El valor de *\* pValWithComps* incluye la composición en la que se llama al método.</span><span class="sxs-lookup"><span data-stu-id="a616c-121">The value of *\*pValWithComps* includes the composition on which you call the method.</span></span> <span data-ttu-id="a616c-122">Por ejemplo, si llama a este método en una composición vacía, *\* pValWithComps* es igual a 1.</span><span class="sxs-lookup"><span data-stu-id="a616c-122">For example, if you call this method on an empty composition, *\*pValWithComps* equals 1.</span></span>

<span data-ttu-id="a616c-123">Los grupos no pueden residir en composiciones, por lo que no puede usar este método para contar grupos.</span><span class="sxs-lookup"><span data-stu-id="a616c-123">Groups cannot reside inside compositions, so you cannot use this method to count groups.</span></span> <span data-ttu-id="a616c-124">(El recuento devuelto siempre será cero). Para contar los grupos, llame al método [**IAMTimeline:: GetGroupCount**](iamtimeline-getgroupcount.md) .</span><span class="sxs-lookup"><span data-stu-id="a616c-124">(The returned count will always be zero.) To count groups, call the [**IAMTimeline::GetGroupCount**](iamtimeline-getgroupcount.md) method.</span></span>

> [!Note]  
> <span data-ttu-id="a616c-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="a616c-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a616c-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a616c-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a616c-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a616c-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a616c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a616c-128">Requirements</span></span>



| <span data-ttu-id="a616c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a616c-129">Requirement</span></span> | <span data-ttu-id="a616c-130">Value</span><span class="sxs-lookup"><span data-stu-id="a616c-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a616c-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a616c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="a616c-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="a616c-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a616c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a616c-133">Library</span></span><br/> | <dl> <span data-ttu-id="a616c-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a616c-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a616c-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="a616c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a616c-136">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="a616c-136">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="a616c-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="a616c-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




