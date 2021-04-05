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
# <a name="aria-label-error"></a><span data-ttu-id="5ffbe-104">Error de etiqueta ARIA</span><span class="sxs-lookup"><span data-stu-id="5ffbe-104">ARIA Label Error</span></span>

## <a name="text"></a><span data-ttu-id="5ffbe-105">Texto</span><span class="sxs-lookup"><span data-stu-id="5ffbe-105">Text</span></span>

<span data-ttu-id="5ffbe-106">El elemento es de tipo **Input**, **Button**, **Image-Button** o **monumentos** pero no tiene un nombre accesible.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-106">Element is of type **input**, **button**, **image-button** or **landmark** but doesn't have an accessible name.</span></span>

## <a name="type"></a><span data-ttu-id="5ffbe-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ffbe-107">Type</span></span>

<span data-ttu-id="5ffbe-108">Error</span><span class="sxs-lookup"><span data-stu-id="5ffbe-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="5ffbe-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ffbe-109">Description</span></span>

<span data-ttu-id="5ffbe-110">Este error se aplica a:</span><span class="sxs-lookup"><span data-stu-id="5ffbe-110">This error applies to:</span></span>

-   <span data-ttu-id="5ffbe-111">Campos de entrada de formulario:</span><span class="sxs-lookup"><span data-stu-id="5ffbe-111">Form input fields:</span></span>
    -   <span data-ttu-id="5ffbe-112">Etiquetas HTML:**tipo de entrada \[ = "texto de la \| casilla de verificación de contraseña \| archivo de \| radio \| \| correo electrónico \| de Tel. fecha y hora fecha y \| \| \| \| hora del día de la \| \| \| \| \| \| búsqueda \| URL \] "**, **Select**, **DataList** y **TextArea**.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-112">HTML tags—**input\[type= "text\|password\|checkbox\|radio\|file\|email\|tel\|color\|date\|datetime\|datetime-local\|time\|week\|month\|number\|range\|search\|url"\]**, **select**, **datalist**, and **textarea**.</span></span>
    -   <span data-ttu-id="5ffbe-113">Roles WAI-ARIA:**CheckBox**, **ComboBox**, **ListBox**, **RadioGroup**, **radio**, **TextBox**, **Tree**, **Slider** y **SpinButton**.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-113">WAI-ARIA roles—**checkbox**, **combobox**, **listbox**, **radiogroup**, **radio**, **textbox**, **tree**, **slider**, and **spinbutton**.</span></span>
-   <span data-ttu-id="5ffbe-114">Imágenes/botones de imagen/botones</span><span class="sxs-lookup"><span data-stu-id="5ffbe-114">Images/image buttons/ buttons</span></span>
    -   <span data-ttu-id="5ffbe-115">Etiquetas HTML:**IMG**, **Input \[ type = "Image \| Button" \]** y **Button**.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-115">HTML tags—**img**, **input\[type="image\|button"\]**, and **button**.</span></span>
    -   <span data-ttu-id="5ffbe-116">Roles WAI-ARIA:**IMG** y **Button**.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-116">WAI-ARIA roles—**img** and **button**.</span></span>
-   <span data-ttu-id="5ffbe-117">Puntos de referencia</span><span class="sxs-lookup"><span data-stu-id="5ffbe-117">Landmarks</span></span>
    -   <span data-ttu-id="5ffbe-118">Roles WAI-ARIA:**región**, **banner**, **complementario**, **ContentInfo**, **formulario**, **principal**, **navegación** y **búsqueda**.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-118">WAI-ARIA roles—**region**, **banner**, **complementary**, **contentinfo**, **form**, **main**, **navigation**, and **search**.</span></span>

> [!Note]  
> <span data-ttu-id="5ffbe-119">AccChecker muestra este error incluso para los elementos para los que el nombre accesible se establece de forma predeterminada en función del contenido HTML interno (vea el elemento **banner** en el ejemplo anterior).</span><span class="sxs-lookup"><span data-stu-id="5ffbe-119">AccChecker shows this error even for elements for which the accessible name is set by default based on inner HTML content (see the **banner** element in the above example).</span></span> <span data-ttu-id="5ffbe-120">En estos casos, puede suprimir este error.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-120">For these cases, you can suppress this errors.</span></span>

 

<span data-ttu-id="5ffbe-121">Todos los elementos de la interfaz de usuario semánticamente importantes, como campos de formulario (por ejemplo, **Input**, **Select**, **TextArea**), imágenes, botones y puntos de referencia (etiquetas que representan regiones lógicas) deben tener el nombre accesible para permitir que los lectores de pantalla los anuncien correctamente.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-121">All semantically important UI elements such as form fields (for example, **input**, **select**, **textarea**), images, buttons and landmarks (tags representing logical regions) must have the accessible name to allow screen readers to correctly announce them.</span></span>

<span data-ttu-id="5ffbe-122">Para corregir este error, establezca el nombre accesible de una de las siguientes maneras (en orden de preferencia).</span><span class="sxs-lookup"><span data-stu-id="5ffbe-122">To fix this error, set the accessible name in one of the following ways (listed in the order of preference).</span></span>

-   <span data-ttu-id="5ffbe-123">Campos de formulario: Use la etiqueta **etiqueta** y establezca el atributo **for** en el valor de **identificador** del campo de destino.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-123">Form fields: Use the **label** tag and set the **for** attribute to the **id** value of the target field.</span></span>
-   <span data-ttu-id="5ffbe-124">Botón imagen/imagen: establezca el atributo **Alt** .</span><span class="sxs-lookup"><span data-stu-id="5ffbe-124">Image/image button: Set the **alt** attribute.</span></span>
-   <span data-ttu-id="5ffbe-125">Botones: establezca el texto del título del botón.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-125">Buttons: Set the button caption text.</span></span>
-   <span data-ttu-id="5ffbe-126">Para cualquier elemento:</span><span class="sxs-lookup"><span data-stu-id="5ffbe-126">For any element:</span></span>
    -   <span data-ttu-id="5ffbe-127">atributo [**Aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : establézcalo en el valor de **identificador** del elemento que contiene la cadena de nombre accesible.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-127">[**aria-labelledby**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the **id** value of the element containing the accessible name string.</span></span>
    -   <span data-ttu-id="5ffbe-128">atributo [**de etiqueta Aria**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) : se establece en la cadena de nombre accesible.</span><span class="sxs-lookup"><span data-stu-id="5ffbe-128">[**aria-label**](https://developer.mozilla.org/docs/Web/Accessibility/ARIA) attribute: Set to the accessible name string.</span></span>
    -   <span data-ttu-id="5ffbe-129">atributo de [**título**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) : establézcalo en la cadena de nombre accesible (también puede crear una **información sobre herramientas**).</span><span class="sxs-lookup"><span data-stu-id="5ffbe-129">[**title**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/title) attribute: Set to the accessible name string (also create a **tooltip**).</span></span>

## <a name="example"></a><span data-ttu-id="5ffbe-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ffbe-130">Example</span></span>


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



 

 




