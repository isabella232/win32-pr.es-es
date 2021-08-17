---
title: Error de rol de ARIA para elementos con controladores de eventos
description: Error de rol de ARIA para elementos con controladores de eventos
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cebaa2e6f4526d0a1e820e60adc1d28439d3f361c7ffb58a0c4d855861ea46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133998"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Error de rol de ARIA para elementos con controladores de eventos

## <a name="text"></a>Texto

El elemento tiene un controlador de eventos, pero no se ha definido el rol VÁLIDO DE ARIA.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que no tienen un rol implícita iniciativa de accesibilidad web: aplicaciones de Internet enriquecciones accesibles (WAI-ARIA).

Este error indica que un elemento tiene un controlador de eventos de mouse o teclado (haga clic en , [](https://developer.mozilla.org/docs/Web/HTML/Reference) **mousedown**, **mouseup**, **mousemove**, **mouseout**, **mouseover**, **keyup**, **keydown** o **keypress**), pero no tiene establecido el atributo de rol y no es una de las etiquetas HTML que tiene un rol IMPLÍCITA DE ARIA PARA EL MOUSE (por **ejemplo,** **un**, botón , **img** **,** entrada **,** seleccionar, y así sucesivamente).

Es [](https://developer.mozilla.org/docs/Web/HTML/Reference) necesario establecer el atributo role para los elementos interactivos que no tienen ningún rol implícito (por ejemplo, una etiqueta **div)** para exponer los patrones de comportamiento del elemento a los lectores de pantalla y otras tecnologías de asistencia.

Para corregir este error, establezca el atributo [**de**](https://developer.mozilla.org/docs/Web/HTML/Reference) rol en un rol VÁLIDO DE ACUERDO ARIA que se adapte mejor a los patrones de comportamiento de este elemento y a los atributos necesarios. Por ejemplo, si una **etiqueta div** funciona como un botón, establezca el atributo role en "button".

## <a name="example"></a>Ejemplo


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




