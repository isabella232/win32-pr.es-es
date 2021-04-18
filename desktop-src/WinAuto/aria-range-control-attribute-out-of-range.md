---
title: Atributos de control de intervalo de ARIA incompatibles
description: Atributos de control de intervalo de ARIA incompatibles
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef55ee57c4966896e666dd5a7ac1d20eb5257c6
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104533574"
---
# <a name="aria-range-control-attributes-incompatible"></a><span data-ttu-id="35cba-104">Atributos de control de intervalo de ARIA incompatibles</span><span class="sxs-lookup"><span data-stu-id="35cba-104">ARIA Range Control Attributes Incompatible</span></span>

## <a name="text"></a><span data-ttu-id="35cba-105">Texto</span><span class="sxs-lookup"><span data-stu-id="35cba-105">Text</span></span>

<span data-ttu-id="35cba-106">El elemento tiene el rol **ProgressBar** o **Slider** , pero **el valor Aria-valuenow** expuesto está fuera del intervalo **Aria-valuemin** **Aria-valuemax** .</span><span class="sxs-lookup"><span data-stu-id="35cba-106">Element has **progressbar** or **slider** role but exposed **aria-valuenow** value is outside of **aria-valuemin** **aria-valuemax** range.</span></span>

## <a name="type"></a><span data-ttu-id="35cba-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="35cba-107">Type</span></span>

<span data-ttu-id="35cba-108">Error</span><span class="sxs-lookup"><span data-stu-id="35cba-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="35cba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="35cba-109">Description</span></span>

<span data-ttu-id="35cba-110">Este error se aplica a los elementos que tienen un [**rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícito o explícito) igual a **ProgressBar**, **Slider** o **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="35cba-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="35cba-111">Este error indica que el valor [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) expuesto no está en el intervalo definido por los atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="35cba-111">This error indicates that the exposed [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) value is not in the range defined by the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="35cba-112">Para corregir este error, Compruebe la implementación para asegurarse de que los atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) están establecidos correctamente y de que el valor del atributo [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) se mantiene correctamente.</span><span class="sxs-lookup"><span data-stu-id="35cba-112">To fix this error, check your implementation to ensure that the [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) and [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes are correctly set, and that the [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute value is properly maintained.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35cba-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35cba-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35cba-114">Faltan atributos de control de intervalo ARIA</span><span class="sxs-lookup"><span data-stu-id="35cba-114">ARIA Range Control Attributes Missing</span></span>](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




