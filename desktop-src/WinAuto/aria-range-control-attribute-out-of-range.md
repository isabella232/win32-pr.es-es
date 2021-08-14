---
title: Atributos de control de intervalo de ARIA incompatibles
description: Atributos de control de intervalo de ARIA incompatibles
ms.assetid: 265AE578-D841-4931-9F4A-97BB86ECEC88
keywords:
- AriaRangeControlAttributesIncompatibleId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991f5de18be88682046cac6c4d4156f48fd3e4994d2e7b9ab1bbdc52f0a2e768
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326758"
---
# <a name="aria-range-control-attributes-incompatible"></a>Atributos de control de intervalo de ARIA incompatibles

## <a name="text"></a>Texto

El elemento tiene  **el rol de** barra de progreso o control deslizante, pero el valor **de aria-valuenow** expuesto está fuera del intervalo **aria-valuemin** **aria-valuemax.**

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un [**rol**](https://developer.mozilla.org/docs/Web/HTML/Reference) (implícito o explícito) igual a **la** barra de progreso, **el control deslizante** o el botón de **número**.

Este error indica que el valor [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) expuesto no está en el intervalo definido por los atributos [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**aria-valuemax.**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA)

Para corregir este error, compruebe la implementación para asegurarse de que los atributos [**aria-valuemin**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) y [**aria-valuemax**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) están establecidos correctamente y de que el valor del atributo [**aria-valuenow**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) se mantiene correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Faltan atributos de control de intervalo de ARIA](aria-range-control-attributes-missing.md)
</dt> </dl>

 

 




