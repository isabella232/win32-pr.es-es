---
title: Error de etiqueta ARIA
description: Error de etiqueta ARIA
ms.assetid: DF45E38D-9AD3-48C8-911E-8C6233F17F43
keywords:
- AriaLabelErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1091c46dbb660c4c3568d24bfca34d94ef869f1e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104078538"
---
# <a name="aria-label-error"></a>Error de etiqueta ARIA

## <a name="text"></a>Texto

El elemento es de tipo **Input**, **Button**, **Image-Button** o **monumentos** pero no tiene un nombre accesible.

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Este error se aplica a:

-   Campos de entrada de formulario:
    -   Etiquetas HTML:**tipo de entrada \[ = "texto de la \| casilla de verificación de contraseña \| archivo de \| radio \| \| correo electrónico \| de Tel. fecha y hora fecha y \| \| \| \| hora del día de la \| \| \| \| \| \| búsqueda \| URL \] "**, **Select**, **DataList** y **TextArea**.
    -   Roles WAI-ARIA:**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **radio**, **TextBox**, **Tree**, **Slider** y **SpinButton**.
-   Imágenes/botones de imagen/botones
    -   Etiquetas HTML:**IMG**, **Input \[ type = "Image \| Button" \]** y **Button**.
    -   Roles WAI-ARIA:**IMG** y **Button**.
-   Puntos de referencia
    -   Roles WAI-ARIA:**región**, **banner**, **complementario**, **ContentInfo**, **formulario**, **principal**, **navegación** y **búsqueda**.

> [!Note]  
> AccChecker muestra este error incluso para los elementos para los que el nombre accesible se establece de forma predeterminada en función del contenido HTML interno (vea el elemento **banner** en el ejemplo anterior). En estos casos, puede suprimir este error.

 

Todos los elementos de la interfaz de usuario semánticamente importantes, como campos de formulario (por ejemplo, **Input**, **Select**, **TextArea**), imágenes, botones y puntos de referencia (etiquetas que representan regiones lógicas) deben tener el nombre accesible para permitir que los lectores de pantalla los anuncien correctamente.

Para corregir este error, establezca el nombre accesible de una de las siguientes maneras (en orden de preferencia).

-   Campos de formulario: Use la etiqueta **etiqueta** y establezca el atributo **for** en el valor de **identificador** del campo de destino.
-   Botón imagen/imagen: establezca el atributo **Alt** .
-   Botones: establezca el texto del título del botón.
-   Para cualquier elemento:
    -   atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : establézcalo en el valor de **identificador** del elemento que contiene la cadena de nombre accesible.
    -   atributo [**de etiqueta Aria**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : se establece en la cadena de nombre accesible.
    -   atributo de [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : establézcalo en la cadena de nombre accesible (también puede crear una **información sobre herramientas**).

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



 

 




