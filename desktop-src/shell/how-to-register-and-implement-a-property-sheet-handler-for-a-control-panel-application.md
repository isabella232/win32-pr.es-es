---
description: Muchas aplicaciones del panel de control muestran una hoja de propiedades para que los usuarios puedan ver y modificar diversas configuraciones del sistema y del dispositivo.
title: Cómo registrar e implementar un controlador de la hoja de propiedades para una aplicación del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909534"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7c370-103">Cómo registrar e implementar un controlador de la hoja de propiedades para una aplicación del panel de control</span><span class="sxs-lookup"><span data-stu-id="7c370-103">How to Register and Implement a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7c370-104">Muchas aplicaciones del panel de control muestran una hoja de propiedades para que los usuarios puedan ver y modificar diversas configuraciones del sistema y del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c370-104">Many Control Panel applications display a Properties property sheet to enable users to view and modify various device and system settings.</span></span> <span data-ttu-id="7c370-105">Dos de estas aplicaciones (mouse y pantalla) permiten a los controladores de hojas de propiedades reemplazar una o varias de sus páginas por una página personalizada.</span><span class="sxs-lookup"><span data-stu-id="7c370-105">Two of these applications—Mouse and Display—allow property sheet handlers to replace one or more of their pages with a custom page.</span></span> <span data-ttu-id="7c370-106">En la captura de pantalla siguiente se muestra la hoja de propiedades **del mouse** .</span><span class="sxs-lookup"><span data-stu-id="7c370-106">The following screen shot shows the **Mouse Properties** property sheet.</span></span>

![propiedades del mouse (hoja de propiedades)](images/propsheethandler3.jpg)

<span data-ttu-id="7c370-108">Los controladores de la hoja de propiedades de las aplicaciones del panel de control son similares a los de los tipos de archivo, con dos excepciones principales:</span><span class="sxs-lookup"><span data-stu-id="7c370-108">Property sheet handlers for Control Panel applications are similar to those for file types, with two primary exceptions:</span></span>

-   <span data-ttu-id="7c370-109">Los llama una aplicación del panel de control, no el shell.</span><span class="sxs-lookup"><span data-stu-id="7c370-109">They are called by a Control Panel application, not the Shell.</span></span>
-   <span data-ttu-id="7c370-110">Se registran de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="7c370-110">They are registered differently.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7c370-111">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="7c370-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7c370-112">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="7c370-112">Technologies</span></span>

-   <span data-ttu-id="7c370-113">Shell</span><span class="sxs-lookup"><span data-stu-id="7c370-113">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7c370-114">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7c370-114">Prerequisites</span></span>

-   <span data-ttu-id="7c370-115">Descripción del panel de control</span><span class="sxs-lookup"><span data-stu-id="7c370-115">An understanding of the Control Panel</span></span>
-   <span data-ttu-id="7c370-116">Descripción de los menús contextuales</span><span class="sxs-lookup"><span data-stu-id="7c370-116">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="7c370-117">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="7c370-117">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7c370-118">Paso 1: registrar un controlador de la hoja de propiedades para una aplicación del panel de control</span><span class="sxs-lookup"><span data-stu-id="7c370-118">Step 1: Registering a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7c370-119">Un controlador de la hoja de propiedades de la aplicación del panel de control debe estar registrado en la subclave del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7c370-119">A Control Panel application property sheet handler must be registered under the Control Panel subkey.</span></span> <span data-ttu-id="7c370-120">Esta clave puede estar en cualquiera de las dos ubicaciones, en función de si el controlador debe ser por usuario o por equipo.</span><span class="sxs-lookup"><span data-stu-id="7c370-120">This key can be in either of two locations, depending on whether the handler is to be per-user or per-computer.</span></span> <span data-ttu-id="7c370-121">En el caso del registro por usuario, la subclave del panel de control es **HKEY \_ Current \_ User** \\ **control panel**.</span><span class="sxs-lookup"><span data-stu-id="7c370-121">For per-user registration, the Control Panel subkey is **HKEY\_CURRENT\_USER**\\**Control Panel**.</span></span> <span data-ttu-id="7c370-122">La macro REGSTR \_ ruta de acceso \_ CONTROLPANEL tal y como se define en REGSTR. h puede usarse en el código en lugar del "panel de control".</span><span class="sxs-lookup"><span data-stu-id="7c370-122">The macro REGSTR\_PATH\_CONTROLPANEL as defined in Regstr.h can be used in code in place of "Control Panel".</span></span> <span data-ttu-id="7c370-123">En el caso del registro por equipo, la ubicación es:</span><span class="sxs-lookup"><span data-stu-id="7c370-123">For per-computer registration, the location is:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

