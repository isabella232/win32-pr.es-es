---
description: Determina si el IAnalysisRegion especificado contiene el mismo valor que el objeto IAnalysisRegion actual.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion:: EqualsRegion (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154449"
---
# <a name="ianalysisregionequalsregion-method"></a><span data-ttu-id="43b4e-103">IAnalysisRegion:: EqualsRegion (método)</span><span class="sxs-lookup"><span data-stu-id="43b4e-103">IAnalysisRegion::EqualsRegion method</span></span>

<span data-ttu-id="43b4e-104">Determina si el [**IAnalysisRegion**](ianalysisregion.md) especificado contiene el mismo valor que el objeto **IAnalysisRegion** actual.</span><span class="sxs-lookup"><span data-stu-id="43b4e-104">Determines whether the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current **IAnalysisRegion** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b4e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43b4e-105">Syntax</span></span>


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a><span data-ttu-id="43b4e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43b4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b4e-107">*pOtherRegion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-107">*pOtherRegion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43b4e-108">Objeto [**IAnalysisRegion**](ianalysisregion.md) que se va a comparar con el **IAnalysisRegion** actual.</span><span class="sxs-lookup"><span data-stu-id="43b4e-108">The [**IAnalysisRegion**](ianalysisregion.md) object to compare with the current **IAnalysisRegion**.</span></span>

</dd> <dt>

<span data-ttu-id="43b4e-109">*pfRegionsEqual* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-109">*pfRegionsEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43b4e-110">**Variante \_ TRUE** si el [**IAnalysisRegion**](ianalysisregion.md) especificado contiene el mismo valor que el IAnalysisRegion actual; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="43b4e-110">**VARIANT\_TRUE** if the specified [**IAnalysisRegion**](ianalysisregion.md) contains the same value as the current IAnalysisRegion; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b4e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43b4e-111">Return value</span></span>

<span data-ttu-id="43b4e-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="43b4e-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="43b4e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43b4e-113">Requirements</span></span>



| <span data-ttu-id="43b4e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="43b4e-114">Requirement</span></span> | <span data-ttu-id="43b4e-115">Value</span><span class="sxs-lookup"><span data-stu-id="43b4e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43b4e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43b4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="43b4e-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="43b4e-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="43b4e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="43b4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="43b4e-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="43b4e-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="43b4e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43b4e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="43b4e-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="43b4e-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="43b4e-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="43b4e-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43b4e-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43b4e-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="43b4e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="43b4e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43b4e-125">**IAnalysisRegion**</span><span class="sxs-lookup"><span data-stu-id="43b4e-125">**IAnalysisRegion**</span></span>](ianalysisregion.md)
</dt> </dl>

 

 




