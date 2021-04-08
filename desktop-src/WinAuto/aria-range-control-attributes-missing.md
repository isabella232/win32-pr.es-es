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
# <a name="aria-range-control-attributes-missing"></a>Faltan atributos de control de intervalo ARIA

## <a name="text"></a>Texto

El elemento tiene el rol **ProgressBar** o **Slider** , pero no expone los atributos **Aria-valuemin** , **Aria-valuemax** y **Aria-valuenow** correspondientes.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un [**rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícito o explícito) que es igual a **ProgressBar**, **Slider** o **SpinButton**.

Según la especificación de aplicaciones de Internet enriquecidas (WAI-ARIA) de accesibilidad a la iniciativa Web Accessibility Initiative, los elementos que tienen el rol **ProgressBar**, **Slider** o **SpinButton** deben exponer los atributos [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Para corregir este error, establezca los atributos [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y mantenga dinámicamente el valor **Aria-valuenow** para asegurarse de que el valor actual está expuesto. También debe establecer el atributo [**Aria-ValueText**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para agregar más significado al valor **Aria-valuenow** expuesto.

## <a name="example"></a>Ejemplo


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de control de intervalo de ARIA incompatibles](aria-range-control-attribute-out-of-range.md)
</dt> </dl>

 

 




