---
description: El método SetTimelineObject establece la escala de tiempo para que la use el motor de representación.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: 'IRenderEngine:: SetTimelineObject (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 954fab15e92e6111439abb66d53d53525a5afdb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680708"
---
# <a name="irenderenginesettimelineobject-method"></a><span data-ttu-id="14c71-103">IRenderEngine:: SetTimelineObject (método)</span><span class="sxs-lookup"><span data-stu-id="14c71-103">IRenderEngine::SetTimelineObject method</span></span>

> [!Note]  
> <span data-ttu-id="14c71-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="14c71-104">\[Deprecated.</span></span> <span data-ttu-id="14c71-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="14c71-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="14c71-106">El `SetTimelineObject` método establece la escala de tiempo para que la use el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="14c71-106">The `SetTimelineObject` method sets the timeline for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="14c71-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14c71-107">Syntax</span></span>


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a><span data-ttu-id="14c71-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14c71-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14c71-109">*pTimeline*</span><span class="sxs-lookup"><span data-stu-id="14c71-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="14c71-110">Puntero a la interfaz [**IAMTimeline**](iamtimeline.md) del objeto Timeline.</span><span class="sxs-lookup"><span data-stu-id="14c71-110">Pointer to the timeline object's [**IAMTimeline**](iamtimeline.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14c71-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14c71-111">Return value</span></span>

<span data-ttu-id="14c71-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="14c71-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="14c71-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="14c71-113">Return code</span></span>                                                                                            | <span data-ttu-id="14c71-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="14c71-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="14c71-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="14c71-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="14c71-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="14c71-117"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-117"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="14c71-118">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="14c71-118">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="14c71-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="14c71-120">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="14c71-120">Insufficient memory.</span></span><br/>                |
| <dl> <span data-ttu-id="14c71-121"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-121"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="14c71-122">Puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="14c71-122">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="14c71-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="14c71-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="14c71-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="14c71-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="14c71-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="14c71-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="14c71-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="14c71-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="14c71-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14c71-127">Requirements</span></span>



| <span data-ttu-id="14c71-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="14c71-128">Requirement</span></span> | <span data-ttu-id="14c71-129">Value</span><span class="sxs-lookup"><span data-stu-id="14c71-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="14c71-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="14c71-130">Header</span></span><br/>  | <dl> <span data-ttu-id="14c71-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="14c71-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="14c71-132">Library</span></span><br/> | <dl> <span data-ttu-id="14c71-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14c71-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14c71-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="14c71-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c71-135">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="14c71-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="14c71-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="14c71-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




