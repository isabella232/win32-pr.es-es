---
description: En este ejemplo de C, se ha \# analizado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un control InkPicture. En el ejemplo se usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.
ms.assetid: fc9a39c2-9e4b-4d22-a118-3d24544897dd
title: Ejemplo de formulario de papel digitalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d60e1d62a4e023ba38e9a1fd2c4890288a542d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716449"
---
# <a name="scanned-paper-form-sample"></a><span data-ttu-id="a5291-104">Ejemplo de formulario de papel digitalizado</span><span class="sxs-lookup"><span data-stu-id="a5291-104">Scanned Paper Form Sample</span></span>

<span data-ttu-id="a5291-105">En este ejemplo de C, se ha \# analizado un formulario de papel como un archivo PNG (Portable Network Graphics) y se ha especificado como imagen de fondo en tiempo de ejecución para un control [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a5291-105">In this C\# sample, a paper form has been scanned as a Portable Network Graphics (PNG) file and specified as the background image at run time for a [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span> <span data-ttu-id="a5291-106">En el ejemplo se usa un cuadro de mensaje para mostrar los resultados del reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="a5291-106">The sample uses a message box to display handwriting recognition results.</span></span>

<span data-ttu-id="a5291-107">El ejemplo incluye un archivo lenguaje de marcado extensible (XML) Formdata.xml.</span><span class="sxs-lookup"><span data-stu-id="a5291-107">The sample includes an Extensible Markup Language (XML) file, Formdata.xml.</span></span> <span data-ttu-id="a5291-108">El archivo XML contiene el nombre del archivo PNG.</span><span class="sxs-lookup"><span data-stu-id="a5291-108">The XML file contains the name of the PNG file.</span></span> <span data-ttu-id="a5291-109">También contiene `FieldInfo` elementos que definen regiones rectangulares en el formulario donde un usuario puede escribir entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="a5291-109">It also contains `FieldInfo` elements that define rectangular regions on the form where a user can enter ink.</span></span> <span data-ttu-id="a5291-110">La información en el `FieldInfo` elemento se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a5291-110">The information in the `FieldInfo` element is shown in the following example:</span></span>


```C++
    <FieldInfo>
        <Name>first name</Name>
        <Left>88</Left>
        <Top>65</Top>
        <Right>332</Right>
        <Bottom>94</Bottom>
    </FieldInfo>
```



<span data-ttu-id="a5291-111">Los elementos izquierdo, superior, derecho e inferior son definiciones de coordenadas de píxeles para cada campo.</span><span class="sxs-lookup"><span data-stu-id="a5291-111">The Left, Top, Right, and Bottom elements are definitions of pixel coordinates for each field.</span></span>

<span data-ttu-id="a5291-112">El ejemplo Inicializa un nuevo [conjunto](/dotnet/api/system.data.dataset?view=netcore-3.1) de datos con los datos contenidos en Formdata.xml:</span><span class="sxs-lookup"><span data-stu-id="a5291-112">The sample initializes a new [DataSet](/dotnet/api/system.data.dataset?view=netcore-3.1) with the data contained in Formdata.xml:</span></span>


```C++
    formData = new DataSet("FormData");
    formData.ReadXml("formdata.xml"); 
```



<span data-ttu-id="a5291-113">La imagen de formulario especificada en Formdata.xml se carga como el fondo del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a5291-113">The form image specified in Formdata.xml is loaded as the background of the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.BackgroundImage = 
        System.Drawing.Image.FromFile(
        (string) formData.Tables["FormData"].Rows[0]["Image"]);
```



<span data-ttu-id="a5291-114">A continuación, se habilita la recopilación de tinta para el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="a5291-114">Ink collection is then enabled for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control:</span></span>


```C++
    inkPicture1.InkEnabled = true;
