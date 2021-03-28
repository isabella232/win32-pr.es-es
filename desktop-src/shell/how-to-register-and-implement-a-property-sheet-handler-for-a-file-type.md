---
description: Cuando el usuario hace clic con el botón secundario en un miembro de un tipo de archivo para mostrar la hoja de propiedades propiedades, el shell llama a los controladores de hoja de propiedades que se registran para el tipo de archivo. Cada controlador puede Agregar una página personalizada a la hoja de propiedades predeterminada.
title: Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77cf54886f7819fa910da23393c6db488ddfee72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997700"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="ffef7-104">Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ffef7-104">How to Register and Implement a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="ffef7-105">Cuando el usuario hace clic con el botón secundario en un miembro de un tipo de archivo para mostrar la hoja de propiedades propiedades, el shell llama a los controladores de hoja de propiedades que se registran para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ffef7-105">When the user right-clicks a member of a file type to display the Properties property sheet, the Shell calls the property sheet handlers that are registered for the file type.</span></span> <span data-ttu-id="ffef7-106">Cada controlador puede Agregar una página personalizada a la hoja de propiedades predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ffef7-106">Each handler can add one custom page to the default property sheet.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ffef7-107">Aspectos que debe saber</span><span class="sxs-lookup"><span data-stu-id="ffef7-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ffef7-108">Tecnologías</span><span class="sxs-lookup"><span data-stu-id="ffef7-108">Technologies</span></span>

-   <span data-ttu-id="ffef7-109">Shell</span><span class="sxs-lookup"><span data-stu-id="ffef7-109">Shell</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ffef7-110">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ffef7-110">Prerequisites</span></span>

-   <span data-ttu-id="ffef7-111">Descripción de los menús contextuales</span><span class="sxs-lookup"><span data-stu-id="ffef7-111">An understanding of shortcut menus</span></span>

## <a name="instructions"></a><span data-ttu-id="ffef7-112">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="ffef7-112">Instructions</span></span>

### <a name="step-1-registering-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="ffef7-113">Paso 1: registrar un controlador de la hoja de propiedades para un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ffef7-113">Step 1: Registering a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="ffef7-114">Además del registro de modelo de objetos componentes (COM) normal, agregue una subclave **PropertySheetHandlers** a la subclave **shellex** de la clave ProgID de la aplicación asociada al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="ffef7-114">In addition to normal Component Object Model (COM) registration, add a **PropertySheetHandlers** subkey to the **shellex** subkey of the ProgID key of the application associated with the file type.</span></span> <span data-ttu-id="ffef7-115">Cree una subclave de **PropertySheetHandlers** con el nombre del controlador y establezca el valor predeterminado en la forma de cadena del GUID del identificador de clase (CLSID) del controlador de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffef7-115">Create a subkey of **PropertySheetHandlers** with the handler's name, and set the default value to the string form of the property sheet handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="ffef7-116">Para agregar más de una página a la hoja de propiedades, registre un controlador para cada página.</span><span class="sxs-lookup"><span data-stu-id="ffef7-116">To add more than one page to the property sheet, register a handler for each page.</span></span> <span data-ttu-id="ffef7-117">El número máximo de páginas que puede admitir una hoja de propiedades es 32.</span><span class="sxs-lookup"><span data-stu-id="ffef7-117">The maximum number of pages that a property sheet can support is 32.</span></span> <span data-ttu-id="ffef7-118">Para registrar varios controladores, cree una clave en la clave **shellex** para cada controlador, con el valor predeterminado establecido en el GUID de CLSID del controlador.</span><span class="sxs-lookup"><span data-stu-id="ffef7-118">To register multiple handlers, create a key under the **shellex** key for each handler, with the default value set to the handler's CLSID GUID.</span></span> <span data-ttu-id="ffef7-119">No es necesario crear un objeto distinto para cada controlador, lo que significa que varios controladores pueden tener el mismo valor de GUID.</span><span class="sxs-lookup"><span data-stu-id="ffef7-119">It is not necessary to create a distinct object for each handler, which means that multiple handlers can all have the same GUID value.</span></span> <span data-ttu-id="ffef7-120">Las páginas se mostrarán en el orden en que aparecen en **shellex**.</span><span class="sxs-lookup"><span data-stu-id="ffef7-120">The pages will be displayed in the order that their keys are listed under **shellex**.</span></span>

