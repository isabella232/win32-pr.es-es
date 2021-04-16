---
description: Recupera la región del documento correspondiente a los cambios que se realizaron en el árbol de nodos de contexto del objeto IInkAnalyzer como resultado del análisis de tinta.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus:: GetAppliedChangesRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542086"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a><span data-ttu-id="55bbc-103">IAnalysisStatus:: GetAppliedChangesRegion (método)</span><span class="sxs-lookup"><span data-stu-id="55bbc-103">IAnalysisStatus::GetAppliedChangesRegion method</span></span>

<span data-ttu-id="55bbc-104">Recupera la región del documento correspondiente a los cambios que se realizaron en el árbol de nodos de contexto del objeto [**IInkAnalyzer**](iinkanalyzer.md) como resultado del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="55bbc-104">Retrieves the region of the document that corresponds to changes that were made in the [**IInkAnalyzer**](iinkanalyzer.md) object's context node tree as a result of ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bbc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55bbc-105">Syntax</span></span>


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a><span data-ttu-id="55bbc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55bbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55bbc-107">*pAppliedChangesRegion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55bbc-107">*pAppliedChangesRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55bbc-108">Puntero al [**IAnalysisRegion**](ianalysisregion.md) del documento en el que se realizaron los cambios.</span><span class="sxs-lookup"><span data-stu-id="55bbc-108">A pointer to the [**IAnalysisRegion**](ianalysisregion.md) of the document where changes were made.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55bbc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55bbc-109">Return value</span></span>

<span data-ttu-id="55bbc-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="55bbc-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="55bbc-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55bbc-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="55bbc-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pAppliedChangesRegion* cuando ya no necesite usar la región de análisis.</span><span class="sxs-lookup"><span data-stu-id="55bbc-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pAppliedChangesRegion* when you no longer need to use the analysis region.</span></span>

 

<span data-ttu-id="55bbc-113">Este método se usa con más frecuencia cuando la aplicación recibe información con fines de depuración y necesita invalidar el área en la que se pueden producir cambios para que se dibuje la información de depuración.</span><span class="sxs-lookup"><span data-stu-id="55bbc-113">This method is most frequently used when the application receives information for debugging purposes and needs to invalidate the area where changes might occur so that the debugging information is painted.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bbc-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55bbc-114">Requirements</span></span>



| <span data-ttu-id="55bbc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bbc-115">Requirement</span></span> | <span data-ttu-id="55bbc-116">Value</span><span class="sxs-lookup"><span data-stu-id="55bbc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55bbc-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55bbc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="55bbc-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="55bbc-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="55bbc-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55bbc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="55bbc-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55bbc-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="55bbc-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55bbc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="55bbc-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="55bbc-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="55bbc-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55bbc-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55bbc-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55bbc-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="55bbc-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="55bbc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bbc-126">**IAnalysisStatus**</span><span class="sxs-lookup"><span data-stu-id="55bbc-126">**IAnalysisStatus**</span></span>](ianalysisstatus.md)
</dt> <dt>

[<span data-ttu-id="55bbc-127">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="55bbc-127">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="55bbc-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="55bbc-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

