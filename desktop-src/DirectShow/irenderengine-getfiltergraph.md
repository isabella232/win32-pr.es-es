---
description: El método GetFilterGraph recupera el gráfico de filtro que el motor de representación ha construido, si existe.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'IRenderEngine:: GetFilterGraph (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678943"
---
# <a name="irenderenginegetfiltergraph-method"></a><span data-ttu-id="9794a-103">IRenderEngine:: GetFilterGraph (método)</span><span class="sxs-lookup"><span data-stu-id="9794a-103">IRenderEngine::GetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="9794a-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="9794a-104">\[Deprecated.</span></span> <span data-ttu-id="9794a-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9794a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9794a-106">El `GetFilterGraph` método recupera el gráfico de filtro que el motor de representación ha construido, si existe.</span><span class="sxs-lookup"><span data-stu-id="9794a-106">The `GetFilterGraph` method retrieves the filter graph that the render engine has constructed, if any.</span></span>

## <a name="syntax"></a><span data-ttu-id="9794a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9794a-107">Syntax</span></span>


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a><span data-ttu-id="9794a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9794a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9794a-109">*ppFG* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9794a-109">*ppFG* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9794a-110">Recibe un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9794a-110">Receives a pointer to the filter graph's [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface.</span></span> <span data-ttu-id="9794a-111">Recibe el valor **null** si no hay ningún gráfico de filtros.</span><span class="sxs-lookup"><span data-stu-id="9794a-111">It receives the value **NULL** if there is no filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9794a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9794a-112">Return value</span></span>

<span data-ttu-id="9794a-113">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="9794a-113">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="9794a-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="9794a-114">Return code</span></span>                                                                                            | <span data-ttu-id="9794a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9794a-115">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="9794a-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="9794a-116"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="9794a-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9794a-117">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="9794a-118"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="9794a-118"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="9794a-119">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="9794a-119">Render engine failed to initialize.</span></span><br/> |
| <dl> <span data-ttu-id="9794a-120"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="9794a-120"><dt>**E\_POINTER**</dt></span></span> </dl>              | <span data-ttu-id="9794a-121">Puntero no válido.</span><span class="sxs-lookup"><span data-stu-id="9794a-121">Invalid pointer.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9794a-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9794a-122">Remarks</span></span>

<span data-ttu-id="9794a-123">Use el método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="9794a-123">Use the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method to build the front end of the filter graph.</span></span> <span data-ttu-id="9794a-124">Para la versión preliminar, use [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) para completar el gráfico.</span><span class="sxs-lookup"><span data-stu-id="9794a-124">For preview, use the [**IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) to complete the graph.</span></span> <span data-ttu-id="9794a-125">Para la salida de archivos, conecte el front-end a una combinación de escritor de archivos/Mux.</span><span class="sxs-lookup"><span data-stu-id="9794a-125">For file output, connect the front end to a mux/file writer combination.</span></span> <span data-ttu-id="9794a-126">Para obtener más información, vea [representar un proyecto](rendering-a-project.md).</span><span class="sxs-lookup"><span data-stu-id="9794a-126">For more information, see [Rendering a Project](rendering-a-project.md).</span></span>

<span data-ttu-id="9794a-127">El gráfico resultante puede ejecutarse, pausarse, detenerse y buscarse; No obstante, no se puede cambiar la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="9794a-127">The resulting graph can be run, paused, stopped, and seeked; the playback rate cannot be changed, however.</span></span>

<span data-ttu-id="9794a-128">En la devolución, si el valor de *\* ppFG* no es **null**, la interfaz **IGraphBuilder** tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="9794a-128">On return, if the value of *\*ppFG* is non-**NULL**, the **IGraphBuilder** interface has an outstanding reference count.</span></span> <span data-ttu-id="9794a-129">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="9794a-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="9794a-130">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="9794a-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9794a-131">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9794a-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9794a-132">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9794a-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9794a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9794a-133">Requirements</span></span>



| <span data-ttu-id="9794a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9794a-134">Requirement</span></span> | <span data-ttu-id="9794a-135">Value</span><span class="sxs-lookup"><span data-stu-id="9794a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9794a-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9794a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="9794a-137"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="9794a-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9794a-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9794a-138">Library</span></span><br/> | <dl> <span data-ttu-id="9794a-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9794a-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9794a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="9794a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9794a-141">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="9794a-141">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="9794a-142">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="9794a-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




