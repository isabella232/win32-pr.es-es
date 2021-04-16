---
description: Obtiene el valor de cadena reconocido del objeto IAnalysisAlternate.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'IAnalysisAlternate:: GetRecognizedString (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542118"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a><span data-ttu-id="c84cd-103">IAnalysisAlternate:: GetRecognizedString (método)</span><span class="sxs-lookup"><span data-stu-id="c84cd-103">IAnalysisAlternate::GetRecognizedString method</span></span>

<span data-ttu-id="c84cd-104">Obtiene el valor de cadena reconocido del objeto [**IAnalysisAlternate**](ianalysisalternate.md) .</span><span class="sxs-lookup"><span data-stu-id="c84cd-104">Gets the recognized string value of the [**IAnalysisAlternate**](ianalysisalternate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84cd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c84cd-105">Syntax</span></span>


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a><span data-ttu-id="c84cd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c84cd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84cd-107">*pbstrRecognizedString* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c84cd-107">*pbstrRecognizedString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c84cd-108">Puntero al **BSTR** que se establece en el valor de cadena reconocido.</span><span class="sxs-lookup"><span data-stu-id="c84cd-108">A pointer to the **BSTR** that is set to the recognized string value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84cd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c84cd-109">Return value</span></span>

<span data-ttu-id="c84cd-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c84cd-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c84cd-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84cd-111">Requirements</span></span>



| <span data-ttu-id="c84cd-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84cd-112">Requirement</span></span> | <span data-ttu-id="c84cd-113">Value</span><span class="sxs-lookup"><span data-stu-id="c84cd-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84cd-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84cd-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c84cd-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c84cd-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c84cd-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c84cd-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c84cd-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c84cd-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c84cd-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c84cd-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84cd-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c84cd-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c84cd-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c84cd-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c84cd-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c84cd-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c84cd-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="c84cd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84cd-123">**IAnalysisAlternate**</span><span class="sxs-lookup"><span data-stu-id="c84cd-123">**IAnalysisAlternate**</span></span>](ianalysisalternate.md)
</dt> <dt>

[<span data-ttu-id="c84cd-124">**IInkAnalyzer:: GetRecognizedString (método)**</span><span class="sxs-lookup"><span data-stu-id="c84cd-124">**IInkAnalyzer::GetRecognizedString Method**</span></span>](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