```



## <a name="menu-event-handlers"></a><span data-ttu-id="a5291-115">Controladores de eventos de menú</span><span class="sxs-lookup"><span data-stu-id="a5291-115">Menu Event Handlers</span></span>

<span data-ttu-id="a5291-116">La aplicación incluye controladores de eventos de clic para todos los menús mostrados en la parte superior del formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-116">The application includes click event handlers for all of the menus displayed along the top of the form.</span></span>

### <a name="recognize-menu-item"></a><span data-ttu-id="a5291-117">Elemento de menú Recognize</span><span class="sxs-lookup"><span data-stu-id="a5291-117">Recognize Menu Item</span></span>

<span data-ttu-id="a5291-118">El controlador de eventos de clic en el menú reconocer deshabilita la recopilación de entradas manuscritas del control y comprueba si hay un reconocedor de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="a5291-118">The Recognize menu click event handler disables ink collection for the control and checks for a handwriting recognizer.</span></span> <span data-ttu-id="a5291-119">Si no hay ningún reconocedor instalado, se muestra un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a5291-119">If no recognizer is installed, a dialog box is displayed.</span></span> <span data-ttu-id="a5291-120">Un usuario debe hacer clic en la opción de menú tinta o lápiz para volver a habilitar el control para la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a5291-120">A user must then click the Ink or Pen menu option to re-enable the control for ink input.</span></span>

<span data-ttu-id="a5291-121">Si se instala un reconocedor, la `Recognize` función recupera los datos XML que especifican las coordenadas de píxel para cada campo de formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-121">If a recognizer is installed, the `Recognize` function retrieves the XML data that specifies pixel coordinates for each form field.</span></span> <span data-ttu-id="a5291-122">Las coordenadas se convierten en coordenadas de espacio de la tinta y se define un rectángulo para cada campo de formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-122">The coordinates are converted to ink space coordinates, and a rectangle is defined for each form field.</span></span> <span data-ttu-id="a5291-123">Una vez definidos los rectángulos, la función busca los trazos que se cruzan y se encuentran dentro de cada rectángulo.</span><span class="sxs-lookup"><span data-stu-id="a5291-123">After rectangles are defined, the function finds the strokes that intersect and lie within each rectangle.</span></span> <span data-ttu-id="a5291-124">Por último, realiza el reconocimiento de la tinta y muestra los resultados en un cuadro de mensaje.</span><span class="sxs-lookup"><span data-stu-id="a5291-124">Finally, it performs recognition on the ink and displays the results in a message box.</span></span>

### <a name="ink-menu-item"></a><span data-ttu-id="a5291-125">Elemento de menú de entrada manuscrita</span><span class="sxs-lookup"><span data-stu-id="a5291-125">Ink Menu Item</span></span>

<span data-ttu-id="a5291-126">El controlador de eventos de clic de menú de tinta habilita el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="a5291-126">The Ink menu click event handler enables the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control.</span></span>

### <a name="pen-menu-item"></a><span data-ttu-id="a5291-127">Elemento de menú de lápiz</span><span class="sxs-lookup"><span data-stu-id="a5291-127">Pen Menu Item</span></span>

<span data-ttu-id="a5291-128">El controlador de eventos Click del menú lápiz realiza las siguientes tareas:</span><span class="sxs-lookup"><span data-stu-id="a5291-128">The Pen menu click event handler performs the following tasks:</span></span>

-   <span data-ttu-id="a5291-129">Deshabilita la recopilación de entradas manuscritas del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) (que es necesario antes de cambiar la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="a5291-129">Disables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control (which is necessary before changing the [EditingMode](/previous-versions/ms582189(v=vs.100)) property).</span></span>
-   <span data-ttu-id="a5291-130">Establece la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) para recopilar la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="a5291-130">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to collect ink.</span></span>
-   <span data-ttu-id="a5291-131">Vuelve a habilitar la recopilación de entradas manuscritas del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) y activa o desactiva los menús de lápiz, seleccionar y borrador para indicar el modo activo.</span><span class="sxs-lookup"><span data-stu-id="a5291-131">Re-enables ink collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control and toggles the Pen, Select, and Eraser menus to indicate the active mode.</span></span>

### <a name="edit-menu-item"></a><span data-ttu-id="a5291-132">Editar elemento de menú</span><span class="sxs-lookup"><span data-stu-id="a5291-132">Edit Menu Item</span></span>

<span data-ttu-id="a5291-133">El controlador de eventos Click del menú edición es similar al controlador de eventos del menú pluma.</span><span class="sxs-lookup"><span data-stu-id="a5291-133">The Edit menu click event handler is similar to the Pen menu event handler.</span></span> <span data-ttu-id="a5291-134">Realiza las tareas siguientes:</span><span class="sxs-lookup"><span data-stu-id="a5291-134">It performs the following tasks:</span></span>

-   <span data-ttu-id="a5291-135">Deshabilita la recopilación de entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="a5291-135">Disables ink collection.</span></span>
-   <span data-ttu-id="a5291-136">Establece la propiedad [EditingMode](/previous-versions/ms582189(v=vs.100)) en **Select**, que permite al usuario realizar la selección de entradas manuscritas.</span><span class="sxs-lookup"><span data-stu-id="a5291-136">Sets the [EditingMode](/previous-versions/ms582189(v=vs.100)) property to **Select**, which enables the user to perform ink selection.</span></span>
-   <span data-ttu-id="a5291-137">Vuelve a habilitar la recopilación de entradas manuscritas y alterna los menús de pluma, edición y borrador para indicar el modo activo.</span><span class="sxs-lookup"><span data-stu-id="a5291-137">Re-enables ink collection and toggles the Pen, Edit, and Eraser menus to indicate the active mode.</span></span>

### <a name="eraser-menu-item"></a><span data-ttu-id="a5291-138">Elemento de menú de borrador</span><span class="sxs-lookup"><span data-stu-id="a5291-138">Eraser Menu Item</span></span>

<span data-ttu-id="a5291-139">El controlador de eventos de clic de menú de borrador establece el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) [EditingMode](/previous-versions/ms582189(v=vs.100)) en **Delete**, lo que permite al usuario borrar la tinta.</span><span class="sxs-lookup"><span data-stu-id="a5291-139">The Eraser menu click event handler sets the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control [EditingMode](/previous-versions/ms582189(v=vs.100)) to **Delete**, which enables a user to erase ink.</span></span> <span data-ttu-id="a5291-140">También alterna los elementos de menú de lápiz, edición y borrador.</span><span class="sxs-lookup"><span data-stu-id="a5291-140">It also toggles the Pen, Edit, and Eraser menu items.</span></span>

### <a name="clear-menu-item"></a><span data-ttu-id="a5291-141">Borrar elemento de menú</span><span class="sxs-lookup"><span data-stu-id="a5291-141">Clear Menu Item</span></span>

<span data-ttu-id="a5291-142">El controlador de eventos de clic de menú borrar elimina la colección de [trazos](/previous-versions/ms552701(v=vs.100)) actual del control [InkPicture](/previous-versions/aa514604(v=msdn.10)) , con lo que se borran todas las entradas de lápiz del formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-142">The Clear menu click event handler deletes the current [Strokes](/previous-versions/ms552701(v=vs.100)) collection for the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control, thereby erasing all of the ink on the form.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="a5291-143">Cierre del formulario</span><span class="sxs-lookup"><span data-stu-id="a5291-143">Closing the Form</span></span>

<span data-ttu-id="a5291-144">En el código generado por el diseñador de Windows Forms, el control [InkPicture](/previous-versions/aa514604(v=msdn.10)) se agrega a la lista de componentes del formulario cuando se inicializa el formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-144">In the Windows Form Designer generated code, the [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="a5291-145">Cuando se cierra el formulario, se desecha el control InkPicture, así como los demás componentes del formulario, mediante el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="a5291-145">When the form closes, the InkPicture control is disposed, as well as the other components of the form, by the form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5291-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a5291-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5291-147">Control InkEdit</span><span class="sxs-lookup"><span data-stu-id="a5291-147">InkEdit Control</span></span>](inkedit-control.md)
</dt> <dt>

[<span data-ttu-id="a5291-148">InkPicture (control)</span><span class="sxs-lookup"><span data-stu-id="a5291-148">InkPicture Control</span></span>](inkpicture-control.md)
</dt> </dl>

 

 
