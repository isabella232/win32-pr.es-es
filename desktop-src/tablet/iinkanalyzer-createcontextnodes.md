---
description: Crea un objeto IContextNodes.
ms.assetid: d6d37595-307b-4cbc-9d48-ad10f8b272dd
title: 'IInkAnalyzer:: CreateContextNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateContextNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07bdfc9a32fd4aec8e716cdd3c788c211c1adaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715211"
---
# <a name="iinkanalyzercreatecontextnodes-method"></a><span data-ttu-id="f5196-103">IInkAnalyzer:: CreateContextNodes (método)</span><span class="sxs-lookup"><span data-stu-id="f5196-103">IInkAnalyzer::CreateContextNodes method</span></span>

<span data-ttu-id="f5196-104">Crea un objeto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="f5196-104">Creates an [**IContextNodes**](icontextnodes.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5196-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f5196-105">Syntax</span></span>


```C++
HRESULT CreateContextNodes(
  [out] IContextNodes **ppContextNodes
);
```



## <a name="parameters"></a><span data-ttu-id="f5196-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5196-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5196-107">*ppContextNodes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f5196-107">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5196-108">Puntero al objeto [**IContextNodes**](icontextnodes.md) .</span><span class="sxs-lookup"><span data-stu-id="f5196-108">A pointer to the [**IContextNodes**](icontextnodes.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5196-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5196-109">Return value</span></span>

<span data-ttu-id="f5196-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="f5196-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5196-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5196-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="f5196-112">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en *ppContextNodes* cuando ya no necesite usar el objeto.</span><span class="sxs-lookup"><span data-stu-id="f5196-112">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on *ppContextNodes* when you no longer need to use the object.</span></span>

 

<span data-ttu-id="f5196-113">Use este método para crear una colección [**IContextNodes**](icontextnodes.md) vacía que esté asociada a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f5196-113">Use this method to create an empty [**IContextNodes**](icontextnodes.md) collection that is associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="f5196-114">La nueva colección **IContextNodes** no forma parte del árbol de contexto del objeto **IInkAnalyzer** .</span><span class="sxs-lookup"><span data-stu-id="f5196-114">The new **IContextNodes** collection is not part of the **IInkAnalyzer** object's context tree.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5196-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5196-115">Requirements</span></span>



| <span data-ttu-id="f5196-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5196-116">Requirement</span></span> | <span data-ttu-id="f5196-117">Value</span><span class="sxs-lookup"><span data-stu-id="f5196-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5196-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5196-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f5196-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f5196-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f5196-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5196-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f5196-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f5196-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="f5196-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5196-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5196-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f5196-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f5196-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f5196-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5196-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5196-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="f5196-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5196-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5196-127">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="f5196-127">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="f5196-128">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="f5196-128">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="f5196-129">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="f5196-129">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

