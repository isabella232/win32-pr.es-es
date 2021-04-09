---
description: Obtiene todos los objetos IContextNode de la sugerencia de análisis que están asociados a IInkAnalyzer.
ms.assetid: 97cff025-3d9e-4137-b1ac-635153804744
title: 'IInkAnalyzer:: GetAnalysisHints (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisHints
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c5ce66eeb6362ed74f1df1a38f220603d3a30117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154415"
---
# <a name="iinkanalyzergetanalysishints-method"></a><span data-ttu-id="7fcad-103">IInkAnalyzer:: GetAnalysisHints (método)</span><span class="sxs-lookup"><span data-stu-id="7fcad-103">IInkAnalyzer::GetAnalysisHints method</span></span>

<span data-ttu-id="7fcad-104">Obtiene todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis que están asociados a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-104">Gets all of the analysis hint [**IContextNode**](icontextnode.md) objects that are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcad-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7fcad-105">Syntax</span></span>


```C++
HRESULT GetAnalysisHints(
  [out] IContextNodes **ppAnalysisHints
);
```



## <a name="parameters"></a><span data-ttu-id="7fcad-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7fcad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcad-107">*ppAnalysisHints* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7fcad-107">*ppAnalysisHints* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fcad-108">Un puntero a todos los objetos [**IContextNode**](icontextnode.md) de la sugerencia de análisis en el [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-108">A pointer to all the analysis hint [**IContextNode**](icontextnode.md) objects in the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcad-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7fcad-109">Return value</span></span>

<span data-ttu-id="7fcad-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7fcad-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7fcad-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="7fcad-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppAnalysisHints* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="7fcad-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppAnalysisHints* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="7fcad-113">Este método devuelve una colección vacía si no hay ningún nodo de sugerencia de análisis asociado al [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-113">This method returns an empty collection if no analysis hint nodes are attached to the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

<span data-ttu-id="7fcad-114">Un nodo de sugerencia de análisis es un [**IContextNode**](icontextnode.md) con un tipo de nodo de contexto AnalysisHint (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [tipos de nodo de contexto](context-node-types.md)).</span><span class="sxs-lookup"><span data-stu-id="7fcad-114">An analysis hint node is an [**IContextNode**](icontextnode.md) with a context node type of AnalysisHint (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Context Node Types](context-node-types.md)).</span></span>

<span data-ttu-id="7fcad-115">Para agregar información de contexto a la sugerencia, use [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md) con el parámetro *pPropertyDataId* establecido en uno de los identificadores únicos globales (GUID) en las constantes de [las propiedades](analysis-hint-properties.md) de la sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="7fcad-115">To add context information to the hint, use [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md) with the *pPropertyDataId* parameter set to one of the globally unique identifiers (GUIDs) in the [Analysis Hint Properties](analysis-hint-properties.md) constants.</span></span>

<span data-ttu-id="7fcad-116">Para averiguar qué valores de propiedad se establecen en un nodo de contexto, use [**IContextNode:: GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-116">To find which property values are set on a context node, use [**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md).</span></span> <span data-ttu-id="7fcad-117">Para buscar el valor de una propiedad, use [**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md).</span><span class="sxs-lookup"><span data-stu-id="7fcad-117">To find the value of a property, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcad-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7fcad-118">Requirements</span></span>



| <span data-ttu-id="7fcad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fcad-119">Requirement</span></span> | <span data-ttu-id="7fcad-120">Value</span><span class="sxs-lookup"><span data-stu-id="7fcad-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcad-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fcad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7fcad-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7fcad-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7fcad-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7fcad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7fcad-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7fcad-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7fcad-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7fcad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fcad-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7fcad-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7fcad-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7fcad-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fcad-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fcad-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7fcad-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7fcad-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcad-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="7fcad-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="7fcad-131">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7fcad-131">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7fcad-132">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="7fcad-132">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="7fcad-133">**IInkAnalyzer::D método eleteAnalysisHint**</span><span class="sxs-lookup"><span data-stu-id="7fcad-133">**IInkAnalyzer::DeleteAnalysisHint Method**</span></span>](iinkanalyzer-deleteanalysishint.md)
</dt> <dt>

[<span data-ttu-id="7fcad-134">**IInkAnalyzer:: GetAnalysisHintsByName (método)**</span><span class="sxs-lookup"><span data-stu-id="7fcad-134">**IInkAnalyzer::GetAnalysisHintsByName Method**</span></span>](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[<span data-ttu-id="7fcad-135">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7fcad-135">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

