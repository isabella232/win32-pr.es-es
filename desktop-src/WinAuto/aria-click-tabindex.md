---
title: Error de TabIndex de ARIA
description: Error de TabIndex de ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078541"
---
# <a name="aria-tabindex-error"></a>Error de TabIndex de ARIA

## <a name="text"></a>Texto

El elemento no está deshabilitado y tiene un controlador de eventos **click** pero tiene **TabIndex** < 0 y no está en el orden de tabulación de forma predeterminada.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a los elementos que tienen un controlador de eventos click y no están deshabilitados. Estos elementos deben estar en el orden de tabulación. Esto garantiza que se puede obtener acceso a un elemento mediante la tecla Tab, que es la forma en que los usuarios del lector de pantalla navegan por la interfaz de usuario.

Para corregir este error, establezca el atributo [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) en un valor que sea igual o mayor que 0. No es necesario establecer explícitamente el atributo **TabIndex** para las etiquetas que se encuentran en el orden de tabulación de forma predeterminada, como [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) (con el atributo [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), el [**botón**](https://developer.mozilla.org/docs/Web/HTML/Element/button), la [**entrada**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (excepto "Hidden"), [**Select**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**TextArea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)y [**Area**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (como parte del mapa de imágenes).

## <a name="example"></a>Ejemplo


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




