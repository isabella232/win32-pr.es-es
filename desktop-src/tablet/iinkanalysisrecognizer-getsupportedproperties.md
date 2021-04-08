---
description: Recupera los identificadores únicos globales (GUID) de las propiedades que este IInkAnalysisRecognizer puede generar para los resultados del análisis.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'IInkAnalysisRecognizer:: GetSupportedProperties (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001186"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a><span data-ttu-id="abd82-103">IInkAnalysisRecognizer:: GetSupportedProperties (método)</span><span class="sxs-lookup"><span data-stu-id="abd82-103">IInkAnalysisRecognizer::GetSupportedProperties method</span></span>

<span data-ttu-id="abd82-104">Recupera los identificadores únicos globales (GUID) de las propiedades que este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="abd82-104">Retrieves the globally unique identifiers (GUIDs) for the properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd82-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abd82-105">Syntax</span></span>


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a><span data-ttu-id="abd82-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="abd82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd82-107">*pulPropertiesCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="abd82-107">*pulPropertiesCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd82-108">Número de GUID de *ppProperties*.</span><span class="sxs-lookup"><span data-stu-id="abd82-108">The number of GUIDs in *ppProperties*.</span></span>

</dd> <dt>

<span data-ttu-id="abd82-109">*ppProperties* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="abd82-109">*ppProperties* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd82-110">Puntero a los GUID de las propiedades que este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) puede generar para los resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="abd82-110">A pointer to the GUIDs of properties that this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) can generate for analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd82-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="abd82-111">Return value</span></span>

<span data-ttu-id="abd82-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="abd82-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abd82-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="abd82-113">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="abd82-114">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppProperties* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="abd82-114">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppProperties* when you no longer need the information.</span></span>

 

<span data-ttu-id="abd82-115">Un reconocedor puede admitir las métricas de línea, los números de línea, los niveles de confianza, etc.</span><span class="sxs-lookup"><span data-stu-id="abd82-115">A recognizer can support line metrics, line numbers, confidence levels, and so on.</span></span> <span data-ttu-id="abd82-116">Para obtener una lista completa de las propiedades que puede admitir un reconocedor, vea [constantes RecognitionProperty](recognitionproperty-constants.md).</span><span class="sxs-lookup"><span data-stu-id="abd82-116">For a complete list of the properties that a recognizer can support, see [RecognitionProperty Constants](recognitionproperty-constants.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd82-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abd82-117">Requirements</span></span>



| <span data-ttu-id="abd82-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="abd82-118">Requirement</span></span> | <span data-ttu-id="abd82-119">Value</span><span class="sxs-lookup"><span data-stu-id="abd82-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd82-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd82-120">Minimum supported client</span></span><br/> | <span data-ttu-id="abd82-121">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="abd82-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="abd82-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abd82-122">Minimum supported server</span></span><br/> | <span data-ttu-id="abd82-123">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="abd82-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="abd82-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="abd82-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd82-125"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="abd82-125"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="abd82-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abd82-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd82-127"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd82-127"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="abd82-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="abd82-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd82-129">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="abd82-129">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="abd82-130">Constantes de RecognitionProperty</span><span class="sxs-lookup"><span data-stu-id="abd82-130">RecognitionProperty Constants</span></span>](recognitionproperty-constants.md)
</dt> <dt>

[<span data-ttu-id="abd82-131">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="abd82-131">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

