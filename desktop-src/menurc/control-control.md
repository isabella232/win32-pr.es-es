---
title: Control CONTROL
description: Define un control definido por el usuario.
ms.assetid: e5e7b7af-e2b0-41ff-b697-b9ea80e7c61f
keywords:
- CONTROLAR los menús de control y otros recursos
topic_type:
- apiref
api_name:
- CONTROL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 703f95778c66522d67e40a51293c8fb8fe956ecb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995187"
---
# <a name="control-control"></a><span data-ttu-id="1ce5b-104">Control CONTROL</span><span class="sxs-lookup"><span data-stu-id="1ce5b-104">CONTROL control</span></span>

<span data-ttu-id="1ce5b-105">Define un control definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-105">Defines a user-defined control.</span></span>

``` syntax
CONTROL text, id, class, style, x, y, width, height [, extended-style]
```

<dl> <dt>

<span data-ttu-id="1ce5b-106"><span id="class"></span><span id="CLASS"></span>*las*</span><span class="sxs-lookup"><span data-stu-id="1ce5b-106"><span id="class"></span><span id="CLASS"></span>*class*</span></span>
</dt> <dd>

<span data-ttu-id="1ce5b-107">Nombre redefinido, cadena de caracteres o valor entero sin signo de 16 bits que define la clase.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-107">Redefined name, character string, or a 16-bit unsigned integer value that defines the class.</span></span> <span data-ttu-id="1ce5b-108">Puede ser cualquiera de las clases de control. para obtener una lista de las clases de control, vea la primera lista que sigue a esta descripción.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-108">This can be any one of the control classes; for a list of the control classes, see the first list following this description.</span></span> <span data-ttu-id="1ce5b-109">Si el valor es un nombre redefinido proporcionado por la aplicación, debe ser una cadena entre comillas dobles (").</span><span class="sxs-lookup"><span data-stu-id="1ce5b-109">If the value is a redefined name supplied by the application, it must be a string enclosed in double quotation marks (").</span></span>

</dd> <dt>

<span data-ttu-id="1ce5b-110"><span id="style"></span><span id="STYLE"></span>*aplicar*</span><span class="sxs-lookup"><span data-stu-id="1ce5b-110"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="1ce5b-111">Nombre redefinido o valor entero que especifica el estilo del control dado.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-111">Redefined name or integer value that specifies the style of the given control.</span></span> <span data-ttu-id="1ce5b-112">El significado exacto de *Style* depende del valor de la *clase* .</span><span class="sxs-lookup"><span data-stu-id="1ce5b-112">The exact meaning of *style* depends on the *class* value.</span></span> <span data-ttu-id="1ce5b-113">En las secciones que siguen a esta descripción se muestran las clases de control y los estilos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-113">The sections following this description show the control classes and corresponding styles.</span></span>

</dd> </dl>

<span data-ttu-id="1ce5b-114">Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-114">For more information about the general syntax of a control statement, see [Common Control Parameters](common-control-parameters.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1ce5b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ce5b-115">Remarks</span></span>

<span data-ttu-id="1ce5b-116">Las seis clases de control posibles se describen en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-116">The six possible control classes are described in the following sections.</span></span>

### <a name="the-button-control-class"></a><span data-ttu-id="1ce5b-117">La clase de control Button</span><span class="sxs-lookup"><span data-stu-id="1ce5b-117">The Button Control Class</span></span>

<span data-ttu-id="1ce5b-118">Un control de botón es una pequeña ventana secundaria rectangular que el usuario puede activar o desactivar haciendo clic en él con el mouse.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-118">A button control is a small rectangular child window that the user can turn on or off by clicking it with the mouse.</span></span> <span data-ttu-id="1ce5b-119">Los controles de botón se pueden usar solo o en grupos, y se pueden etiquetar o mostrar sin texto.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-119">Button controls can be used alone or in groups, and can either be labeled or appear without text.</span></span> <span data-ttu-id="1ce5b-120">Los controles de botón normalmente cambian de apariencia cuando el usuario hace clic en ellos.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-120">Button controls typically change appearance when the user clicks them.</span></span>

