---
title: ARIA Tabindex Error
description: ARIA Tabindex Error
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1637008b6679f196f7bba0701606e0514abe44410032e1a5ffc063977ddf10e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118326757"
---
# <a name="aria-tabindex-error"></a>ARIA Tabindex Error

## <a name="text"></a>Texto

El elemento no está deshabilitado y tiene un controlador de eventos **click,** pero tiene **tabIndex** < 0 y no está en el orden de tabulación de forma predeterminada.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un controlador de eventos click y no están deshabilitados. Estos elementos deben estar en el orden de tabulación. Esto garantiza que se pueda acceder a un elemento mediante la tecla Tab, que es la forma en que los usuarios del lector de pantalla suelen navegar por la interfaz de usuario.

Para corregir este error, establezca el atributo [**tabindex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) en un valor igual o mayor que 0. No es necesario establecer explícitamente el atributo **tabindex** para las etiquetas que están en el orden de tabulación de forma predeterminada, como [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (con el atributo [**href),**](https://developer.mozilla.org/docs/Web/HTML/Attributes) el botón [**,**](https://developer.mozilla.org/docs/Web/HTML/Element/button)la entrada [**(excepto**](https://developer.mozilla.org/docs/Web/HTML/Element/input) "hidden"), [](https://developer.mozilla.org/docs/Web/HTML/Element/select)seleccionar , [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)y [**el**](https://developer.mozilla.org/docs/Web/HTML/Element/area) área (como parte del mapa de imágenes).

## <a name="example"></a>Ejemplo


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




