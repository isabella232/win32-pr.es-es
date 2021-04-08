---
title: Faltan atributos de control de intervalo ARIA
description: Faltan atributos de control de intervalo ARIA
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cd32a7a4807f06c26bd013ee3fd294d33cc57
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078537"
---
# <a name="aria-range-control-attributes-missing"></a><span data-ttu-id="5080f-104">Faltan atributos de control de intervalo ARIA</span><span class="sxs-lookup"><span data-stu-id="5080f-104">ARIA Range Control Attributes Missing</span></span>

## <a name="text"></a><span data-ttu-id="5080f-105">Texto</span><span class="sxs-lookup"><span data-stu-id="5080f-105">Text</span></span>

<span data-ttu-id="5080f-106">El elemento tiene el rol **ProgressBar** o **Slider** , pero no expone los atributos **Aria-valuemin** , **Aria-valuemax** y **Aria-valuenow** correspondientes.</span><span class="sxs-lookup"><span data-stu-id="5080f-106">Element has **progressbar** or **slider** role but is not exposing corresponding **aria-valuemin** , **aria-valuemax** , and **aria-valuenow** attributes.</span></span>

## <a name="type"></a><span data-ttu-id="5080f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5080f-107">Type</span></span>

<span data-ttu-id="5080f-108">Error</span><span class="sxs-lookup"><span data-stu-id="5080f-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="5080f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5080f-109">Description</span></span>

<span data-ttu-id="5080f-110">Este error se aplica a los elementos que tienen un [**rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícito o explícito) que es igual a **ProgressBar**, **Slider** o **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="5080f-110">This error applies to elements that have a [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implicit or explicit) that is equal to **progressbar**, **slider**, or **spinbutton**.</span></span>

<span data-ttu-id="5080f-111">Según la especificación de aplicaciones de Internet enriquecidas (WAI-ARIA) de accesibilidad a la iniciativa Web Accessibility Initiative, los elementos que tienen el rol **ProgressBar**, **Slider** o **SpinButton** deben exponer los atributos [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .</span><span class="sxs-lookup"><span data-stu-id="5080f-111">According to the Web Accessibility Initiative - Accessible Rich Internet Applications (WAI-ARIA) specification, elements that have the **progressbar**, **slider**, or **spinbutton** role must expose the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes.</span></span>

<span data-ttu-id="5080f-112">Para corregir este error, establezca los atributos [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y mantenga dinámicamente el valor **Aria-valuenow** para asegurarse de que el valor actual está expuesto.</span><span class="sxs-lookup"><span data-stu-id="5080f-112">To fix this error, set the [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), and [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attributes, and dynamically maintain the **aria-valuenow** value to ensure that the current value is exposed.</span></span> <span data-ttu-id="5080f-113">También debe establecer el atributo [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para agregar más significado al valor **Aria-valuenow** expuesto.</span><span class="sxs-lookup"><span data-stu-id="5080f-113">You should also set the [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute to add more meaning to the exposed **aria-valuenow** value.</span></span>

## <a name="example"></a><span data-ttu-id="5080f-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5080f-114">Example</span></span>


```HTML
<div role="slider" id="sl" aria-valuemin="1" aria-valuemax="5" aria-valuenow="3" aria-valuetext="good"…>
</div>

<script>
  // This function should be triggered when the slider value changes.
  function manageValue()
  {
    ...
    sl.setAttribute("aria-valuenow", currentValue);
    sl.setAttribute("aria-valuetext", currentValueText);
    ...
  }
</script>
```



## <a name="related-topics"></a><span data-ttu-id="5080f-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5080f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5080f-116">Atributos de control de intervalo de ARIA incompatibles</span><span class="sxs-lookup"><span data-stu-id="5080f-116">ARIA Range Control Attributes Incompatible</span></span>](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




