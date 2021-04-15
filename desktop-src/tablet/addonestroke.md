---
description: Agrega un nuevo objeto IInkStrokeDisp al objeto InkDivider que se ha pasado.
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496751"
---
# <a name="addonestroke-function"></a><span data-ttu-id="85c21-103">AddOneStroke función)</span><span class="sxs-lookup"><span data-stu-id="85c21-103">AddOneStroke function</span></span>

<span data-ttu-id="85c21-104">Agrega un nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) al objeto [**InkDivider**](inkdivider-class.md) que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="85c21-104">Adds a new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to the [**InkDivider**](inkdivider-class.md) object that was passed in.</span></span>

<span data-ttu-id="85c21-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="85c21-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="85c21-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85c21-106">Syntax</span></span>


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a><span data-ttu-id="85c21-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85c21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85c21-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85c21-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c21-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="85c21-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85c21-110">*strokeId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85c21-110">*strokeId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c21-111">[**Identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) del objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) que se va a agregar al objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="85c21-111">The [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object to be added to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="85c21-112">*cPoints* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85c21-112">*cPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c21-113">El número de paquetes que componen el nuevo objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="85c21-113">The number of packets that make up the new [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="85c21-114">*aPoints* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="85c21-114">*aPoints* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85c21-115">La matriz de paquetes que componen el objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) en *strokeId*.</span><span class="sxs-lookup"><span data-stu-id="85c21-115">The array of packets that make up the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object in *strokeId*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85c21-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85c21-116">Return value</span></span>

<span data-ttu-id="85c21-117">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="85c21-117">This function can return one of these values.</span></span>



| <span data-ttu-id="85c21-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="85c21-118">Return code</span></span>                                                                                  | <span data-ttu-id="85c21-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="85c21-119">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="85c21-120"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="85c21-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="85c21-121">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="85c21-121">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="85c21-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="85c21-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="85c21-123">El parámetro *hDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="85c21-123">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="85c21-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85c21-124">Requirements</span></span>



| <span data-ttu-id="85c21-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="85c21-125">Requirement</span></span> | <span data-ttu-id="85c21-126">Value</span><span class="sxs-lookup"><span data-stu-id="85c21-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85c21-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85c21-127">Minimum supported client</span></span><br/> | <span data-ttu-id="85c21-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85c21-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="85c21-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85c21-129">Minimum supported server</span></span><br/> | <span data-ttu-id="85c21-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="85c21-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="85c21-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85c21-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="85c21-132"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85c21-132"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




