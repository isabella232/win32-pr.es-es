---
description: Recupera una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'IInkAnalysisRecognizer:: GetUnicodeRanges (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908019"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a><span data-ttu-id="5ea75-103">IInkAnalysisRecognizer:: GetUnicodeRanges (método)</span><span class="sxs-lookup"><span data-stu-id="5ea75-103">IInkAnalysisRecognizer::GetUnicodeRanges method</span></span>

<span data-ttu-id="5ea75-104">Recupera una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.</span><span class="sxs-lookup"><span data-stu-id="5ea75-104">Retrieves an array of character ranges representing the supported Unicode character ranges.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea75-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ea75-105">Syntax</span></span>


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a><span data-ttu-id="5ea75-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ea75-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea75-107">*pulNumberOfRanges* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5ea75-107">*pulNumberOfRanges* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea75-108">El número de intervalos de caracteres a los que apunta *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="5ea75-108">The number of character ranges pointed to by *ppulLowUnicode*.</span></span>

</dd> <dt>

<span data-ttu-id="5ea75-109">*ppulLowUnicode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ea75-109">*ppulLowUnicode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea75-110">Puntero a una matriz de intervalos de caracteres que representan los intervalos de caracteres Unicode admitidos.</span><span class="sxs-lookup"><span data-stu-id="5ea75-110">Pointer to an array of character ranges representing the supported Unicode character ranges.</span></span>

</dd> <dt>

<span data-ttu-id="5ea75-111">*ppusUnicodeRangeLength* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5ea75-111">*ppusUnicodeRangeLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea75-112">Puntero a una matriz de valores que indica la longitud de cada matriz que apunta a *ppulLowUnicode*.</span><span class="sxs-lookup"><span data-stu-id="5ea75-112">Pointer to an array of values indicating the length of each array point to by *ppulLowUnicode*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea75-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ea75-113">Return value</span></span>

<span data-ttu-id="5ea75-114">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5ea75-114">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea75-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ea75-115">Requirements</span></span>



| <span data-ttu-id="5ea75-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ea75-116">Requirement</span></span> | <span data-ttu-id="5ea75-117">Value</span><span class="sxs-lookup"><span data-stu-id="5ea75-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea75-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea75-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea75-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ea75-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5ea75-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ea75-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea75-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ea75-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5ea75-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ea75-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea75-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ea75-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ea75-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ea75-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ea75-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea75-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5ea75-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ea75-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea75-127">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="5ea75-127">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




