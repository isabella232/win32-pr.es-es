---
description: Recupera el valor que indica si un objeto IContextNode se rellena parcialmente o está totalmente rellenado.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'IContextNode:: GetPartiallyPopulated (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154438"
---
# <a name="icontextnodegetpartiallypopulated-method"></a><span data-ttu-id="ffa6a-103">IContextNode:: GetPartiallyPopulated (método)</span><span class="sxs-lookup"><span data-stu-id="ffa6a-103">IContextNode::GetPartiallyPopulated method</span></span>

<span data-ttu-id="ffa6a-104">Recupera el valor que indica si un objeto [**IContextNode**](icontextnode.md) se rellena parcialmente o está totalmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="ffa6a-104">Retrieves the value that indicates whether an [**IContextNode**](icontextnode.md) object is partially populated or fully populated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa6a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffa6a-105">Syntax</span></span>


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a><span data-ttu-id="ffa6a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ffa6a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa6a-107">*pfPartiallyPopulated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ffa6a-107">*pfPartiallyPopulated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffa6a-108">**Variante \_ TRUE** si este objeto [**IContextNode**](icontextnode.md) no contiene datos completos; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="ffa6a-108">**VARIANT\_TRUE** if this [**IContextNode**](icontextnode.md) object does not contain complete data; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffa6a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffa6a-109">Return value</span></span>

<span data-ttu-id="ffa6a-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ffa6a-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffa6a-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffa6a-111">Remarks</span></span>

<span data-ttu-id="ffa6a-112">Use este método cuando la aplicación mantenga su propia estructura de datos, que está sincronizada con la de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="ffa6a-112">Use this method when your application maintains its own data structure, which is synchronized with that of the [**IInkAnalyzer**](iinkanalyzer.md).</span></span> <span data-ttu-id="ffa6a-113">Para obtener más información, consulte [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="ffa6a-113">For more information, see [Data Proxy with Ink Analysis](data-proxy-with-ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffa6a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffa6a-114">Requirements</span></span>



| <span data-ttu-id="ffa6a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffa6a-115">Requirement</span></span> | <span data-ttu-id="ffa6a-116">Value</span><span class="sxs-lookup"><span data-stu-id="ffa6a-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa6a-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffa6a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa6a-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ffa6a-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ffa6a-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffa6a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa6a-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ffa6a-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="ffa6a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ffa6a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa6a-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ffa6a-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ffa6a-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffa6a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffa6a-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffa6a-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="ffa6a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffa6a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa6a-126">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="ffa6a-126">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="ffa6a-127">**IContextNode::SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="ffa6a-127">**IContextNode::SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[<span data-ttu-id="ffa6a-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="ffa6a-128">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="ffa6a-129">**\_IAnalysisProxyEvents::P opulateContextNode**</span><span class="sxs-lookup"><span data-stu-id="ffa6a-129">**\_IAnalysisProxyEvents::PopulateContextNode**</span></span>](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[<span data-ttu-id="ffa6a-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="ffa6a-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




