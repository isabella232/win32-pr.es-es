---
title: Faltan atributos de control de intervalo de ARIA
description: Faltan atributos de control de intervalo de ARIA
ms.assetid: B79F6277-5339-406A-B5FC-A3657BFC5034
keywords:
- AriaRangeControlAttributesAbsentId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44e4e5c69ea6971846ed9ef5f3a6108bb488c6effb21a6cbc75953ed1bb780e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645125"
---
# <a name="aria-range-control-attributes-missing"></a>Faltan atributos de control de intervalo de ARIA

## <a name="text"></a>Texto

El elemento tiene  **el rol de** barra de progreso o control deslizante, pero no expone los atributos **aria-valuemin** , **aria-valuemax** y **aria-valuenow** correspondientes.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica [**a**](https://developer.mozilla.org/docs/Web/HTML/Reference) los elementos que tienen un rol (implícito o explícito) que es igual a **la** barra de progreso, el **control deslizante** o el botón **de número**.

Según la especificación iniciativa de accesibilidad web: aplicaciones de Internet enriquecencia accesibles (WAI-ARIA), los elementos que tienen el rol **progressbar**, **slider** o **spinbutton** deben exponer los atributos [**aria-valuemax,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**aria-valuenow.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)

Para corregir este error, establezca los atributos [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA), [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)y [**aria-valuenow,**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y mantenga dinámicamente el valor **aria-valuenow** para asegurarse de que se expone el valor actual. También debe establecer el atributo [**aria-valuetext**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) para agregar más significado al valor **aria-valuenow** expuesto.

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

 

 




