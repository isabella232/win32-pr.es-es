---
title: Error de etiqueta de ARIA
description: Error de etiqueta de ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42abee9028db8c3a4070d9b60d0650187339fc4c9ec34d0b70f720c27e973897
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122325"
---
# <a name="aria-label-error"></a>Error de etiqueta de ARIA

## <a name="text"></a>Texto

El elemento es de tipo **entrada**, **botón**, botón **de imagen** o **punto** de referencia, pero no tiene un nombre accesible.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a:

-   Campos de entrada de formulario:
    -   Etiquetas HTML: input **\[ type= "text password checkbox radio file \| email tel color \| date \| \| \| \| \| \| \| datetime \| datetime-local \| time week month number search \| \| \| \| \| \| url", \]** **select**, **datalist** y **textarea**.
    -   Roles DE ARIA: casilla **,** **cuadro** **combinado,** cuadro de lista, grupo de **radio,** **radio,** cuadro de **texto,** **árbol,** **control deslizante** y botón **de giro**.
-   Imágenes/botones de imagen/botones
    -   Etiquetas HTML:**img**, **input \[ type="image \| button" \]** y **el botón**.
    -   Roles DE ARIA DE ARIA:**img** y **botón**.
-   Puntos de referencia
    -   Roles DE ARIA:**región,** **banner,** **complementario,** **contentinfo,** **formulario**, **principal,** **navegación** y **búsqueda.**

> [!Note]  
> AccChecker muestra este error incluso para los elementos para los que el  nombre accesible se establece de forma predeterminada en función del contenido HTML interno (vea el elemento banner en el ejemplo anterior). En estos casos, puede suprimir estos errores.

 

Todos los elementos de interfaz de usuario semánticamente importantes, como los campos de formulario (por **ejemplo,** entrada **,** seleccione , **textarea**), imágenes, botones y puntos de referencia (etiquetas que representan regiones lógicas) deben tener el nombre accesible para permitir que los lectores de pantalla los anuncien correctamente.

Para corregir este error, establezca el nombre accesible de una de las maneras siguientes (enumeradas en el orden de preferencia).

-   Campos de formulario: use la **etiqueta de** etiqueta y establezca el atributo **for** en el valor **de identificador** del campo de destino.
-   Botón Imagen/imagen: establezca el **atributo alt.**
-   Botones: establezca el texto del título del botón.
-   Para cualquier elemento:
    -   [**Atributo aria-labelledby:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) establezca en el valor **de identificador** del elemento que contiene la cadena de nombre accesible.
    -   [**Atributo aria-label:**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) se establece en la cadena de nombre accesible.
    -   [**atributo title:**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) establezca en la cadena de nombre accesible (también cree una información sobre **herramientas).**

## <a name="example"></a>Ejemplo


```HTML
<!-- For landmark tags, set the accessible name by using the aria-labelledby 
attribute to reference the visible headers. -->
<h1 id="formHeader">Application Form</h1>
<form aria-labelledby="formHeader">

  <!-- For input fields, use the LABEL tag with the for attribute. -->
  <label for="fullName">Full Name</label>
  <input id="fullName" type="text" />

  <!-- If there is no visible text that can be referenced, set the accessible 
  name by using aria-label or title attributes. -->
  <input type="file" aria-label="Your photo"/>

  <!-- For images, use the alt attribute. -->
  <img src="…" alt="Uploaded photo" />

  <!-- For buttons, caption text is also used as the accessible name. -->
  <button onclick="processForm()">Send</button>

  <!-- For image buttons, use the alt attribute to define the accessible name. -->
  <input type="image" src="images/moreinfo.png" alt="Show more info"/>

  <!-- For elements with inner text this error can be suppressed because the 
  accessible name is set by default. -->
  <div role="banner">Accessible name set by default</div>
</form >
```



 

 




