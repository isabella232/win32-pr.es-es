---
description: Indica si la cadena reconocida especificada procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'IContextNode:: IsAlternateStringSupported (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666501"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="7abc0-103">IContextNode:: IsAlternateStringSupported (método)</span><span class="sxs-lookup"><span data-stu-id="7abc0-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="7abc0-104">Indica si la cadena reconocida especificada procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="7abc0-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="7abc0-105">Los datos restrictivos, como wordlists, Guides o Factoids, en cualquier nodo de sugerencia correspondiente se utilizarán para determinar si se admite la cadena.</span><span class="sxs-lookup"><span data-stu-id="7abc0-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="7abc0-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7abc0-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="7abc0-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7abc0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7abc0-108">*bstrAlternateString* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7abc0-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7abc0-109">Cadena reconocida que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="7abc0-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="7abc0-110">*pfIsSupported* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7abc0-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7abc0-111">**Variante \_ TRUE** si el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) admite la cadena especificada con los nodos de sugerencia correspondientes aplicados; **Variante \_ FALSE** si no se admite.</span><span class="sxs-lookup"><span data-stu-id="7abc0-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7abc0-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7abc0-112">Return value</span></span>

<span data-ttu-id="7abc0-113">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="7abc0-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7abc0-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7abc0-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="7abc0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7abc0-115">Requirements</span></span>



| <span data-ttu-id="7abc0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7abc0-116">Requirement</span></span> | <span data-ttu-id="7abc0-117">Value</span><span class="sxs-lookup"><span data-stu-id="7abc0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abc0-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7abc0-119">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="7abc0-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7abc0-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7abc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7abc0-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7abc0-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="7abc0-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7abc0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7abc0-123"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="7abc0-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="7abc0-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7abc0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7abc0-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7abc0-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="7abc0-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7abc0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abc0-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="7abc0-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




