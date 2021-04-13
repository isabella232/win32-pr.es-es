---
title: Error de rol de ARIA para elementos con controladores de eventos
description: Error de rol de ARIA para elementos con controladores de eventos
ms.assetid: 20BB874A-874B-4266-9C7B-49C07D4146DA
keywords:
- AriaContainerRoleErrorMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eede416392e8b4cb644938242a9975238118ff07
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104421553"
---
# <a name="aria-role-error-for-elements-with-event-handlers"></a>Error de rol de ARIA para elementos con controladores de eventos

## <a name="text"></a>Texto

El elemento tiene un controlador de eventos pero no se ha definido un rol WAI-ARIA válido.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que no tienen un rol de aplicaciones de Internet enriquecidas con acceso a la iniciativa de accesibilidad web (WAI-ARIA).

Este error indica que un elemento tiene un mouse o un controlador de eventos de teclado (**click**, **MouseDown**, **MouseUp**, **MouseMove**, **mouseout**, **mouseover**, **KeyUp**, **KeyDown** o **KEYPRESS**), pero no tiene establecido el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) y no es una de las etiquetas HTML que tiene un rol WAI-ARIA implícito (por ejemplo, **a**, **Button**, **IMG**, **Input**, **Select** , etc.).

Es necesario establecer el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) para los elementos interactivos que no tienen ningún rol implícito (como una etiqueta **div** ) para exponer los patrones de comportamiento del elemento a los lectores de pantalla y otras tecnologías de asistencia.

Para corregir este error, establezca el atributo [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) en un rol WAI-ARIA válido que se ajuste mejor a los patrones de comportamiento de este elemento y los atributos requeridos. Por ejemplo, si una etiqueta **div** funciona como un botón, establezca el atributo role en "Button".

## <a name="example"></a>Ejemplo


```HTML
<!-- Setting role attribute allows screen readers to know it can be clicked -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




