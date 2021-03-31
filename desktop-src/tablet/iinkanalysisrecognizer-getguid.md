---
description: Recupera el identificador único global (GUID) del reconocedor.
ms.assetid: 9b98993b-eaf3-4207-9d56-33efeceb75cf
title: 'IInkAnalysisRecognizer:: GetGuid (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetGuid
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9a027a405829e6d1237a8ec90dd59fcc8905006d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908021"
---
# <a name="iinkanalysisrecognizergetguid-method"></a><span data-ttu-id="d27f2-103">IInkAnalysisRecognizer:: GetGuid (método)</span><span class="sxs-lookup"><span data-stu-id="d27f2-103">IInkAnalysisRecognizer::GetGuid method</span></span>

<span data-ttu-id="d27f2-104">Recupera el identificador único global (GUID) del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="d27f2-104">Retrieves the globally unique identifier (GUID) of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d27f2-105">Syntax</span></span>


```C++
HRESULT GetGuid(
  [out] GUID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="d27f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d27f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27f2-107">*pId* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d27f2-107">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d27f2-108">GUID que identifica este [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="d27f2-108">The GUID that identifies this [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d27f2-109">Return value</span></span>

<span data-ttu-id="d27f2-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="d27f2-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d27f2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d27f2-111">Requirements</span></span>



| <span data-ttu-id="d27f2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d27f2-112">Requirement</span></span> | <span data-ttu-id="d27f2-113">Value</span><span class="sxs-lookup"><span data-stu-id="d27f2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27f2-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d27f2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d27f2-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d27f2-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d27f2-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d27f2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d27f2-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d27f2-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d27f2-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d27f2-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d27f2-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d27f2-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d27f2-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d27f2-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d27f2-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d27f2-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d27f2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d27f2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27f2-123">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="d27f2-123">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="d27f2-124">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="d27f2-124">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




