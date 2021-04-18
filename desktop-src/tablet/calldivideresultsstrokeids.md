---
description: Recupera las propiedades de identificador para los objetos IInkStrokeDisp de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de tinta.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705395"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="df487-103">CallDivideResultsStrokeIds función)</span><span class="sxs-lookup"><span data-stu-id="df487-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="df487-104">Recupera las propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) de la palabra, línea, párrafo o dibujo correspondientes determinados por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="df487-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="df487-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="df487-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="df487-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df487-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="df487-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="df487-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df487-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="df487-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df487-109">Identificador del objeto de [divisor](the-divider-object.md) .</span><span class="sxs-lookup"><span data-stu-id="df487-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="df487-110">*\[ aWordStrokeIds \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="df487-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df487-111">Matriz de los identificadores de trazo de la tinta de la palabra.</span><span class="sxs-lookup"><span data-stu-id="df487-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="df487-112">*\[ aLineStrokeIds \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="df487-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df487-113">Matriz de los identificadores de trazo de la entrada de lápiz en la línea.</span><span class="sxs-lookup"><span data-stu-id="df487-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="df487-114">*\[ aParagraphStrokeIds \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="df487-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df487-115">Matriz de los identificadores de trazo de la entrada de lápiz en el párrafo.</span><span class="sxs-lookup"><span data-stu-id="df487-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="df487-116">*\[ aDrawingStrokeIds \]* \[fuera de\]</span><span class="sxs-lookup"><span data-stu-id="df487-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="df487-117">Matriz de los identificadores de trazo de la tinta del dibujo.</span><span class="sxs-lookup"><span data-stu-id="df487-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df487-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df487-118">Return value</span></span>

<span data-ttu-id="df487-119">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="df487-119">This function can return one of these values.</span></span>



| <span data-ttu-id="df487-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="df487-120">Return code</span></span>                                                                                  | <span data-ttu-id="df487-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="df487-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="df487-122"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="df487-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="df487-123">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="df487-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="df487-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="df487-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="df487-125">El parámetro *hDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="df487-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="df487-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df487-126">Requirements</span></span>



| <span data-ttu-id="df487-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="df487-127">Requirement</span></span> | <span data-ttu-id="df487-128">Value</span><span class="sxs-lookup"><span data-stu-id="df487-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df487-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df487-129">Minimum supported client</span></span><br/> | <span data-ttu-id="df487-130">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="df487-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="df487-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df487-131">Minimum supported server</span></span><br/> | <span data-ttu-id="df487-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="df487-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="df487-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df487-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="df487-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df487-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




