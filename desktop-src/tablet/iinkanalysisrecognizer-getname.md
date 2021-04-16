---
description: Recupera el nombre del reconocedor.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'IInkAnalysisRecognizer:: GetName (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666499"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="63ef8-103">IInkAnalysisRecognizer:: GetName (método)</span><span class="sxs-lookup"><span data-stu-id="63ef8-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="63ef8-104">Recupera el nombre del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="63ef8-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ef8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63ef8-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="63ef8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63ef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63ef8-107">*pbstrName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63ef8-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63ef8-108">Nombre del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="63ef8-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63ef8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63ef8-109">Return value</span></span>

<span data-ttu-id="63ef8-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="63ef8-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="63ef8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63ef8-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="63ef8-112">Para evitar una pérdida de memoria, llame a [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) en \* *pbstrName* cuando ya no necesite usar la cadena.</span><span class="sxs-lookup"><span data-stu-id="63ef8-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="63ef8-113">El nombre se localiza para el idioma independiente de la región que admite el reconocedor.</span><span class="sxs-lookup"><span data-stu-id="63ef8-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="63ef8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ef8-114">Requirements</span></span>



| <span data-ttu-id="63ef8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ef8-115">Requirement</span></span> | <span data-ttu-id="63ef8-116">Value</span><span class="sxs-lookup"><span data-stu-id="63ef8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ef8-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ef8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63ef8-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="63ef8-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="63ef8-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ef8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63ef8-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63ef8-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="63ef8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63ef8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="63ef8-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="63ef8-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="63ef8-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63ef8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63ef8-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63ef8-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="63ef8-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ef8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ef8-126">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="63ef8-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="63ef8-127">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="63ef8-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

