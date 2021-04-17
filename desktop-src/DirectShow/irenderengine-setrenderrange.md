---
description: El método SetRenderRange establece el intervalo de tiempo en la escala de tiempo que se va a representar. Los objetos que se encuentran fuera del intervalo especificado no se representan y no se les asignan recursos.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: 'IRenderEngine:: SetRenderRange (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e715c2c0077a890948cfd5f5026afe98633325ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680711"
---
# <a name="irenderenginesetrenderrange-method"></a><span data-ttu-id="25e5a-104">IRenderEngine:: SetRenderRange (método)</span><span class="sxs-lookup"><span data-stu-id="25e5a-104">IRenderEngine::SetRenderRange method</span></span>

> [!Note]  
> <span data-ttu-id="25e5a-105">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="25e5a-105">\[Deprecated.</span></span> <span data-ttu-id="25e5a-106">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="25e5a-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="25e5a-107">El `SetRenderRange` método establece el intervalo de tiempo en la escala de tiempo que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="25e5a-107">The `SetRenderRange` method sets the range of time on the timeline to be rendered.</span></span> <span data-ttu-id="25e5a-108">Los objetos que se encuentran fuera del intervalo especificado no se representan y no se les asignan recursos.</span><span class="sxs-lookup"><span data-stu-id="25e5a-108">Objects that lie outside the specified range are not rendered, and resources are not allocated for them.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e5a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25e5a-109">Syntax</span></span>


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a><span data-ttu-id="25e5a-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25e5a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25e5a-111">*Iniciar*</span><span class="sxs-lookup"><span data-stu-id="25e5a-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="25e5a-112">Hora de inicio, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="25e5a-112">Start time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="25e5a-113">*Detención*</span><span class="sxs-lookup"><span data-stu-id="25e5a-113">*Stop*</span></span> 
</dt> <dd>

<span data-ttu-id="25e5a-114">Hora de detención, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="25e5a-114">Stop time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25e5a-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="25e5a-115">Return value</span></span>

<span data-ttu-id="25e5a-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="25e5a-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="25e5a-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="25e5a-117">Return code</span></span>                                                                                            | <span data-ttu-id="25e5a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="25e5a-118">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="25e5a-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="25e5a-119"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="25e5a-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="25e5a-120">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="25e5a-121"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="25e5a-121"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="25e5a-122">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="25e5a-122">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25e5a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25e5a-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="25e5a-124">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="25e5a-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="25e5a-125">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="25e5a-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="25e5a-126">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="25e5a-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="25e5a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25e5a-127">Requirements</span></span>



| <span data-ttu-id="25e5a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e5a-128">Requirement</span></span> | <span data-ttu-id="25e5a-129">Value</span><span class="sxs-lookup"><span data-stu-id="25e5a-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25e5a-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25e5a-130">Header</span></span><br/>  | <dl> <span data-ttu-id="25e5a-131"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="25e5a-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="25e5a-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25e5a-132">Library</span></span><br/> | <dl> <span data-ttu-id="25e5a-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25e5a-133"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e5a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="25e5a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e5a-135">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="25e5a-135">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="25e5a-136">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="25e5a-136">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




