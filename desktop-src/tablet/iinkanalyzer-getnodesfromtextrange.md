---
description: Recupera una colección de objetos IContextNode que son pertinentes para el intervalo de texto especificado para los nodos de contexto especificados.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'IInkAnalyzer:: GetNodesFromTextRange (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810009"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="965b2-103">IInkAnalyzer:: GetNodesFromTextRange (método)</span><span class="sxs-lookup"><span data-stu-id="965b2-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="965b2-104">Recupera una colección de objetos [**IContextNode**](icontextnode.md) que son pertinentes para el intervalo de texto especificado para los nodos de contexto especificados.</span><span class="sxs-lookup"><span data-stu-id="965b2-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="965b2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="965b2-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="965b2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="965b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965b2-107">*plStart* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="965b2-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="965b2-108">Referencia al inicio del intervalo de texto en la parte *pNodesToSearch* de la cadena reconocida.</span><span class="sxs-lookup"><span data-stu-id="965b2-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="965b2-109">*plLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="965b2-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="965b2-110">Referencia a la longitud del intervalo de texto en la parte *pNodesToSearch* de la cadena reconocida.</span><span class="sxs-lookup"><span data-stu-id="965b2-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="965b2-111">*ppContextNodes* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="965b2-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="965b2-112">Puntero a los objetos [**IContextNode**](icontextnode.md) que son pertinentes para el intervalo de texto especificado para los nodos de contexto especificados.</span><span class="sxs-lookup"><span data-stu-id="965b2-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="965b2-113">*pNodesToSearch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="965b2-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="965b2-114">Objetos [**IContextNode**](icontextnode.md) a los que se va a limitar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="965b2-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965b2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="965b2-115">Return value</span></span>

<span data-ttu-id="965b2-116">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="965b2-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="965b2-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="965b2-117">Remarks</span></span>

<span data-ttu-id="965b2-118">El intervalo de texto especificado debe ser relativo a la parte *pNodesToSearch* de la cadena reconocida de [**IInkAnalyzer**](iinkanalyzer.md), en lugar de a la cadena reconocida de toda la **IInkAnalyzer**.</span><span class="sxs-lookup"><span data-stu-id="965b2-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="965b2-119">Este método modifica los valores de los parámetros *plStart* y *plLength* expandiendo el intervalo de texto a los límites de palabra más cercanos.</span><span class="sxs-lookup"><span data-stu-id="965b2-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="965b2-120">Por ejemplo, si la cadena reconocida es "he tarde" y llama a este método con los valores de parámetro de 6 para *plStart* y 1 para *plLength*, que corresponde a la letra "a" en "late", este método devuelve una colección que contiene una sola [**IContextNode**](icontextnode.md), InkWord o TextWord que corresponde a la palabra "late".</span><span class="sxs-lookup"><span data-stu-id="965b2-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="965b2-121">En este ejemplo, este método también modifica el valor de *plStart* a 5 y el valor de *plLength* a 4, que corresponde a la palabra "late".</span><span class="sxs-lookup"><span data-stu-id="965b2-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="965b2-122">El parámetro *plStart* es relativo a la cadena reconocida del parámetro *pNodesToSearch* .</span><span class="sxs-lookup"><span data-stu-id="965b2-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="965b2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="965b2-123">Requirements</span></span>



| <span data-ttu-id="965b2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="965b2-124">Requirement</span></span> | <span data-ttu-id="965b2-125">Value</span><span class="sxs-lookup"><span data-stu-id="965b2-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965b2-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965b2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="965b2-127">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="965b2-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="965b2-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965b2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="965b2-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="965b2-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="965b2-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="965b2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="965b2-131"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="965b2-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="965b2-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="965b2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="965b2-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="965b2-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="965b2-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="965b2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="965b2-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="965b2-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




