---
description: Borra los datos de los paquetes de trazos de IInkAnalyzer.
ms.assetid: c87a1e73-5e3f-4d27-93e9-e30d9ec5d9e3
title: 'IInkAnalyzer:: ClearStrokeData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ClearStrokeData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 823ceaa825b454af851fab43e233526285445c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497566"
---
# <a name="iinkanalyzerclearstrokedata-method"></a><span data-ttu-id="49a42-103">IInkAnalyzer:: ClearStrokeData (método)</span><span class="sxs-lookup"><span data-stu-id="49a42-103">IInkAnalyzer::ClearStrokeData method</span></span>

<span data-ttu-id="49a42-104">Borra los datos de los paquetes de trazos de [**IInkAnalyzer**](iinkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="49a42-104">Clears stroke packet data from the [**IInkAnalyzer**](iinkanalyzer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="49a42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49a42-105">Syntax</span></span>


```C++
HRESULT ClearStrokeData(
  [in] LONG lStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="49a42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="49a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a42-107">*lStrokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="49a42-107">*lStrokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a42-108">Identificador del trazo para el que se borran los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="49a42-108">The identifier of the stroke for which the packet data is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a42-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="49a42-109">Return value</span></span>

<span data-ttu-id="49a42-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="49a42-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="49a42-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="49a42-111">Remarks</span></span>

<span data-ttu-id="49a42-112">Use este método cuando los datos de paquetes de un trazo cambien, por ejemplo, cuando un trazo se mueve o se transforma de otro modo.</span><span class="sxs-lookup"><span data-stu-id="49a42-112">Use this method when packet data for a stroke changes, such as when a stroke is moved or otherwise transformed.</span></span> <span data-ttu-id="49a42-113">[**IInkAnalyzer**](iinkanalyzer.md) genera el evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) cuando necesita datos de paquetes de trazos de un trazo para el que se han borrado los datos del paquete.</span><span class="sxs-lookup"><span data-stu-id="49a42-113">The [**IInkAnalyzer**](iinkanalyzer.md) raises the [**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) event when it needs stroke packet data from a stroke for which the packet data has been cleared.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a42-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49a42-114">Requirements</span></span>



| <span data-ttu-id="49a42-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="49a42-115">Requirement</span></span> | <span data-ttu-id="49a42-116">Value</span><span class="sxs-lookup"><span data-stu-id="49a42-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a42-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49a42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49a42-118">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="49a42-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="49a42-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49a42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49a42-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="49a42-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="49a42-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="49a42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a42-122"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="49a42-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="49a42-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49a42-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49a42-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49a42-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="49a42-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="49a42-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a42-126">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="49a42-126">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="49a42-127">**IInkAnalyzer:: UpdateStrokesData (método)**</span><span class="sxs-lookup"><span data-stu-id="49a42-127">**IInkAnalyzer::UpdateStrokesData Method**</span></span>](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[<span data-ttu-id="49a42-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="49a42-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




