---
description: Recupera el tipo del trazo especificado.
ms.assetid: bbd0bc23-89f9-4033-bc32-f9bd737c960c
title: 'IInkAnalyzer:: GetStrokeType (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d9358b2583f31fd26310ea880470f36404021fec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275465"
---
# <a name="iinkanalyzergetstroketype-method"></a><span data-ttu-id="5aad9-103">IInkAnalyzer:: GetStrokeType (método)</span><span class="sxs-lookup"><span data-stu-id="5aad9-103">IInkAnalyzer::GetStrokeType method</span></span>

<span data-ttu-id="5aad9-104">Recupera el tipo del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="5aad9-104">Retrieves the type of the specified stroke.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aad9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aad9-105">Syntax</span></span>


```C++
HRESULT GetStrokeType(
  [in]  LONG       lStrokeId,
  [out] StrokeType *pStrokeType
);
```



## <a name="parameters"></a><span data-ttu-id="5aad9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aad9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aad9-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5aad9-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad9-108">Identificador del trazo.</span><span class="sxs-lookup"><span data-stu-id="5aad9-108">The stroke identifier.</span></span>

</dd> <dt>

<span data-ttu-id="5aad9-109">*pStrokeType* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5aad9-109">*pStrokeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5aad9-110">La clasificación del trazo especificado.</span><span class="sxs-lookup"><span data-stu-id="5aad9-110">The classification of the specified stroke.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aad9-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aad9-111">Return value</span></span>

<span data-ttu-id="5aad9-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="5aad9-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5aad9-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aad9-113">Remarks</span></span>

<span data-ttu-id="5aad9-114">Si el tipo del trazo es el valor de [**StrokeType**](stroketype.md) StrokeType sin \_ clasificar, el [**IInkAnalyzer**](iinkanalyzer.md) clasifica el trazo durante el análisis de la tinta.</span><span class="sxs-lookup"><span data-stu-id="5aad9-114">If the stroke's type is the [**StrokeType**](stroketype.md) value StrokeType\_Unclassified, the [**IInkAnalyzer**](iinkanalyzer.md) classifies the stroke during ink analysis.</span></span> <span data-ttu-id="5aad9-115">De lo contrario, **IInkAnalyzer** usa el tipo establecido en el trazo.</span><span class="sxs-lookup"><span data-stu-id="5aad9-115">Otherwise, the **IInkAnalyzer** uses the type set on the stroke.</span></span>

<span data-ttu-id="5aad9-116">[**IInkAnalyzer**](iinkanalyzer.md) no establece el valor de tipo de trazo como parte del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="5aad9-116">The [**IInkAnalyzer**](iinkanalyzer.md) does not set the stroke type value as part of ink analysis.</span></span> <span data-ttu-id="5aad9-117">Para especificar o cambiar el tipo de trazo, use el método [**IInkAnalyzer:: SetStrokeType**](iinkanalyzer-setstroketype.md) o [**IInkAnalyzer:: SetStrokesType**](iinkanalyzer-setstrokestype.md).</span><span class="sxs-lookup"><span data-stu-id="5aad9-117">To specify or change the stroke type, use [**IInkAnalyzer::SetStrokeType Method**](iinkanalyzer-setstroketype.md) or [**IInkAnalyzer::SetStrokesType Method**](iinkanalyzer-setstrokestype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aad9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aad9-118">Requirements</span></span>



| <span data-ttu-id="5aad9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aad9-119">Requirement</span></span> | <span data-ttu-id="5aad9-120">Value</span><span class="sxs-lookup"><span data-stu-id="5aad9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aad9-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aad9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5aad9-122">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5aad9-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5aad9-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aad9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5aad9-124">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5aad9-124">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5aad9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5aad9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5aad9-126"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5aad9-126"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5aad9-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aad9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aad9-128"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aad9-128"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5aad9-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aad9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aad9-130">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="5aad9-130">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="5aad9-131">**IInkAnalyzer:: SetStrokeType (método)**</span><span class="sxs-lookup"><span data-stu-id="5aad9-131">**IInkAnalyzer::SetStrokeType Method**</span></span>](iinkanalyzer-setstroketype.md)
</dt> <dt>

[<span data-ttu-id="5aad9-132">**IInkAnalyzer:: SetStrokesType (método)**</span><span class="sxs-lookup"><span data-stu-id="5aad9-132">**IInkAnalyzer::SetStrokesType Method**</span></span>](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[<span data-ttu-id="5aad9-133">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5aad9-133">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




