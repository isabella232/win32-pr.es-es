---
description: Crea una copia de IAnalysisRegion.
ms.assetid: eb94e1ce-7801-409d-9ae6-e7db0a9b861f
title: 'IAnalysisRegion:: Clone (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.Clone
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fb069ddb461ab4422f8cbbc8990fb6d735808e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696549"
---
# <a name="ianalysisregionclone-method"></a><span data-ttu-id="c4112-103">IAnalysisRegion:: Clone (método)</span><span class="sxs-lookup"><span data-stu-id="c4112-103">IAnalysisRegion::Clone method</span></span>

<span data-ttu-id="c4112-104">Crea una copia de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="c4112-104">Creates a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4112-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4112-105">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IAnalysisRegion **pClonedRegion
);
```



## <a name="parameters"></a><span data-ttu-id="c4112-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4112-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4112-107">*pClonedRegion* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4112-107">*pClonedRegion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4112-108">Puntero a una copia de [**IAnalysisRegion**](ianalysisregion.md).</span><span class="sxs-lookup"><span data-stu-id="c4112-108">A pointer to a copy of the [**IAnalysisRegion**](ianalysisregion.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4112-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4112-109">Return value</span></span>

<span data-ttu-id="c4112-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c4112-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c4112-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4112-111">Remarks</span></span>

<span data-ttu-id="c4112-112">Este método se eqivalent al método System. Windows. Ink. AnalysisCore. AnalysisRegionBase. Clone en el .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c4112-112">This method is eqivalent to theSystem.Windows.Ink.AnalysisCore.AnalysisRegionBase.Clone Method in the .NET Framework.</span></span>

> [!Caution]  
> <span data-ttu-id="c4112-113">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *pClonedRegion* cuando ya no necesite usar la región de análisis clonada.</span><span class="sxs-lookup"><span data-stu-id="c4112-113">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**pClonedRegion* when you no longer need to use the cloned analysis region.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c4112-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4112-114">Requirements</span></span>



| <span data-ttu-id="c4112-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4112-115">Requirement</span></span> | <span data-ttu-id="c4112-116">Value</span><span class="sxs-lookup"><span data-stu-id="c4112-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4112-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4112-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c4112-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c4112-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c4112-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4112-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c4112-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c4112-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c4112-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4112-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4112-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4112-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4112-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4112-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4112-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4112-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c4112-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4112-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4112-126">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="c4112-126">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> <dt>

[<span data-ttu-id="c4112-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c4112-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