<span data-ttu-id="1ce5b-121">Los estilos de botón se describen en el tema siguiente: [estilos de botón](../controls/button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-121">The button styles are described in the following topic: [Button Styles](../controls/button-styles.md).</span></span>

### <a name="the-combo-box-control-class"></a><span data-ttu-id="1ce5b-122">Clase de control de cuadro combinado</span><span class="sxs-lookup"><span data-stu-id="1ce5b-122">The Combo Box Control Class</span></span>

<span data-ttu-id="1ce5b-123">Los controles de cuadro combinado constan de un campo de selección similar a un control de edición y un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-123">Combo box controls consist of a selection field similar to an edit control plus a list box.</span></span> <span data-ttu-id="1ce5b-124">El cuadro de lista se puede mostrar en todo momento o se puede desplegar cuando el usuario selecciona un "cuadro de lista desplegable" junto al campo de selección.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-124">The list box may be displayed at all times or may be dropped down when the user selects a "pop box" next to the selection field.</span></span>

<span data-ttu-id="1ce5b-125">Dependiendo del estilo del cuadro combinado, el usuario puede o no puede editar el contenido del campo de selección.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-125">Depending on the style of the combo box, the user can or cannot edit the contents of the selection field.</span></span> <span data-ttu-id="1ce5b-126">Si el cuadro de lista está visible, si escribe caracteres en el cuadro de selección, se resaltará la primera entrada que coincida con los caracteres escritos.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-126">If the list box is visible, typing characters into the selection box will cause the first entry that matches the characters typed to be highlighted.</span></span> <span data-ttu-id="1ce5b-127">Por el contrario, al seleccionar un elemento en el cuadro de lista se muestra el texto seleccionado en el campo de selección.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-127">Conversely, selecting an item in the list box displays the selected text in the selection field.</span></span>

<span data-ttu-id="1ce5b-128">Los estilos de control de cuadro combinado se describen en el tema siguiente: [estilos de cuadro combinado](../controls/combo-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-128">The combo box control styles are described in the following topic: [Combo Box Styles](../controls/combo-box-styles.md).</span></span>

### <a name="the-edit-control-class"></a><span data-ttu-id="1ce5b-129">Clase Edit control</span><span class="sxs-lookup"><span data-stu-id="1ce5b-129">The Edit Control Class</span></span>

<span data-ttu-id="1ce5b-130">Un control de edición es una ventana secundaria rectangular en la que el usuario puede escribir texto desde el teclado.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-130">An edit control is a rectangular child window in which the user can enter text from the keyboard.</span></span> <span data-ttu-id="1ce5b-131">El usuario selecciona el control y le asigna el foco de entrada; para ello, hace clic en el mouse dentro de él o presiona la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-131">The user selects the control, and gives it the input focus, by clicking the mouse inside it or pressing the TAB key.</span></span> <span data-ttu-id="1ce5b-132">El usuario puede escribir texto cuando el control muestra un punto de inserción parpadeante.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-132">The user can enter text when the control displays a flashing insertion point.</span></span> <span data-ttu-id="1ce5b-133">El mouse se puede usar para mover el cursor y seleccionar los caracteres que se van a reemplazar, o para colocar el cursor para insertar caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-133">The mouse can be used to move the cursor and select characters to be replaced, or to position the cursor for inserting characters.</span></span> <span data-ttu-id="1ce5b-134">La tecla retroceso se puede utilizar para eliminar caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-134">The BACKSPACE key can be used to delete characters.</span></span>

<span data-ttu-id="1ce5b-135">Los controles de edición utilizan la fuente de punto fijo y muestran caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-135">Edit controls use the fixed-pitch font and display Unicode characters.</span></span> <span data-ttu-id="1ce5b-136">Expanden los caracteres de tabulación en tantos caracteres de espacio como sean necesarios para colocar el cursor en la siguiente posición de tabulación.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-136">They expand tab characters into as many space characters as are required to move the cursor to the next tab stop.</span></span> <span data-ttu-id="1ce5b-137">Se supone que las tabulaciones están en cada octava posición de carácter.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-137">Tab stops are assumed to be at every eighth character position.</span></span>

<span data-ttu-id="1ce5b-138">Los estilos de control de edición se describen en el tema siguiente: [Editar estilos de control](../controls/edit-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-138">The edit control styles are described in the following topic: [Edit Control Styles](../controls/edit-control-styles.md).</span></span>

### <a name="the-list-box-control-class"></a><span data-ttu-id="1ce5b-139">Clase de control de cuadro de lista</span><span class="sxs-lookup"><span data-stu-id="1ce5b-139">The List Box Control Class</span></span>

<span data-ttu-id="1ce5b-140">Los controles de cuadro de lista constan de una lista de cadenas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-140">List box controls consist of a list of character strings.</span></span> <span data-ttu-id="1ce5b-141">El control se usa siempre que una aplicación necesita presentar una lista de nombres, como nombres de archivo, que el usuario puede ver y seleccionar.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-141">The control is used whenever an application needs to present a list of names, such as filenames, that the user can view and select.</span></span> <span data-ttu-id="1ce5b-142">El usuario puede seleccionar una cadena seleccionando la cadena con el mouse y haciendo clic en un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-142">The user can select a string by pointing to the string with the mouse and clicking a mouse button.</span></span> <span data-ttu-id="1ce5b-143">Cuando se selecciona una cadena, se resalta y se pasa un mensaje de notificación a la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-143">When a string is selected, it is highlighted and a notification message is passed to the parent window.</span></span> <span data-ttu-id="1ce5b-144">Se puede usar una barra de desplazamiento con un control de cuadro de lista para desplazarse por las listas demasiado largas o demasiado anchas para la ventana de control.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-144">A scroll bar can be used with a list box control to scroll lists that are too long or too wide for the control window.</span></span>

<span data-ttu-id="1ce5b-145">Los estilos de control de cuadro de lista se describen en el tema siguiente: [estilos de cuadro de lista](../controls/list-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-145">The list box control styles are described in the following topic: [List Box Styles](../controls/list-box-styles.md).</span></span>

### <a name="the-scroll-bar-control-class"></a><span data-ttu-id="1ce5b-146">Clase de control Scroll-Bar</span><span class="sxs-lookup"><span data-stu-id="1ce5b-146">The Scroll-Bar Control Class</span></span>

<span data-ttu-id="1ce5b-147">Un control de barra de desplazamiento es un rectángulo que contiene un control de desplazamiento y tiene flechas de dirección en ambos extremos.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-147">A scroll-bar control is a rectangle that contains a scroll thumb and has direction arrows at both ends.</span></span> <span data-ttu-id="1ce5b-148">La barra de desplazamiento envía un mensaje de notificación a su elemento primario cada vez que el usuario hace clic con el mouse en el control.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-148">The scroll bar sends a notification message to its parent whenever the user clicks the mouse in the control.</span></span> <span data-ttu-id="1ce5b-149">El elemento primario es responsable de actualizar la posición del control, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-149">The parent is responsible for updating the thumb position, if necessary.</span></span> <span data-ttu-id="1ce5b-150">Los controles de barra de desplazamiento tienen la misma apariencia y función que las barras de desplazamiento usadas en las ventanas normales.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-150">Scroll-bar controls have the same appearance and function as the scroll bars used in ordinary windows.</span></span> <span data-ttu-id="1ce5b-151">Pero a diferencia de las barras de desplazamiento, los controles de barra de desplazamiento se pueden colocar en cualquier parte dentro de una ventana y usarse siempre que sea necesario para proporcionar la entrada de desplazamiento para una ventana.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-151">But unlike scroll bars, scroll-bar controls can be positioned anywhere within a window and used whenever needed to provide scrolling input for a window.</span></span>

<span data-ttu-id="1ce5b-152">Los estilos de barra de desplazamiento se describen en el tema siguiente: [estilos de control de barra de desplazamiento](../controls/scroll-bar-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-152">The scroll bar styles are described in the following topic: [Scroll Bar Control Styles](../controls/scroll-bar-control-styles.md).</span></span>

### <a name="the-static-control-class"></a><span data-ttu-id="1ce5b-153">La clase de control estática</span><span class="sxs-lookup"><span data-stu-id="1ce5b-153">The Static Control Class</span></span>

<span data-ttu-id="1ce5b-154">Los controles estáticos son campos de texto simples, cuadros y rectángulos que se pueden usar para etiquetar, mostrar o separar otros controles.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-154">Static controls are simple text fields, boxes, and rectangles that can be used to label, box, or separate other controls.</span></span> <span data-ttu-id="1ce5b-155">Los controles estáticos no toman ninguna entrada y no proporcionan ninguna salida.</span><span class="sxs-lookup"><span data-stu-id="1ce5b-155">Static controls take no input and provide no output.</span></span>

<span data-ttu-id="1ce5b-156">Los estilos de control estático se describen en el tema siguiente: [estilos de control estáticos](../controls/static-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1ce5b-156">The static control styles are described in the following topic: [Static Control Styles](../controls/static-control-styles.md).</span></span>

 

 