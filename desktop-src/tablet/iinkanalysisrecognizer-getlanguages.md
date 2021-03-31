---
description: Recupera los identificadores de las configuraciones regionales admitidas por este IInkAnalysisRecognizer.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'IInkAnalysisRecognizer:: GetLanguages (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908020"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a><span data-ttu-id="c8f3d-103">IInkAnalysisRecognizer:: GetLanguages (método)</span><span class="sxs-lookup"><span data-stu-id="c8f3d-103">IInkAnalysisRecognizer::GetLanguages method</span></span>

<span data-ttu-id="c8f3d-104">Recupera los identificadores de las configuraciones regionales admitidas por este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f3d-104">Retrieves the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f3d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8f3d-105">Syntax</span></span>


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a><span data-ttu-id="c8f3d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8f3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8f3d-107">*pulLanguagesCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c8f3d-107">*pulLanguagesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f3d-108">Número de identificadores de *ppulLanguages*.</span><span class="sxs-lookup"><span data-stu-id="c8f3d-108">The number of identifiers in *ppulLanguages*.</span></span>

</dd> <dt>

<span data-ttu-id="c8f3d-109">*ppulLanguages* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8f3d-109">*ppulLanguages* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8f3d-110">Puntero a los identificadores de las configuraciones regionales admitidas por este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f3d-110">A pointer to the identifiers for the locales that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8f3d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8f3d-111">Return value</span></span>

<span data-ttu-id="c8f3d-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c8f3d-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8f3d-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8f3d-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="c8f3d-114">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppulLanguages* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="c8f3d-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppulLanguages* when you no longer need the information.</span></span>

 

<span data-ttu-id="c8f3d-115">Este método devuelve una matriz vacía para los reconocedores de objetos y gestos.</span><span class="sxs-lookup"><span data-stu-id="c8f3d-115">This method returns an empty array for object and gesture recognizers.</span></span>

<span data-ttu-id="c8f3d-116">Para obtener más información sobre los identificadores de idioma, vea [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).</span><span class="sxs-lookup"><span data-stu-id="c8f3d-116">For more information about language identifiers, see [Language Identifier Constants and Strings](/windows/desktop/Intl/language-identifier-constants-and-strings).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8f3d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f3d-117">Requirements</span></span>



| <span data-ttu-id="c8f3d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f3d-118">Requirement</span></span> | <span data-ttu-id="c8f3d-119">Value</span><span class="sxs-lookup"><span data-stu-id="c8f3d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f3d-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8f3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c8f3d-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c8f3d-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c8f3d-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8f3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c8f3d-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8f3d-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c8f3d-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8f3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8f3d-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f3d-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c8f3d-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8f3d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8f3d-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8f3d-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c8f3d-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8f3d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f3d-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="c8f3d-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="c8f3d-130">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="c8f3d-130">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

