---
description: El método GetTimelineObject recupera la escala de tiempo que el motor de representación está usando actualmente.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: 'IRenderEngine:: GetTimelineObject (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: aab8e9a5f77affc464763b1c5a5045eaa4fc042a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680719"
---
# <a name="irenderenginegettimelineobject-method"></a><span data-ttu-id="e3af0-103">IRenderEngine:: GetTimelineObject (método)</span><span class="sxs-lookup"><span data-stu-id="e3af0-103">IRenderEngine::GetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="e3af0-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="e3af0-104">\[Deprecated.</span></span> <span data-ttu-id="e3af0-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3af0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3af0-106">El `GetTimelineObject` método recupera la escala de tiempo que el motor de representación está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e3af0-106">The `GetTimelineObject` method retrieves the timeline that the render engine is currently using.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3af0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3af0-107">Syntax</span></span>


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="e3af0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3af0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3af0-109">*ppTimeline* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e3af0-109">*ppTimeline* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3af0-110">Recibe un puntero a la interfaz [**IAMTimeline**](iamtimeline.md) de la escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e3af0-110">Receives a pointer to the timeline's [**IAMTimeline**](iamtimeline.md) interface.</span></span> <span data-ttu-id="e3af0-111">Recibe el valor **null** si no hay ninguna escala de tiempo.</span><span class="sxs-lookup"><span data-stu-id="e3af0-111">It receives the value **NULL** if there is no timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3af0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3af0-112">Return value</span></span>

<span data-ttu-id="e3af0-113">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="e3af0-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="e3af0-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e3af0-114">Return code</span></span>                                                                                            | <span data-ttu-id="e3af0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3af0-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e3af0-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e3af0-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e3af0-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="e3af0-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-118"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="e3af0-119">Puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="e3af0-119">Invalid pointer.</span></span><br/>                    |
| <dl> <span data-ttu-id="e3af0-120"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-120"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="e3af0-121">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="e3af0-121">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3af0-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3af0-122">Remarks</span></span>

<span data-ttu-id="e3af0-123">En la devolución, si el valor de *\* ppTimeline* no es **null**, la interfaz **IAMTimeline** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="e3af0-123">On return, if the value of *\*ppTimeline* is non-**NULL**, the **IAMTimeline** interface has an outstanding reference count.</span></span> <span data-ttu-id="e3af0-124">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="e3af0-124">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="e3af0-125">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="e3af0-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3af0-126">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3af0-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3af0-127">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e3af0-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3af0-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3af0-128">Requirements</span></span>



| <span data-ttu-id="e3af0-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3af0-129">Requirement</span></span> | <span data-ttu-id="e3af0-130">Value</span><span class="sxs-lookup"><span data-stu-id="e3af0-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3af0-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3af0-131">Header</span></span><br/>  | <dl> <span data-ttu-id="e3af0-132"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3af0-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3af0-133">Library</span></span><br/> | <dl> <span data-ttu-id="e3af0-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3af0-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3af0-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3af0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3af0-136">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="e3af0-136">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="e3af0-137">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="e3af0-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