<span data-ttu-id="7c370-124">Se puede hacer referencia a esta ruta de acceso en el código como HKEY \_ local \_ Machine \\ REGSTR \_ path \_ CONTROLSFOLDER mediante la \_ macro REGSTR path \_ CONTROLSFOLDER que se define en REGSTR. h.</span><span class="sxs-lookup"><span data-stu-id="7c370-124">This path can be referred to in code as HKEY\_LOCAL\_MACHINE\\REGSTR\_PATH\_CONTROLSFOLDER, using the REGSTR\_PATH\_CONTROLSFOLDER macro that is defined in Regstr.h.</span></span>

<span data-ttu-id="7c370-125">Las aplicaciones del panel de control que permiten a los controladores de hojas de propiedades reemplazar páginas tienen una subclave en la subclave del panel de control, con el nombre de la aplicación, como el mouse y la presentación.</span><span class="sxs-lookup"><span data-stu-id="7c370-125">The Control Panel applications that allow property sheet handlers to replace pages have a subkey under the Control Panel's subkey, named for the application, such as Mouse and Display.</span></span> <span data-ttu-id="7c370-126">La subclave de la aplicación debe tener una subclave **shellex** con una subclave **PropertySheetHandlers** .</span><span class="sxs-lookup"><span data-stu-id="7c370-126">The application's subkey must have a **shellex** subkey with a **PropertySheetHandlers** subkey.</span></span> <span data-ttu-id="7c370-127">Para registrar un controlador de la hoja de propiedades, agregue su GUID a la subclave **PropertySheetHandlers** asociada a la aplicación del panel de control.</span><span class="sxs-lookup"><span data-stu-id="7c370-127">To register a property sheet handler, add its GUID to the **PropertySheetHandlers** subkey that is associated with the Control Panel application.</span></span> <span data-ttu-id="7c370-128">Para ello, cree una subclave de la subclave **PropertySheetHandlers** , denominada para el controlador de la hoja de propiedades, y establezca su valor predeterminado en el formato de cadena del GUID del controlador.</span><span class="sxs-lookup"><span data-stu-id="7c370-128">To do so, create a subkey of the **PropertySheetHandlers** subkey, named for the property sheet handler, and set its default value to the string form of the handler's GUID.</span></span>

<span data-ttu-id="7c370-129">En el ejemplo siguiente se registra un controlador de la hoja de propiedades para la aplicación del panel de control del mouse por equipo.</span><span class="sxs-lookup"><span data-stu-id="7c370-129">The following example registers a property sheet handler for the Mouse Control Panel application on a per-computer basis.</span></span> <span data-ttu-id="7c370-130">Para registrarlo por usuario, reemplace **HKEY \_ local \_ Machine** \\ **REGSTR \_ path \_ CONTROLSFOLDER** por **HKEY \_ Current \_ User** \\ **REGSTR \_ rutaDeAcceso \_ CONTROLPANEL**.</span><span class="sxs-lookup"><span data-stu-id="7c370-130">To register it on a per-user basis, replace **HKEY\_LOCAL\_MACHINE**\\**REGSTR\_PATH\_CONTROLSFOLDER** with **HKEY\_CURRENT\_USER**\\**REGSTR\_PATH\_CONTROLPANEL**.</span></span>

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a><span data-ttu-id="7c370-131">Paso 2: implementar un controlador de la hoja de propiedades para una aplicación del panel de control</span><span class="sxs-lookup"><span data-stu-id="7c370-131">Step 2: Implementing a Property Sheet Handler for a Control Panel Application</span></span>