<span data-ttu-id="ffef7-121">En el ejemplo siguiente se muestra una entrada del registro que habilita dos controladores de extensión de la hoja de propiedades para un tipo de archivo. MYP de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ffef7-121">The following example illustrates a registry entry that enables two property sheet extension handlers for an example .myp file type.</span></span> <span data-ttu-id="ffef7-122">En este ejemplo, se usa un objeto independiente para cada página, pero también se puede usar un único objeto para ambos.</span><span class="sxs-lookup"><span data-stu-id="ffef7-122">In this example, a separate object is used for each page, but a single object could also be used for both.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {Page 1 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet1.dll
            ThreadingModel = Apartment
      {Page 2 Property Sheet Handler CLSID GUID}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet2.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         PropertySheetHandlers
            MyPropSheet1
               (Default) = {Page1 Property Sheet Handler CLSID GUID}
            MyPropSheet2
               (Default) = {Page2 Property Sheet Handler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-file-type"></a><span data-ttu-id="ffef7-123">Paso 2: implementar un controlador de hoja de propiedades para un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="ffef7-123">Step 2: Implementing a Property Sheet Handler for a File Type</span></span>

<span data-ttu-id="ffef7-124">Además de la implementación general que se describe en [Cómo funcionan los controladores de hoja de propiedades](propsheet-handlers.md), un controlador de hoja de propiedades para un tipo de archivo también debe tener una implementación adecuada de la interfaz [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="ffef7-124">In addition to the general implementation discussed in [How Property Sheet Handlers Work](propsheet-handlers.md), a property sheet handler for a file type must also have an appropriate implementation of the [**IShellPropSheetExt**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interface.</span></span> <span data-ttu-id="ffef7-125">Solo el método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) necesita una implementación que no sea de token.</span><span class="sxs-lookup"><span data-stu-id="ffef7-125">Only the [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method needs a nontoken implementation.</span></span> <span data-ttu-id="ffef7-126">El shell no llama a [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span><span class="sxs-lookup"><span data-stu-id="ffef7-126">The Shell does not call [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage).</span></span>

<span data-ttu-id="ffef7-127">El método [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) permite que un controlador de hoja de propiedades agregue una página a una hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffef7-127">The [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method allows a property sheet handler to add a page to a property sheet.</span></span> <span data-ttu-id="ffef7-128">El método tiene dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="ffef7-128">The method has two input parameters.</span></span> <span data-ttu-id="ffef7-129">El primero, *lpfnAddPage*, es un puntero a una función de devolución de llamada [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) que se usa para proporcionar al shell la información necesaria para agregar la página a la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffef7-129">The first, *lpfnAddPage*, is a pointer to an [*AddPropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnaddpropsheetpage) callback function that is used to provide the Shell with the information needed to add the page to the property sheet.</span></span> <span data-ttu-id="ffef7-130">El segundo, *lParam*, es un valor definido por el shell que no es procesado por el controlador.</span><span class="sxs-lookup"><span data-stu-id="ffef7-130">The second, *lParam*, is a Shell-defined value that is not processed by the handler.</span></span> <span data-ttu-id="ffef7-131">Simplemente se devuelve al shell cuando se llama a la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="ffef7-131">It is simply passed back to the Shell when the callback function is called.</span></span>

<span data-ttu-id="ffef7-132">El procedimiento general para implementar [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffef7-132">The general procedure for implementing [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) is as follows.</span></span>

<span data-ttu-id="ffef7-133">**Implementar el método AddPages**</span><span class="sxs-lookup"><span data-stu-id="ffef7-133">**Implementing the AddPages Method**</span></span>

1.  <span data-ttu-id="ffef7-134">Asigne los valores adecuados a los miembros de una estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="ffef7-134">Assign appropriate values to the members of a [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span> <span data-ttu-id="ffef7-135">En concreto:</span><span class="sxs-lookup"><span data-stu-id="ffef7-135">In particular:</span></span>
    -   <span data-ttu-id="ffef7-136">Asigne la variable que contiene el recuento de referencias del controlador al miembro **pcRefParent** .</span><span class="sxs-lookup"><span data-stu-id="ffef7-136">Assign the variable that holds the handler's reference count to the **pcRefParent** member.</span></span> <span data-ttu-id="ffef7-137">Esta práctica evita que el objeto de controlador se descargue mientras la hoja de propiedades todavía se está mostrando.</span><span class="sxs-lookup"><span data-stu-id="ffef7-137">This practice prevents the handler object from being unloaded while the property sheet is still being displayed.</span></span>
    -   <span data-ttu-id="ffef7-138">También puede implementar una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) y asignar su puntero a un miembro **pfnCallback** .</span><span class="sxs-lookup"><span data-stu-id="ffef7-138">You can also implement a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function and assign its pointer to a **pfnCallback** member.</span></span> <span data-ttu-id="ffef7-139">Se llama a esta función cuando se crea la página y cuando está a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="ffef7-139">This function is called when the page is created and when it is about to be destroyed.</span></span>
2.  <span data-ttu-id="ffef7-140">Cree el identificador de HPAGE de la página pasando la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) a la función [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) .</span><span class="sxs-lookup"><span data-stu-id="ffef7-140">Create the page's HPAGE handle by passing the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure to the [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) function.</span></span>
3.  <span data-ttu-id="ffef7-141">Llame a la función a la que apunta *lpfnAddPage*.</span><span class="sxs-lookup"><span data-stu-id="ffef7-141">Call the function that is pointed to by *lpfnAddPage*.</span></span> <span data-ttu-id="ffef7-142">Establezca su primer parámetro en el identificador de HPAGE que se creó en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="ffef7-142">Set its first parameter to the HPAGE handle that was created in the previous step.</span></span> <span data-ttu-id="ffef7-143">Establezca el segundo parámetro en el valor *lParam* que se pasó a [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) por el shell.</span><span class="sxs-lookup"><span data-stu-id="ffef7-143">Set its second parameter to the *lParam* value that was passed in to [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) by the Shell.</span></span>
4.  <span data-ttu-id="ffef7-144">Los mensajes asociados a la página se pasarán al procedimiento del cuadro de diálogo que se asignó al miembro **pfnDlgProc** de la estructura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) .</span><span class="sxs-lookup"><span data-stu-id="ffef7-144">Any messages associated with the page will be passed to the dialog box procedure that was assigned to the **pfnDlgProc** member of the [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v3) structure.</span></span>
5.  <span data-ttu-id="ffef7-145">Si ha asignado una función de devolución de llamada [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) a **pfnCallback**, se le llamará cuando la página esté a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="ffef7-145">If you assigned a [*PropSheetPageProc*](/windows/win32/api/prsht/nc-prsht-lpfnpspcallbacka) callback function to **pfnCallback**, it will be called when the page is about to be destroyed.</span></span> <span data-ttu-id="ffef7-146">Después, el controlador puede realizar las operaciones de limpieza necesarias, como liberar las referencias que contiene.</span><span class="sxs-lookup"><span data-stu-id="ffef7-146">Your handler can then perform any needed cleanup operations, such as releasing any references that it holds.</span></span>

<span data-ttu-id="ffef7-147">En el ejemplo de código siguiente se muestra una implementación de [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) simple.</span><span class="sxs-lookup"><span data-stu-id="ffef7-147">The following code sample illustrates a simple [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) implementation.</span></span>


```C++
STDMETHODIMP CShellPropSheetExt::AddPages(LPFNADDPROPSHEETPAGE, lpfnAddPage, LPARAM lParam)
{
    PROPSHEETPAGE  psp;
    HPROPSHEETPAGE hPage;

    psp.dwSize        = sizeof(psp);
    psp.dwFlags       = PSP_USEREFPARENT | PSP_USETITLE | PSP_USECALLBACK;
    psp.hInstance     = g_hInst;
    psp.pszTemplate   = MAKEINTRESOURCE(IDD_PAGEDLG);
    psp.hIcon         = 0;
    psp.pszTitle      = TEXT("Extension Page");
    psp.pfnDlgProc    = (DLGPROC)PageDlgProc;
    psp.pcRefParent   = &g_DllRefCount;
    psp.pfnCallback   = PageCallbackProc;
    psp.lParam        = (LPARAM)this;

    hPage = CreatePropertySheetPage(&psp);
            
    if(hPage) 
    {
        if(lpfnAddPage(hPage, lParam))
        {
            this->AddRef();
            return S_OK;
        }
        else
        {
            DestroyPropertySheetPage(hPage);
        }
    }
    else
    {
        return E_OUTOFMEMORY;
    }
    return E_FAIL;
}
```



<span data-ttu-id="ffef7-148">La variable **g \_ HINST** es el identificador de instancia de la dll y IDD \_ PAGEDLG es el identificador de recurso de la plantilla de cuadro de diálogo de la página.</span><span class="sxs-lookup"><span data-stu-id="ffef7-148">The **g\_hInst** variable is the instance handle to the DLL, and IDD\_PAGEDLG is the resource ID of the page's dialog box template.</span></span> <span data-ttu-id="ffef7-149">La función **PageDlgProc** es el procedimiento de cuadro de diálogo que controla los mensajes de la página.</span><span class="sxs-lookup"><span data-stu-id="ffef7-149">The **PageDlgProc** function is the dialog box procedure that handles the page's messages.</span></span> <span data-ttu-id="ffef7-150">La variable **g \_ DllRefCount** contiene el recuento de referencias del objeto.</span><span class="sxs-lookup"><span data-stu-id="ffef7-150">The **g\_DllRefCount** variable holds the object's reference count.</span></span> <span data-ttu-id="ffef7-151">El método [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) llama a [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) para incrementar el recuento.</span><span class="sxs-lookup"><span data-stu-id="ffef7-151">The [**AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages) method calls [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) to increment the count.</span></span> <span data-ttu-id="ffef7-152">Sin embargo, el recuento de referencias se libera mediante la función de devolución de llamada, **PageCallbackProc**, cuando la página está a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="ffef7-152">However, the reference count is released by the callback function, **PageCallbackProc**, when the page is about to be destroyed.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffef7-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffef7-153">Remarks</span></span>

<span data-ttu-id="ffef7-154">Para obtener información general sobre cómo registrar controladores de extensión de Shell, vea [crear controladores de extensión de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ffef7-154">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffef7-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffef7-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffef7-156">**IShellPropSheetExt**</span><span class="sxs-lookup"><span data-stu-id="ffef7-156">**IShellPropSheetExt**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext)
</dt> </dl>

 

 
