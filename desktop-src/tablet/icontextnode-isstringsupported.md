---
description: Indica si la cadena reconocida de este IContextNode procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'IContextNode:: IsStringSupported (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696531"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="b16d5-103">IContextNode:: IsStringSupported (método)</span><span class="sxs-lookup"><span data-stu-id="b16d5-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="b16d5-104">Indica si la cadena reconocida de este [**IContextNode**](icontextnode.md) procede del Diccionario del sistema, del Diccionario del usuario o de la lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="b16d5-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b16d5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b16d5-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="b16d5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b16d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b16d5-107">*pfIsSupported* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b16d5-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b16d5-108">**Variante \_ TRUE** si el valor de cadena reconocido de este [**IContextNode**](icontextnode.md) es compatible con [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) con los nodos de sugerencia correspondientes aplicados; de lo contrario, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b16d5-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b16d5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b16d5-109">Return value</span></span>

<span data-ttu-id="b16d5-110">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="b16d5-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b16d5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b16d5-111">Requirements</span></span>



| <span data-ttu-id="b16d5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b16d5-112">Requirement</span></span> | <span data-ttu-id="b16d5-113">Value</span><span class="sxs-lookup"><span data-stu-id="b16d5-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b16d5-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b16d5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b16d5-115">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b16d5-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="b16d5-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b16d5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b16d5-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b16d5-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="b16d5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b16d5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b16d5-119"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b16d5-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b16d5-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b16d5-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b16d5-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b16d5-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="b16d5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="b16d5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b16d5-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="b16d5-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