<span data-ttu-id="7c370-132">El procedimiento para implementar un controlador de la hoja de propiedades del panel de control es muy similar al que se describe en [Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="7c370-132">The procedure for implementing a Control Panel property sheet handler is very similar to that discussed in [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span> <span data-ttu-id="7c370-133">La principal diferencia es que ahora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) necesita una implementación que no sea de token en lugar de [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="7c370-133">The primary difference is that now [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) needs a nontoken implementation instead of [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span>

<span data-ttu-id="7c370-134">Cuando una aplicación del panel de control está a punto de mostrar su hoja de propiedades, llama una vez al método [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del controlador de la hoja de propiedades para cada página que se puede reemplazar.</span><span class="sxs-lookup"><span data-stu-id="7c370-134">When a Control Panel application is about to display its property sheet, it calls the property sheet handler's [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) method once for each page that can be replaced.</span></span> <span data-ttu-id="7c370-135">El parámetro *uPageID* se establece en el identificador de la página.</span><span class="sxs-lookup"><span data-stu-id="7c370-135">The *uPageID* parameter is set to the page's ID.</span></span> <span data-ttu-id="7c370-136">Los identificadores de las páginas disponibles se definen en Cplext. h.</span><span class="sxs-lookup"><span data-stu-id="7c370-136">The IDs for the available pages are defined in Cplext.h.</span></span> <span data-ttu-id="7c370-137">Los identificadores disponibles actualmente se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c370-137">The currently available IDs are listed in the following table.</span></span> 

| <span data-ttu-id="7c370-138">Identificador de página</span><span class="sxs-lookup"><span data-stu-id="7c370-138">Page ID</span></span>                      | <span data-ttu-id="7c370-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c370-139">Description</span></span>         | <span data-ttu-id="7c370-140">Aplicación del panel de control</span><span class="sxs-lookup"><span data-stu-id="7c370-140">Control Panel application</span></span> |
|------------------------------|---------------------|---------------------------|
| <span data-ttu-id="7c370-141">\_botones del mouse CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="7c370-141">CPLPAGE\_MOUSE\_BUTTONS</span></span>      | <span data-ttu-id="7c370-142">La página botones</span><span class="sxs-lookup"><span data-stu-id="7c370-142">The Buttons page</span></span>    | <span data-ttu-id="7c370-143">Mouse</span><span class="sxs-lookup"><span data-stu-id="7c370-143">Mouse</span></span>                     |
| <span data-ttu-id="7c370-144">CPLPAGE \_ mouse \_ PTRMOTION</span><span class="sxs-lookup"><span data-stu-id="7c370-144">CPLPAGE\_MOUSE\_PTRMOTION</span></span>    | <span data-ttu-id="7c370-145">La página de movimiento</span><span class="sxs-lookup"><span data-stu-id="7c370-145">The Motion page</span></span>     | <span data-ttu-id="7c370-146">Mouse</span><span class="sxs-lookup"><span data-stu-id="7c370-146">Mouse</span></span>                     |
| <span data-ttu-id="7c370-147">\_rueda del mouse CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="7c370-147">CPLPAGE\_MOUSE\_WHEEL</span></span>        | <span data-ttu-id="7c370-148">La página rueda</span><span class="sxs-lookup"><span data-stu-id="7c370-148">The Wheel page</span></span>      | <span data-ttu-id="7c370-149">Mouse</span><span class="sxs-lookup"><span data-stu-id="7c370-149">Mouse</span></span>                     |
| <span data-ttu-id="7c370-150">\_velocidad del teclado de CPLPAGE \_</span><span class="sxs-lookup"><span data-stu-id="7c370-150">CPLPAGE\_KEYBOARD\_SPEED</span></span>     | <span data-ttu-id="7c370-151">Página velocidad</span><span class="sxs-lookup"><span data-stu-id="7c370-151">The Speed page</span></span>      | <span data-ttu-id="7c370-152">Keyboard</span><span class="sxs-lookup"><span data-stu-id="7c370-152">Keyboard</span></span>                  |
| <span data-ttu-id="7c370-153">CPLPAGE \_ Mostrar \_ fondo</span><span class="sxs-lookup"><span data-stu-id="7c370-153">CPLPAGE\_DISPLAY\_BACKGROUND</span></span> | <span data-ttu-id="7c370-154">Página de fondo</span><span class="sxs-lookup"><span data-stu-id="7c370-154">The Background page</span></span> | <span data-ttu-id="7c370-155">Pantalla</span><span class="sxs-lookup"><span data-stu-id="7c370-155">Display</span></span>                   |



 

## <a name="remarks"></a><span data-ttu-id="7c370-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c370-156">Remarks</span></span>

<span data-ttu-id="7c370-157">El procedimiento para crear y reemplazar una página es idéntico al de agregar una página.</span><span class="sxs-lookup"><span data-stu-id="7c370-157">The procedure for creating and replacing a page is identical to that for adding a page.</span></span> <span data-ttu-id="7c370-158">Para obtener más información, vea [Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span><span class="sxs-lookup"><span data-stu-id="7c370-158">For more information, see [How to Register and Implement a Property Sheet Handler for a File Type](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).</span></span>

 

 



