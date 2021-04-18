---
description: El método SetFilterGraph especifica un gráfico de filtro para que lo use el motor de representación.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine:: SetFilterGraph (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681222"
---
# <a name="irenderenginesetfiltergraph-method"></a><span data-ttu-id="976a3-103">IRenderEngine:: SetFilterGraph (método)</span><span class="sxs-lookup"><span data-stu-id="976a3-103">IRenderEngine::SetFilterGraph method</span></span>

> [!Note]  
> <span data-ttu-id="976a3-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="976a3-104">\[Deprecated.</span></span> <span data-ttu-id="976a3-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="976a3-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="976a3-106">El `SetFilterGraph` método especifica un gráfico de filtro para que lo use el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="976a3-106">The `SetFilterGraph` method specifies a filter graph for the render engine to use.</span></span>

## <a name="syntax"></a><span data-ttu-id="976a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="976a3-107">Syntax</span></span>


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a><span data-ttu-id="976a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="976a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="976a3-109">*pFG*</span><span class="sxs-lookup"><span data-stu-id="976a3-109">*pFG*</span></span> 
</dt> <dd>

<span data-ttu-id="976a3-110">Puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="976a3-110">Pointer to the [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) interface of the filter graph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="976a3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="976a3-111">Return value</span></span>

<span data-ttu-id="976a3-112">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="976a3-112">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="976a3-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="976a3-113">Return code</span></span>                                                                                            | <span data-ttu-id="976a3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="976a3-114">Description</span></span>                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="976a3-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="976a3-115"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="976a3-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="976a3-116">Success.</span></span><br/>                            |
| <dl> <span data-ttu-id="976a3-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="976a3-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>           | <span data-ttu-id="976a3-118">Argumento no válido.</span><span class="sxs-lookup"><span data-stu-id="976a3-118">Invalid argument.</span></span><br/>                   |
| <dl> <span data-ttu-id="976a3-119"><dt>**E \_ debe \_ inicializar el \_ representador**</dt></span><span class="sxs-lookup"><span data-stu-id="976a3-119"><dt>**E\_MUST\_INIT\_RENDERER**</dt></span></span> </dl> | <span data-ttu-id="976a3-120">No se pudo inicializar el motor de representación.</span><span class="sxs-lookup"><span data-stu-id="976a3-120">Render engine failed to initialize.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="976a3-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="976a3-121">Remarks</span></span>

<span data-ttu-id="976a3-122">La mayoría de las aplicaciones no necesitan llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="976a3-122">Most applications do not need to call this method.</span></span> <span data-ttu-id="976a3-123">Es más habitual permitir que el motor de representación cree el gráfico automáticamente, llamando al método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="976a3-123">It is more typical to let the render engine build the graph for you, by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span>

<span data-ttu-id="976a3-124">Este método produce un error si el motor de representación ya tiene un gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="976a3-124">This method fails if the render engine already has a filter graph.</span></span>

<span data-ttu-id="976a3-125">No recupere nunca un puntero a un gráfico de filtro creado por un motor de representación y, a continuación, úselo como parámetro para este método en otro motor de representación.</span><span class="sxs-lookup"><span data-stu-id="976a3-125">Never retrieve a pointer to a filter graph created by one render engine and then use it as the parameter to this method on another render engine.</span></span> <span data-ttu-id="976a3-126">Si lo hace, se producirán resultados imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="976a3-126">Doing so will cause unpredictable results.</span></span>

<span data-ttu-id="976a3-127">El método **ConnectFrontEnd** anula el gráfico de filtros existente, pero mantiene la misma instancia de Filter Graph Manager.</span><span class="sxs-lookup"><span data-stu-id="976a3-127">The **ConnectFrontEnd** method tears down any existing filter graph, but keeps the same Filter Graph Manager instance.</span></span>

> [!Note]  
> <span data-ttu-id="976a3-128">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="976a3-128">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="976a3-129">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="976a3-129">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="976a3-130">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="976a3-130">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="976a3-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="976a3-131">Requirements</span></span>



| <span data-ttu-id="976a3-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="976a3-132">Requirement</span></span> | <span data-ttu-id="976a3-133">Value</span><span class="sxs-lookup"><span data-stu-id="976a3-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="976a3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="976a3-134">Header</span></span><br/>  | <dl> <span data-ttu-id="976a3-135"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="976a3-135"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="976a3-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="976a3-136">Library</span></span><br/> | <dl> <span data-ttu-id="976a3-137"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="976a3-137"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="976a3-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="976a3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="976a3-139">**Interfaz IRenderEngine**</span><span class="sxs-lookup"><span data-stu-id="976a3-139">**IRenderEngine Interface**</span></span>](irenderengine.md)
</dt> <dt>

[<span data-ttu-id="976a3-140">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="976a3-140">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




