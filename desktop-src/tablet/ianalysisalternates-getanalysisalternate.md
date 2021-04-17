---
description: Recupera el objeto IAnalysisAlternate en el índice especificado de la colección.
ms.assetid: d927e2f1-ca21-415d-90ad-d1ded575fcb7
title: 'IAnalysisAlternates:: GetAnalysisAlternate (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates.GetAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 122bccc4985ed7ba5617e9d373ecdf3d0c84dac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696551"
---
# <a name="ianalysisalternatesgetanalysisalternate-method"></a><span data-ttu-id="a7484-103">IAnalysisAlternates:: GetAnalysisAlternate (método)</span><span class="sxs-lookup"><span data-stu-id="a7484-103">IAnalysisAlternates::GetAnalysisAlternate method</span></span>

<span data-ttu-id="a7484-104">Recupera el objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="a7484-104">Retrieves the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7484-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7484-105">Syntax</span></span>


```C++
HRESULT GetAnalysisAlternate(
  [in]  ULONG              ulIndex,
  [out] IAnalysisAlternate **ppAlternate
);
```



## <a name="parameters"></a><span data-ttu-id="a7484-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7484-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7484-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a7484-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7484-108">Índice de base cero del objeto [**IAnalysisAlternate**](ianalysisalternate.md) que se va a obtener.</span><span class="sxs-lookup"><span data-stu-id="a7484-108">The zero-based index of the [**IAnalysisAlternate**](ianalysisalternate.md) object to get.</span></span>

</dd> <dt>

<span data-ttu-id="a7484-109">*ppAlternate* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a7484-109">*ppAlternate* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7484-110">Puntero al objeto [**IAnalysisAlternate**](ianalysisalternate.md) en el índice especificado de la colección.</span><span class="sxs-lookup"><span data-stu-id="a7484-110">A pointer to the [**IAnalysisAlternate**](ianalysisalternate.md) object at the specified index within the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7484-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7484-111">Return value</span></span>

<span data-ttu-id="a7484-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a7484-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7484-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a7484-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="a7484-114">Para evitar una pérdida de memoria, llame a [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) en \* *ppAlternate* cuando ya no necesite usar la alternativa de análisis.</span><span class="sxs-lookup"><span data-stu-id="a7484-114">To avoid a memory leak, call [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on \**ppAlternate* when you no longer need to use the analysis alternate.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a7484-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7484-115">Requirements</span></span>



| <span data-ttu-id="a7484-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7484-116">Requirement</span></span> | <span data-ttu-id="a7484-117">Value</span><span class="sxs-lookup"><span data-stu-id="a7484-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7484-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7484-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a7484-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="a7484-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a7484-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a7484-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a7484-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a7484-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a7484-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7484-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7484-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a7484-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a7484-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a7484-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7484-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7484-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a7484-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7484-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7484-127">**IAnalysisAlternates**</span><span class="sxs-lookup"><span data-stu-id="a7484-127">**IAnalysisAlternates**</span></span>](ianalysisalternates.md)
</dt> <dt>

[<span data-ttu-id="a7484-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="a7484-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

