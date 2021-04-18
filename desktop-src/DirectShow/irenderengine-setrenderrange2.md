---
description: 'El método SetRenderRange2 establece el intervalo de tiempo en la escala de tiempo que se va a representar. Este método es equivalente a IRenderEngine:: SetRenderRange, pero toma valores de tipo Double.'
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: 'IRenderEngine:: SetRenderRange2 (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 555533b11c96073763af0d2b52823af44e3797be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680710"
---
# <a name="irenderenginesetrenderrange2-method"></a><span data-ttu-id="c7cdb-104">IRenderEngine:: SetRenderRange2 (método)</span><span class="sxs-lookup"><span data-stu-id="c7cdb-104">IRenderEngine::SetRenderRange2 method</span></span>

> [!Note]  
> <span data-ttu-id="c7cdb-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-105">\[Deprecated.</span></span> <span data-ttu-id="c7cdb-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c7cdb-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c7cdb-107">El `SetRenderRange2` método establece el intervalo de tiempo en la escala de tiempo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-107">The `SetRenderRange2` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="c7cdb-108">Este método es equivalente a [**IRenderEngine:: SetRenderRange**](irenderengine-setrenderrange.md), pero toma valores de tipo **Double**.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-108">This method is equivalent to [**IRenderEngine::SetRenderRange**](irenderengine-setrenderrange.md), but takes values of type **double**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7cdb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7cdb-109">Syntax</span></span>


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a><span data-ttu-id="c7cdb-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7cdb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7cdb-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="c7cdb-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="c7cdb-112">Hora de inicio, en segundos.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-112">Start time, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="c7cdb-113">*Detención*</span><span class="sxs-lookup"><span data-stu-id="c7cdb-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="c7cdb-114">Tiempo de detención, en segundos.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-114">Stop time, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7cdb-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7cdb-115">Return value</span></span>

<span data-ttu-id="c7cdb-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="c7cdb-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="c7cdb-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c7cdb-117">Return code</span></span>                                                                                            | <span data-ttu-id="c7cdb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7cdb-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c7cdb-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c7cdb-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="c7cdb-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="c7cdb-121"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="c7cdb-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="c7cdb-122">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c7cdb-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7cdb-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c7cdb-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c7cdb-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="c7cdb-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c7cdb-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="c7cdb-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c7cdb-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7cdb-127">Requirements</span></span>



| <span data-ttu-id="c7cdb-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7cdb-128">Requirement</span></span> | <span data-ttu-id="c7cdb-129">Value</span><span class="sxs-lookup"><span data-stu-id="c7cdb-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cdb-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7cdb-130">Header</span></span><br/>  | <dl> <span data-ttu-id="c7cdb-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7cdb-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c7cdb-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c7cdb-132">Library</span></span><br/> | <dl> <span data-ttu-id="c7cdb-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7cdb-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7cdb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7cdb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7cdb-135">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="c7cdb-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="c7cdb-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="c7cdb-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




