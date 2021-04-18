---
description: Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos IContextNode.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'IInkAnalyzer:: GetTextRangeFromNodes (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715204"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a><span data-ttu-id="a7383-103">IInkAnalyzer:: GetTextRangeFromNodes (método)</span><span class="sxs-lookup"><span data-stu-id="a7383-103">IInkAnalyzer::GetTextRangeFromNodes method</span></span>

<span data-ttu-id="a7383-104">Busca el intervalo de texto en la cadena reconocida que corresponde a una colección de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="a7383-104">Finds the text range in the recognized string that corresponds to a collection of [**IContextNode**](icontextnode.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7383-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7383-105">Syntax</span></span>


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a><span data-ttu-id="a7383-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7383-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7383-107">*plStart* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a7383-107">*plStart* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7383-108">Entero de 32 bits con signo que indica el inicio del intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="a7383-108">A 32-bit signed integer that indicates the start of the text range.</span></span> <span data-ttu-id="a7383-109">Este parámetro se pasa sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="a7383-109">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="a7383-110">*plLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a7383-110">*plLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7383-111">Entero de 32 bits con signo que indica la longitud del intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="a7383-111">A 32-bit signed integer that indicates the length of the text range.</span></span> <span data-ttu-id="a7383-112">Este parámetro se pasa sin inicializar.</span><span class="sxs-lookup"><span data-stu-id="a7383-112">This parameter is passed uninitialized.</span></span>

</dd> <dt>

<span data-ttu-id="a7383-113">*pNodesToSearch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7383-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7383-114">Colección de objetos [**IContextNode**](icontextnode.md) para los que se va a buscar el intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="a7383-114">The collection of [**IContextNode**](icontextnode.md) objects for which to find the text range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7383-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7383-115">Return value</span></span>

<span data-ttu-id="a7383-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a7383-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7383-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7383-117">Remarks</span></span>

<span data-ttu-id="a7383-118">Si *pNodesToSearch* contiene objetos [**IContextNode**](icontextnode.md) que no son adyacentes, este método devuelve el intervalo de texto más pequeño que abarca todos los objetos **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="a7383-118">If *pNodesToSearch* contains [**IContextNode**](icontextnode.md) objects that are not adjacent, this method returns the smallest text range that covers all of the **IContextNode** objects.</span></span>

<span data-ttu-id="a7383-119">Este método produce una excepción E \_ INVALIDARG cuando *pNodesToSearch* contiene un [**IContextNode**](icontextnode.md) que no está asociado a [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="a7383-119">This method throws an E\_INVALIDARG exception when *pNodesToSearch* contains an [**IContextNode**](icontextnode.md) that is not associated with the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a7383-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7383-120">Requirements</span></span>



| <span data-ttu-id="a7383-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7383-121">Requirement</span></span> | <span data-ttu-id="a7383-122">Value</span><span class="sxs-lookup"><span data-stu-id="a7383-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7383-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7383-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7383-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a7383-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7383-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7383-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7383-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a7383-126">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7383-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7383-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7383-128"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7383-128"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7383-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7383-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7383-130"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7383-130"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7383-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7383-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7383-132">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="a7383-132">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




