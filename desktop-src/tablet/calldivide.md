---
description: Recupera información de análisis del objeto InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539454"
---
# <a name="calldivide-function"></a><span data-ttu-id="65968-103">CallDivide función)</span><span class="sxs-lookup"><span data-stu-id="65968-103">CallDivide function</span></span>

<span data-ttu-id="65968-104">Recupera información de análisis del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="65968-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65968-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="65968-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65968-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="65968-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65968-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65968-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65968-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="65968-110">*pWordSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65968-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-111">Tamaño de la palabra devuelta por el objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="65968-112">*pLineSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65968-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-113">Tamaño de la línea devuelta por el objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="65968-114">*pParagraphSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65968-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-115">Tamaño del párrafo devuelto por el objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="65968-116">*pDrawingSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="65968-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-117">Tamaño del dibujo devuelto por el objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="65968-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="65968-118">*pWordCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65968-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-119">Número de palabras que devuelve el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="65968-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="65968-120">*pLineCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65968-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-121">Número de líneas devueltas por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="65968-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="65968-122">*pParagraphCount* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="65968-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65968-123">El número de párrafos devueltos por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="65968-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65968-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65968-124">Return value</span></span>

<span data-ttu-id="65968-125">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="65968-125">This function can return one of these values.</span></span>



| <span data-ttu-id="65968-126">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="65968-126">Return code</span></span>                                                                                  | <span data-ttu-id="65968-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="65968-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="65968-128"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="65968-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="65968-129">La función correcta.</span><span class="sxs-lookup"><span data-stu-id="65968-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="65968-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="65968-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="65968-131">Uno o más parámetros no son válidos.</span><span class="sxs-lookup"><span data-stu-id="65968-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="65968-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65968-132">Requirements</span></span>



| <span data-ttu-id="65968-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="65968-133">Requirement</span></span> | <span data-ttu-id="65968-134">Value</span><span class="sxs-lookup"><span data-stu-id="65968-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65968-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65968-135">Minimum supported client</span></span><br/> | <span data-ttu-id="65968-136">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="65968-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="65968-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65968-137">Minimum supported server</span></span><br/> | <span data-ttu-id="65968-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="65968-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="65968-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65968-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="65968-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65968-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




