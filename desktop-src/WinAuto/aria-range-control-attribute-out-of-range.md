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
# <a name="aria-range-control-attributes-incompatible"></a>Atributos de control de intervalo de ARIA incompatibles

## <a name="text"></a>Texto

El elemento tiene el rol **ProgressBar** o **Slider** , pero **el valor Aria-valuenow** expuesto está fuera del intervalo **Aria-valuemin** **Aria-valuemax** .

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un [**rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícito o explícito) igual a **ProgressBar**, **Slider** o **SpinButton**.

Este error indica que el valor [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) expuesto no está en el intervalo definido por los atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) .

Para corregir este error, Compruebe la implementación para asegurarse de que los atributos [**Aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**Aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) están establecidos correctamente y de que el valor del atributo [**Aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) se mantiene correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Faltan atributos de control de intervalo ARIA](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




