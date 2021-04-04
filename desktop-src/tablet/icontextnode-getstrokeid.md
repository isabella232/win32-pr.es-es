---
description: Recupera el identificador de trazo para el trazo al que hace referencia un valor de índice dentro del objeto IContextNode.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'IContextNode:: GetStrokeId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810033"
---
# <a name="icontextnodegetstrokeid-method"></a><span data-ttu-id="7cfce-103">IContextNode:: GetStrokeId (método)</span><span class="sxs-lookup"><span data-stu-id="7cfce-103">IContextNode::GetStrokeId method</span></span>

<span data-ttu-id="7cfce-104">Recupera el identificador de trazo para el trazo al que hace referencia un valor de índice dentro del objeto [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="7cfce-104">Retrieves the stroke identifier for the stroke referenced by an index value within the [**IContextNode**](icontextnode.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cfce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7cfce-105">Syntax</span></span>


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a><span data-ttu-id="7cfce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7cfce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cfce-107">*ulIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7cfce-107">*ulIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfce-108">Índice del trazo que se va a devolver.</span><span class="sxs-lookup"><span data-stu-id="7cfce-108">The index of the stroke to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="7cfce-109">*plStrokeId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7cfce-109">*plStrokeId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7cfce-110">Identificador de trazo del trazo al que hace referencia el parámetro *ulIndex* dentro del objeto [**IContextNode**](icontextnode.md) actual.</span><span class="sxs-lookup"><span data-stu-id="7cfce-110">The stroke identifier for the stroke referenced by the *ulIndex* parameter within the current [**IContextNode**](icontextnode.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cfce-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cfce-111">Return value</span></span>

<span data-ttu-id="7cfce-112">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7cfce-112">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7cfce-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cfce-113">Requirements</span></span>



| <span data-ttu-id="7cfce-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cfce-114">Requirement</span></span> | <span data-ttu-id="7cfce-115">Value</span><span class="sxs-lookup"><span data-stu-id="7cfce-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cfce-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cfce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7cfce-117">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7cfce-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7cfce-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7cfce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7cfce-119">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7cfce-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7cfce-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7cfce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cfce-121"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7cfce-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7cfce-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7cfce-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cfce-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cfce-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7cfce-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cfce-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cfce-125">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7cfce-125">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="7cfce-126">**IContextNode::GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="7cfce-126">**IContextNode::GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)
</dt> <dt>

[<span data-ttu-id="7cfce-127">**IContextNode::GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="7cfce-127">**IContextNode::GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)
</dt> <dt>

[<span data-ttu-id="7cfce-128">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7cfce-128">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




