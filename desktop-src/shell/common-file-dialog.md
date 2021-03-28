---
description: A partir de Windows Vista, el cuadro de diálogo de elementos comunes reemplaza al cuadro de diálogo de archivos común más antiguo cuando se usa para abrir o guardar un archivo.
title: Cuadro de diálogo de elementos comunes
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f8846148-89a5-4b9b-ad68-56137a5c2f65
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 896514779b2ba3d11d3db0551f82e21f1d4120b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360168"
---
# <a name="common-item-dialog"></a><span data-ttu-id="86f06-103">Cuadro de diálogo de elementos comunes</span><span class="sxs-lookup"><span data-stu-id="86f06-103">Common Item Dialog</span></span>

<span data-ttu-id="86f06-104">A partir de Windows Vista, el cuadro de diálogo de elementos comunes reemplaza al cuadro de diálogo de archivos común más antiguo cuando se usa para abrir o guardar un archivo.</span><span class="sxs-lookup"><span data-stu-id="86f06-104">Starting with Windows Vista, the Common Item Dialog supersedes the older Common File Dialog when used to open or save a file.</span></span> <span data-ttu-id="86f06-105">El cuadro de diálogo de elementos comunes se usa en dos variaciones: el cuadro de diálogo **abrir** y el cuadro de diálogo **Guardar** .</span><span class="sxs-lookup"><span data-stu-id="86f06-105">The Common Item Dialog is used in two variations: the **Open** dialog and the **Save** dialog.</span></span> <span data-ttu-id="86f06-106">Estos dos cuadros de diálogo comparten la mayor parte de su funcionalidad, pero cada uno tiene sus propios métodos únicos.</span><span class="sxs-lookup"><span data-stu-id="86f06-106">These two dialogs share most of their functionality, but each has its own unique methods.</span></span>

<span data-ttu-id="86f06-107">Aunque esta nueva versión se denomina cuadro de diálogo de elementos comunes, se sigue llamando cuadro de diálogo de archivo común en la mayoría de la documentación.</span><span class="sxs-lookup"><span data-stu-id="86f06-107">While this newer version is named the Common Item Dialog, it continues to be called the Common File Dialog in most documentation.</span></span> <span data-ttu-id="86f06-108">A menos que esté tratando específicamente con una versión anterior de Windows, debe suponer que cualquier mención del cuadro de diálogo de archivo común hace referencia a este cuadro de diálogo de elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="86f06-108">Unless you are dealing specifically with an older version of Windows, you should assume that any mention of the Common File Dialog refers to this Common Item Dialog.</span></span>

<span data-ttu-id="86f06-109">Los temas siguientes se tratan aquí:</span><span class="sxs-lookup"><span data-stu-id="86f06-109">The following topics are discussed here:</span></span>

-   [<span data-ttu-id="86f06-110">IFileDialog, IFileOpenDialog y IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="86f06-110">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>](#ifiledialog-ifileopendialog-and-ifilesavedialog)
    -   [<span data-ttu-id="86f06-111">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="86f06-111">Sample Usage</span></span>](#sample-usage)
-   [<span data-ttu-id="86f06-112">Escuchar eventos desde el cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-112">Listening to Events from the Dialog</span></span>](#listening-to-events-from-the-dialog)
    -   [<span data-ttu-id="86f06-113">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="86f06-113">OnFileOk</span></span>](#onfileok)
    -   [<span data-ttu-id="86f06-114">OnShareViolation y OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="86f06-114">OnShareViolation and OnOverwrite</span></span>](#onshareviolation-and-onoverwrite)
-   [<span data-ttu-id="86f06-115">Personalización del cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-115">Customizing the Dialog</span></span>](#customizing-the-dialog)
    -   [<span data-ttu-id="86f06-116">Agregar opciones al botón Aceptar</span><span class="sxs-lookup"><span data-stu-id="86f06-116">Adding Options to the OK Button</span></span>](#adding-options-to-the-ok-button)
    -   [<span data-ttu-id="86f06-117">Responder a eventos en controles agregados</span><span class="sxs-lookup"><span data-stu-id="86f06-117">Responding to Events in Added Controls</span></span>](#responding-to-events-in-added-controls)
-   [<span data-ttu-id="86f06-118">Ejemplos completos</span><span class="sxs-lookup"><span data-stu-id="86f06-118">Full Samples</span></span>](#full-samples)
-   [<span data-ttu-id="86f06-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86f06-119">Related topics</span></span>](#related-topics)

## <a name="ifiledialog-ifileopendialog-and-ifilesavedialog"></a><span data-ttu-id="86f06-120">IFileDialog, IFileOpenDialog y IFileSaveDialog</span><span class="sxs-lookup"><span data-stu-id="86f06-120">IFileDialog, IFileOpenDialog, and IFileSaveDialog</span></span>

<span data-ttu-id="86f06-121">Windows Vista proporciona implementaciones de los cuadros de diálogo de **apertura** y **guardado** : CLSID \_ FileOpenDialog y CLSID \_ FileSaveDialog.</span><span class="sxs-lookup"><span data-stu-id="86f06-121">Windows Vista provides implementations of the **Open** and **Save** dialogs: CLSID\_FileOpenDialog and CLSID\_FileSaveDialog.</span></span> <span data-ttu-id="86f06-122">Estos cuadros de diálogo se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="86f06-122">Those dialog boxes are shown here.</span></span>

![captura de pantalla del cuadro de diálogo abrir](images/cid/openfiledialog.png)

![captura de pantalla del cuadro de diálogo Guardar como](images/cid/savefiledialog.png)

<span data-ttu-id="86f06-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) y [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) se heredan de [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) y comparten gran parte de su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="86f06-125">[**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) and [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog) inherit from [**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and share much of their functionality.</span></span> <span data-ttu-id="86f06-126">Además, el cuadro de diálogo **abrir** admite **IFileOpenDialog** y el cuadro de diálogo **Guardar** es compatible con **IFileSaveDialog**.</span><span class="sxs-lookup"><span data-stu-id="86f06-126">In addition, the **Open** dialog supports **IFileOpenDialog**, and the **Save** dialog supports **IFileSaveDialog**.</span></span>

<span data-ttu-id="86f06-127">La implementación del cuadro de diálogo de elementos comunes que se encuentra en Windows Vista proporciona varias ventajas con respecto a la implementación proporcionada en versiones anteriores:</span><span class="sxs-lookup"><span data-stu-id="86f06-127">The Common Item Dialog implementation found in Windows Vista provides several advantages over the implementation provided in earlier versions:</span></span>

-   <span data-ttu-id="86f06-128">Admite el uso directo del espacio de nombres del shell a través de [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) en lugar de usar rutas de acceso del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="86f06-128">Supports direct use of the Shell namespace through [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) instead of using file system paths.</span></span>
-   <span data-ttu-id="86f06-129">Habilita la personalización simple del cuadro de diálogo, como la configuración de la etiqueta en el botón **Aceptar** , sin necesidad de un procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="86f06-129">Enables simple customization of the dialog, such as setting the label on the **OK** button, without requiring a hook procedure.</span></span>
-   <span data-ttu-id="86f06-130">Admite la personalización más amplia del cuadro de diálogo mediante la adición de un conjunto de controles controlados por datos que funcionan sin una plantilla de cuadro de diálogo de Win32.</span><span class="sxs-lookup"><span data-stu-id="86f06-130">Supports more extensive customization of the dialog by the addition of a set of data-driven controls that operate without a Win32 dialog template.</span></span> <span data-ttu-id="86f06-131">Este esquema de personalización libera el proceso de llamada del diseño de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="86f06-131">This customization scheme frees the calling process from UI layout.</span></span> <span data-ttu-id="86f06-132">Dado que los cambios realizados en el diseño del cuadro de diálogo siguen utilizando este modelo de datos, la implementación del cuadro de diálogo no está asociada a la versión específica actual del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-132">Since any changes to the dialog design continue to use this data model, the dialog implementation is not tied to the specific current version of the dialog.</span></span>
-   <span data-ttu-id="86f06-133">Admite la notificación del llamador de eventos dentro del cuadro de diálogo, como el cambio de selección o el cambio de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="86f06-133">Supports caller notification of events within the dialog, such as selection change or file type change.</span></span> <span data-ttu-id="86f06-134">También permite que el proceso de llamada enlace determinados eventos en el cuadro de diálogo, como el análisis.</span><span class="sxs-lookup"><span data-stu-id="86f06-134">Also enables the calling process to hook certain events in the dialog, such as the parsing.</span></span>
-   <span data-ttu-id="86f06-135">Presenta nuevas características de diálogo como agregar lugares especificados por el autor de la llamada a la barra de **ubicaciones** .</span><span class="sxs-lookup"><span data-stu-id="86f06-135">Introduces new dialog features such as adding caller-specified places to the **Places** bar.</span></span>
-   <span data-ttu-id="86f06-136">En el cuadro de diálogo **Guardar** , los desarrolladores pueden aprovechar las nuevas características de metadatos del shell de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="86f06-136">In the **Save** dialog, developers can take advantage of new metadata features of the Windows Vista Shell.</span></span>

<span data-ttu-id="86f06-137">Además, los desarrolladores pueden optar por implementar las siguientes interfaces:</span><span class="sxs-lookup"><span data-stu-id="86f06-137">Additionally, developers can choose to implement the following interfaces:</span></span>

-   <span data-ttu-id="86f06-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) para recibir notificaciones de eventos en el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-138">[**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) to receive notifications of events within the dialog.</span></span>
-   <span data-ttu-id="86f06-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) para agregar controles al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-139">[**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) to add controls to the dialog.</span></span>
-   <span data-ttu-id="86f06-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) para recibir notificaciones de eventos en esos controles agregados.</span><span class="sxs-lookup"><span data-stu-id="86f06-140">[**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) to be notified of events in those added controls.</span></span>

<span data-ttu-id="86f06-141">El cuadro de diálogo **abrir** o **Guardar** devuelve un objeto [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) o [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) al proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="86f06-141">The **Open** or **Save** dialog returns an [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) or [**IShellItemArray**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitemarray) object to the calling process.</span></span> <span data-ttu-id="86f06-142">A continuación, el autor de la llamada puede usar un objeto **IShellItem** individual para obtener una ruta de acceso del sistema de archivos o para abrir un flujo en el elemento para leer o escribir información.</span><span class="sxs-lookup"><span data-stu-id="86f06-142">The caller can then use an individual **IShellItem** object to get a file system path or to open a stream on the item to read or write information.</span></span>

<span data-ttu-id="86f06-143">Las marcas y opciones disponibles para los nuevos métodos de diálogo son muy similares a las anteriores marcas de **OFN** que se encuentran en la estructura [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) y se usan en [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) y [**getSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="86f06-143">Flags and options available to the new dialog methods are very similar to the older **OFN** flags found in the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure and used in [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="86f06-144">Muchos de ellos son exactamente iguales, salvo que comienzan con un prefijo de FOS.</span><span class="sxs-lookup"><span data-stu-id="86f06-144">Many of them are exactly the same, except that they begin with an FOS prefix.</span></span> <span data-ttu-id="86f06-145">La lista completa se puede encontrar en los temas [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) y [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) .</span><span class="sxs-lookup"><span data-stu-id="86f06-145">The complete list can be found in the [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions) and [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) topics.</span></span> <span data-ttu-id="86f06-146">Los cuadros de diálogo **abrir** y **Guardar** se crean de forma predeterminada con las marcas más comunes.</span><span class="sxs-lookup"><span data-stu-id="86f06-146">**Open** and **Save** dialogs are created by default with the most common flags.</span></span> <span data-ttu-id="86f06-147">En el cuadro de diálogo **abrir** , es (FOS \_ PATHMUSTEXIST \| FOS \_ FILEMUSTEXIST \| FOS \_ NOCHANGEDIR) y para el cuadro de diálogo **Guardar** esto es (FOS \_ OVERWRITEPROMPT \| FOS \_ NOREADONLYRETURN \| FOS \_ PATHMUSTEXIST \| FOS \_ NOCHANGEDIR).</span><span class="sxs-lookup"><span data-stu-id="86f06-147">For the **Open** dialog, this is (FOS\_PATHMUSTEXIST \| FOS\_FILEMUSTEXIST \| FOS\_NOCHANGEDIR) and for the **Save** dialog this is (FOS\_OVERWRITEPROMPT \| FOS\_NOREADONLYRETURN \| FOS\_PATHMUSTEXIST \| FOS\_NOCHANGEDIR).</span></span>

<span data-ttu-id="86f06-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) y sus interfaces descendientes heredan de y extienden [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span><span class="sxs-lookup"><span data-stu-id="86f06-148">[**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog) and its descendant interfaces inherit from and extend [**IModalWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow).</span></span> <span data-ttu-id="86f06-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) toma como único parámetro el identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="86f06-149">[**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) takes as its only parameter the handle of the parent window.</span></span> <span data-ttu-id="86f06-150">Si **Show** se devuelve correctamente, hay un resultado válido.</span><span class="sxs-lookup"><span data-stu-id="86f06-150">If **Show** returns successfully, there is a valid result.</span></span> <span data-ttu-id="86f06-151">Si devuelve `HRESULT_FROM_WIN32(ERROR_CANCELLED)` , significa que el usuario canceló el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-151">If it returns `HRESULT_FROM_WIN32(ERROR_CANCELLED)`, it means the user canceled the dialog.</span></span> <span data-ttu-id="86f06-152">También podría devolver de forma legítima otro código de error, como **E \_ OUTOFMEMORY**.</span><span class="sxs-lookup"><span data-stu-id="86f06-152">It might also legitimately return another error code such as **E\_OUTOFMEMORY**.</span></span>

### <a name="sample-usage"></a><span data-ttu-id="86f06-153">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="86f06-153">Sample Usage</span></span>

<span data-ttu-id="86f06-154">En las secciones siguientes se muestra código de ejemplo para una variedad de tareas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-154">The following sections show example code for a variety of dialog tasks.</span></span>

-   [<span data-ttu-id="86f06-155">Uso básico</span><span class="sxs-lookup"><span data-stu-id="86f06-155">Basic Usage</span></span>](#basic-usage)
-   [<span data-ttu-id="86f06-156">Limitar los resultados a los elementos del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="86f06-156">Limiting Results to File System Items</span></span>](#limiting-results-to-file-system-items)
-   [<span data-ttu-id="86f06-157">Especificar tipos de archivo para un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-157">Specifying File Types for a Dialog</span></span>](#specifying-file-types-for-a-dialog)
-   [<span data-ttu-id="86f06-158">Controlar la carpeta predeterminada</span><span class="sxs-lookup"><span data-stu-id="86f06-158">Controlling the Default Folder</span></span>](#controlling-the-default-folder)
-   [<span data-ttu-id="86f06-159">Agregar elementos a la barra de ubicaciones</span><span class="sxs-lookup"><span data-stu-id="86f06-159">Adding Items to the Places Bar</span></span>](#adding-items-to-the-places-bar)
-   [<span data-ttu-id="86f06-160">Persistencia de estado</span><span class="sxs-lookup"><span data-stu-id="86f06-160">State Persistence</span></span>](#state-persistence)
-   [<span data-ttu-id="86f06-161">Funcionalidades de selección MultiSelect</span><span class="sxs-lookup"><span data-stu-id="86f06-161">Multiselect Capabilities</span></span>](#multiselect-capabilities)

<span data-ttu-id="86f06-162">La mayor parte del código de ejemplo puede encontrarse en el [ejemplo de cuadro de diálogo Windows SDK Common File](samples-commonfiledialog.md).</span><span class="sxs-lookup"><span data-stu-id="86f06-162">Most of the sample code can be found in the Windows SDK [Common File Dialog Sample](samples-commonfiledialog.md).</span></span>

### <a name="basic-usage"></a><span data-ttu-id="86f06-163">Uso básico</span><span class="sxs-lookup"><span data-stu-id="86f06-163">Basic Usage</span></span>

<span data-ttu-id="86f06-164">En el ejemplo siguiente se muestra cómo iniciar un cuadro de diálogo **abierto** .</span><span class="sxs-lookup"><span data-stu-id="86f06-164">The following example illustrates how to launch an **Open** dialog.</span></span> <span data-ttu-id="86f06-165">En este ejemplo, está restringido a los documentos de Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="86f06-165">In this example, it is restricted to Microsoft Word documents.</span></span>

> [!Note]  
> <span data-ttu-id="86f06-166">En varios ejemplos de este tema se usa la `CDialogEventHandler_CreateInstance` función auxiliar para crear una instancia de la implementación de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) .</span><span class="sxs-lookup"><span data-stu-id="86f06-166">Several examples in this topic use the `CDialogEventHandler_CreateInstance` helper function to create an instance of the [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) implementation.</span></span> <span data-ttu-id="86f06-167">Para usar esta función en su propio código, copie el código fuente de la `CDialogEventHandler_CreateInstance` función del [ejemplo de cuadro de diálogo de archivo común](samples-commonfiledialog.md), del que se toman todos los ejemplos de este tema.</span><span class="sxs-lookup"><span data-stu-id="86f06-167">To use this function in your own code, copy the source code for the `CDialogEventHandler_CreateInstance` function from the [Common File Dialog Sample](samples-commonfiledialog.md), from which all of the examples in this topic are taken.</span></span>

 


```C++
HRESULT BasicFileOpen()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
                    if (SUCCEEDED(hr))
                    {
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
                                if (SUCCEEDED(hr))
                                {
                                    // Show the dialog
                                    hr = pfd->Show(NULL);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Obtain the result once the user clicks 
                                        // the 'Open' button.
                                        // The result is an IShellItem object.
                                        IShellItem *psiResult;
                                        hr = pfd->GetResult(&psiResult);
                                        if (SUCCEEDED(hr))
                                        {
                                            // We are just going to print out the 
                                            // name of the file for sample sake.
                                            PWSTR pszFilePath = NULL;
                                            hr = psiResult->GetDisplayName(SIGDN_FILESYSPATH, 
                                                               &pszFilePath);
                                            if (SUCCEEDED(hr))
                                            {
                                                TaskDialog(NULL,
                                                           NULL,
                                                           L"CommonFileDialogApp",
                                                           pszFilePath,
                                                           NULL,
                                                           TDCBF_OK_BUTTON,
                                                           TD_INFORMATION_ICON,
                                                           NULL);
                                                CoTaskMemFree(pszFilePath);
                                            }
                                            psiResult->Release();
                                        }
                                    }
                                }
                            }
                        }
                    }
                }
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="limiting-results-to-file-system-items"></a><span data-ttu-id="86f06-168">Limitar los resultados a los elementos del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="86f06-168">Limiting Results to File System Items</span></span>

<span data-ttu-id="86f06-169">En el ejemplo siguiente, tomado de arriba, se muestra cómo restringir los resultados a los elementos del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="86f06-169">The following example, taken from above, demonstrates how to restrict results to file system items.</span></span> <span data-ttu-id="86f06-170">Tenga en cuenta que [**IFileDialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) agrega la nueva marca a un valor obtenido a través de [**IFileDialog:: GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span><span class="sxs-lookup"><span data-stu-id="86f06-170">Note that [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) adds the new flag to a value obtained through [**IFileDialog::GetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getoptions).</span></span> <span data-ttu-id="86f06-171">Éste es el método recomendado.</span><span class="sxs-lookup"><span data-stu-id="86f06-171">This is the recommended method.</span></span>


```C++
                // Set the options on the dialog.
                DWORD dwFlags;

                // Before setting, always get the options first in order 
                // not to override existing options.
                hr = pfd->GetOptions(&dwFlags);
                if (SUCCEEDED(hr))
                {
                    // In this case, get shell items only for file system items.
                    hr = pfd->SetOptions(dwFlags | FOS_FORCEFILESYSTEM);
```



### <a name="specifying-file-types-for-a-dialog"></a><span data-ttu-id="86f06-172">Especificar tipos de archivo para un cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-172">Specifying File Types for a Dialog</span></span>

<span data-ttu-id="86f06-173">Para establecer tipos de archivo específicos que el cuadro de diálogo puede controlar, use el método [**IFileDialog:: SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) .</span><span class="sxs-lookup"><span data-stu-id="86f06-173">To set specific file types that the dialog can handle, use the [**IFileDialog::SetFileTypes**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfiletypes) method.</span></span> <span data-ttu-id="86f06-174">Ese método acepta una matriz de estructuras [**COMDLG \_ FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) , cada una de las cuales representa un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="86f06-174">That method accepts an array of [**COMDLG\_FILTERSPEC**](/windows/desktop/api/Shtypes/ns-shtypes-comdlg_filterspec) structures, each of which represents a file type.</span></span>

<span data-ttu-id="86f06-175">El mecanismo de extensión predeterminado en un cuadro de diálogo no cambia de [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) y [**getSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span><span class="sxs-lookup"><span data-stu-id="86f06-175">The default extension mechanism in a dialog is unchanged from [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea) and [**GetSaveFileName**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea).</span></span> <span data-ttu-id="86f06-176">La extensión de nombre de archivo que se anexa al texto que escribe el usuario en el cuadro de edición nombre de archivo se inicializa al abrir el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-176">The file name extension that is appended to the text the user types in the file name edit box is initialized when the dialog opens.</span></span> <span data-ttu-id="86f06-177">Debe coincidir con el tipo de archivo predeterminado (que se selecciona al abrir el cuadro de diálogo).</span><span class="sxs-lookup"><span data-stu-id="86f06-177">It should match the default file type (that selected as the dialog opens).</span></span> <span data-ttu-id="86f06-178">Si el tipo de archivo predeterminado es " \* . \* " (todos los archivos), el archivo puede ser una extensión de su elección.</span><span class="sxs-lookup"><span data-stu-id="86f06-178">If the default file type is "\*.\*" (all files), the file can be an extension of your choice.</span></span> <span data-ttu-id="86f06-179">Si el usuario elige otro tipo de archivo, la extensión se actualiza automáticamente a la primera extensión de nombre de archivo asociada a ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="86f06-179">If the user chooses a different file type, the extension automatically updates to the first file name extension associated with that file type.</span></span> <span data-ttu-id="86f06-180">Si el usuario elige "" \* . \* (todos los archivos), la extensión vuelve a su valor original.</span><span class="sxs-lookup"><span data-stu-id="86f06-180">If the user chooses "\*.\*" (all files), then the extension reverts to its original value.</span></span>

<span data-ttu-id="86f06-181">En el ejemplo siguiente se muestra cómo se hizo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="86f06-181">The following example illustrates how this was done above.</span></span>


```C++
                        // Set the file types to display only. 
                        // Notice that this is a 1-based array.
                        hr = pfd->SetFileTypes(ARRAYSIZE(c_rgSaveTypes), c_rgSaveTypes);
                        if (SUCCEEDED(hr))
                        {
                            // Set the selected file type index to Word Docs for this example.
                            hr = pfd->SetFileTypeIndex(INDEX_WORDDOC);
                            if (SUCCEEDED(hr))
                            {
                                // Set the default extension to be ".doc" file.
                                hr = pfd->SetDefaultExtension(L"doc;docx");
```



### <a name="controlling-the-default-folder"></a><span data-ttu-id="86f06-182">Controlar la carpeta predeterminada</span><span class="sxs-lookup"><span data-stu-id="86f06-182">Controlling the Default Folder</span></span>

<span data-ttu-id="86f06-183">Casi cualquier carpeta en el espacio de nombres del shell se puede usar como carpeta predeterminada para el cuadro de diálogo (la carpeta que se presenta cuando el usuario elige abrir o guardar un archivo).</span><span class="sxs-lookup"><span data-stu-id="86f06-183">Almost any folder in the Shell namespace can be used as the default folder for the dialog (the folder presented when the user chooses to open or save a file).</span></span> <span data-ttu-id="86f06-184">Llame a [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) antes de llamar a [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="86f06-184">Call [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) to do so.</span></span>

<span data-ttu-id="86f06-185">La carpeta predeterminada es la carpeta en la que se inicia el cuadro de diálogo la primera vez que un usuario lo abre desde la aplicación.</span><span class="sxs-lookup"><span data-stu-id="86f06-185">The default folder is the folder in which the dialog starts the first time a user opens it from your application.</span></span> <span data-ttu-id="86f06-186">Después, el cuadro de diálogo se abrirá en la última carpeta que un usuario abrió o en la última carpeta que usó para guardar un elemento.</span><span class="sxs-lookup"><span data-stu-id="86f06-186">After that, the dialog will open in the last folder a user opened or the last folder they used to save an item.</span></span> <span data-ttu-id="86f06-187">Vea [persistencia del estado](#state-persistence) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="86f06-187">See [State Persistence](#state-persistence) for more details.</span></span>

<span data-ttu-id="86f06-188">Puede forzar que el cuadro de diálogo muestre siempre la misma carpeta cuando se abra, independientemente de la acción anterior del usuario, mediante una llamada a [**IFileDialog:: SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span><span class="sxs-lookup"><span data-stu-id="86f06-188">You can force the dialog to always show the same folder when it opens, regardless of previous user action, by calling [**IFileDialog::SetFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setfolder).</span></span> <span data-ttu-id="86f06-189">Sin embargo, no se recomienda hacerlo.</span><span class="sxs-lookup"><span data-stu-id="86f06-189">However, we do not recommended doing this.</span></span> <span data-ttu-id="86f06-190">Si llama a **SetFolder** antes de mostrar el cuadro de diálogo, no se muestra la ubicación más reciente en la que el usuario guardó o se abrió.</span><span class="sxs-lookup"><span data-stu-id="86f06-190">If you call **SetFolder** before you display the dialog box, the most recent location that the user saved to or opened from is not shown.</span></span> <span data-ttu-id="86f06-191">A menos que haya un motivo muy específico para este comportamiento, no es una experiencia de usuario buena o esperada y se debe evitar.</span><span class="sxs-lookup"><span data-stu-id="86f06-191">Unless there is a very specific reason for this behavior, it is not a good or expected user experience and should be avoided.</span></span> <span data-ttu-id="86f06-192">En casi todas las instancias, [**IFileDialog:: SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) es el mejor método.</span><span class="sxs-lookup"><span data-stu-id="86f06-192">In almost all instances, [**IFileDialog::SetDefaultFolder**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setdefaultfolder) is the better method.</span></span>

<span data-ttu-id="86f06-193">Al guardar un documento por primera vez en el cuadro de diálogo **Guardar** , debe seguir las mismas directrices para determinar la carpeta inicial como hizo en el cuadro de diálogo **abrir** .</span><span class="sxs-lookup"><span data-stu-id="86f06-193">When saving a document for the first time in the **Save** dialog, you should follow the same guidelines in determining the initial folder as you did in the **Open** dialog.</span></span> <span data-ttu-id="86f06-194">Si el usuario está editando un documento existente previamente, abra el cuadro de diálogo en la carpeta donde se almacena ese documento y rellene el cuadro de edición con el nombre del documento.</span><span class="sxs-lookup"><span data-stu-id="86f06-194">If the user is editing a previously existing document, open the dialog in the folder where that document is stored, and populate the edit box with that document's name.</span></span> <span data-ttu-id="86f06-195">Llame a [**IFileSaveDialog:: SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) con el elemento actual antes de llamar a [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span><span class="sxs-lookup"><span data-stu-id="86f06-195">Call [**IFileSaveDialog::SetSaveAsItem**](/windows/desktop/api/Shobjidl_core/nf-shobjidl_core-ifilesavedialog-setsaveasitem) with the current item prior to calling [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show).</span></span>

### <a name="adding-items-to-the-places-bar"></a><span data-ttu-id="86f06-196">Agregar elementos a la barra de ubicaciones</span><span class="sxs-lookup"><span data-stu-id="86f06-196">Adding Items to the Places Bar</span></span>

<span data-ttu-id="86f06-197">En el ejemplo siguiente se muestra la adición de elementos a la barra de **ubicaciones** :</span><span class="sxs-lookup"><span data-stu-id="86f06-197">The following example demonstrates the addition of items to the **Places** bar:</span></span>


```C++
HRESULT AddItemsToCommonPlaces()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Always use known folders instead of hard-coding physical file paths.
        // In this case we are using Public Music KnownFolder.
        IKnownFolderManager *pkfm = NULL;
        hr = CoCreateInstance(CLSID_KnownFolderManager, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pkfm));
        if (SUCCEEDED(hr))
        {
            // Get the known folder.
            IKnownFolder *pKnownFolder = NULL;
            hr = pkfm->GetFolder(FOLDERID_PublicMusic, &pKnownFolder);
            if (SUCCEEDED(hr))
            {
                // File Dialog APIs need an IShellItem that represents the location.
                IShellItem *psi = NULL;
                hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                if (SUCCEEDED(hr))
                {
                    // Add the place to the bottom of default list in Common File Dialog.
                    hr = pfd->AddPlace(psi, FDAP_BOTTOM);
                    if (SUCCEEDED(hr))
                    {
                        // Show the File Dialog.
                        hr = pfd->Show(NULL);
                        if (SUCCEEDED(hr))
                        {
                            //
                            // You can add your own code here to handle the results.
                            //
                        }
                    }
                    psi->Release();
                }
                pKnownFolder->Release();
            }
            pkfm->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



### <a name="state-persistence"></a><span data-ttu-id="86f06-198">Persistencia de estado</span><span class="sxs-lookup"><span data-stu-id="86f06-198">State Persistence</span></span>

<span data-ttu-id="86f06-199">Antes de Windows Vista, un estado, como la última carpeta visitada, se guardaba por proceso.</span><span class="sxs-lookup"><span data-stu-id="86f06-199">Prior to Windows Vista, a state, such as the last visited folder, was saved on a per-process basis.</span></span> <span data-ttu-id="86f06-200">Sin embargo, esa información se usó independientemente de la acción concreta.</span><span class="sxs-lookup"><span data-stu-id="86f06-200">However, that information was used regardless of the particular action.</span></span> <span data-ttu-id="86f06-201">Por ejemplo, una aplicación de edición de vídeo presentaría la misma carpeta en el cuadro de diálogo **representar como** en el cuadro de diálogo **importar medios** .</span><span class="sxs-lookup"><span data-stu-id="86f06-201">For example, a video editing application would present the same folder in the **Render As** dialog as is would in the **Import Media** dialog.</span></span> <span data-ttu-id="86f06-202">En Windows Vista puede ser más específico a través del uso de GUID.</span><span class="sxs-lookup"><span data-stu-id="86f06-202">In Windows Vista you can be more specific through the use of GUIDs.</span></span> <span data-ttu-id="86f06-203">Para asignar un **GUID** al cuadro de diálogo, llame a [**IFileDialog:: SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span><span class="sxs-lookup"><span data-stu-id="86f06-203">To assign a **GUID** to the dialog, call [**iFileDialog::SetClientGuid**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setclientguid).</span></span>

### <a name="multiselect-capabilities"></a><span data-ttu-id="86f06-204">Funcionalidades de selección MultiSelect</span><span class="sxs-lookup"><span data-stu-id="86f06-204">Multiselect Capabilities</span></span>

<span data-ttu-id="86f06-205">La funcionalidad de selección MultiSelect está disponible en el cuadro de diálogo **abrir** con el método [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) , tal como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="86f06-205">Multiselect functionality is available in the **Open** dialog using the [**GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) method as shown here.</span></span>


```C++
HRESULT MultiselectInvoke()
{
    IFileOpenDialog *pfd;
    
    // CoCreate the dialog object.
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));

    if (SUCCEEDED(hr))
    {
        DWORD dwOptions;
        // Specify multiselect.
        hr = pfd->GetOptions(&dwOptions);
        
        if (SUCCEEDED(hr))
        {
            hr = pfd->SetOptions(dwOptions | FOS_ALLOWMULTISELECT);
        }

        if (SUCCEEDED(hr))
        {
            // Show the Open dialog.
            hr = pfd->Show(NULL);

            if (SUCCEEDED(hr))
            {
                // Obtain the result of the user interaction.
                IShellItemArray *psiaResults;
                hr = pfd->GetResults(&psiaResults);
                
                if (SUCCEEDED(hr))
                {
                    //
                    // You can add your own code here to handle the results.
                    //
                    psiaResults->Release();
                }
            }
        }
        pfd->Release();
    }
    return hr;
}
```



## <a name="listening-to-events-from-the-dialog"></a><span data-ttu-id="86f06-206">Escuchar eventos desde el cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-206">Listening to Events from the Dialog</span></span>

<span data-ttu-id="86f06-207">Un proceso de llamada puede registrar una interfaz [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) con el cuadro de diálogo mediante los métodos [**IFileDialog:: Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) y [**IFileDialog:: Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="86f06-207">A calling process can register an [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents) interface with the dialog by using the [**IFileDialog::Advise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-advise) and [**IFileDialog::Unadvise**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-unadvise) methods as shown here.</span></span>

<span data-ttu-id="86f06-208">Esto se toma del ejemplo de [uso básico](#basic-usage) .</span><span class="sxs-lookup"><span data-stu-id="86f06-208">This is taken from the [Basic Usage](#basic-usage) sample.</span></span>


```C++
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents *pfde = NULL;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            DWORD dwCookie;
            hr = pfd->Advise(pfde, &dwCookie);
```



<span data-ttu-id="86f06-209">La mayor parte del procesamiento de cuadros de diálogo se situaría aquí.</span><span class="sxs-lookup"><span data-stu-id="86f06-209">The bulk of the dialog processing would be placed here.</span></span>


```C++
                // Unhook the event handler.
                pfd->Unadvise(dwCookie);
            }
            pfde->Release();
        }
        pfd->Release();
    }
    return hr;
}
```



<span data-ttu-id="86f06-210">El proceso de llamada puede usar eventos para la notificación cuando el usuario cambia la carpeta, el tipo de archivo o la selección.</span><span class="sxs-lookup"><span data-stu-id="86f06-210">The calling process can use events for notification when the user changes the folder, file type, or selection.</span></span> <span data-ttu-id="86f06-211">Estos eventos son especialmente útiles cuando el proceso de llamada agrega controles al cuadro de diálogo (vea [personalizar el cuadro de diálogo](#customizing-the-dialog)) y debe cambiar el estado de dichos controles en respuesta a estos eventos.</span><span class="sxs-lookup"><span data-stu-id="86f06-211">These events are particularly useful when the calling process has added controls to the dialog (see [Customizing the Dialog](#customizing-the-dialog)) and must change the state of those controls in reaction to these events.</span></span> <span data-ttu-id="86f06-212">Útil en todos los casos es la capacidad del proceso de llamada de proporcionar código personalizado para tratar situaciones como el uso compartido de infracciones, la sobrescritura de archivos o la determinación de si un archivo es válido antes de que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-212">Useful in all cases is the ability of the calling process to provide custom code to deal with situations such as sharing violations, overwriting files, or determining if a file is valid before the dialog closes.</span></span> <span data-ttu-id="86f06-213">Algunos de estos casos se describen en esta sección.</span><span class="sxs-lookup"><span data-stu-id="86f06-213">Some of those cases are described in this section.</span></span>

### <a name="onfileok"></a><span data-ttu-id="86f06-214">OnFileOk</span><span class="sxs-lookup"><span data-stu-id="86f06-214">OnFileOk</span></span>

<span data-ttu-id="86f06-215">Se llama a este método después de que el usuario elija un elemento, justo antes de que se cierre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-215">This method is called after the user chooses an item, just before the dialog closes.</span></span> <span data-ttu-id="86f06-216">A continuación, la aplicación puede llamar a [**IFileDialog:: GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) o [**IFileOpenDialog:: GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) tal como se haría una vez que el cuadro de diálogo se hubiera cerrado.</span><span class="sxs-lookup"><span data-stu-id="86f06-216">The application can then call [**IFileDialog::GetResult**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-getresult) or [**IFileOpenDialog::GetResults**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifileopendialog-getresults) as would be done once the dialog had closed.</span></span> <span data-ttu-id="86f06-217">Si el elemento elegido es aceptable, pueden devolver S \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="86f06-217">If the item chosen is acceptable, they can return S\_OK.</span></span> <span data-ttu-id="86f06-218">De lo contrario, devuelven S \_ false y muestran la interfaz de usuario que indica al usuario por qué el elemento elegido no es válido.</span><span class="sxs-lookup"><span data-stu-id="86f06-218">Otherwise, they return S\_FALSE and display UI that tells the user why the chosen item is not valid.</span></span> <span data-ttu-id="86f06-219">Si \_ se devuelve S false, el cuadro de diálogo no se cierra.</span><span class="sxs-lookup"><span data-stu-id="86f06-219">If S\_FALSE is returned, the dialog does not close.</span></span>

<span data-ttu-id="86f06-220">El proceso de llamada puede usar el identificador de ventana del propio cuadro de diálogo como elemento primario de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="86f06-220">The calling process can use the window handle of the dialog itself as the parent of the UI.</span></span> <span data-ttu-id="86f06-221">Ese identificador se puede obtener llamando primero a [**IOleWindow:: QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) y llamando a [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) con el identificador tal como se muestra en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="86f06-221">That handle can be obtained by first calling [**IOleWindow::QueryInterface**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) and then calling [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) with the handle as shown in this example.</span></span>


```C++
HRESULT CDialogEventHandler::OnFileOk(IFileDialog *pfd) 
{ 
    IShellItem *psiResult;
    HRESULT hr = pfd->GetResult(&psiResult);
    
    if (SUCCEEDED(hr))
    {
        SFGAOF attributes;
        hr = psiResult->GetAttributes(SFGAO_COMPRESSED, &attributes);
    
        if (SUCCEEDED(hr))
        {
            if (attributes & SFGAO_COMPRESSED)
            {
                // Accept the file.
                hr = S_OK;
            }
            else
            {
                // Refuse the file.
                hr = S_FALSE;
                
                _DisplayMessage(pfd, L"Not a compressed file.");
            }
        }
        psiResult->Release();
    }
    return hr;
};

HRESULT CDialogEventHandler::_DisplayMessage(IFileDialog *pfd, PCWSTR pszMessage)
{
    IOleWindow *pWindow;
    HRESULT hr = pfd->QueryInterface(IID_PPV_ARGS(&pWindow));
    
    if (SUCCEEDED(hr))
    {
        HWND hwndDialog;
        hr = pWindow->GetWindow(&hwndDialog);
    
        if (SUCCEEDED(hr))
        {
            MessageBox(hwndDialog, pszMessage, L"An error has occurred", MB_OK);
        }
        pWindow->Release();
    }
    return hr;
}
```



### <a name="onshareviolation-and-onoverwrite"></a><span data-ttu-id="86f06-222">OnShareViolation y OnOverwrite</span><span class="sxs-lookup"><span data-stu-id="86f06-222">OnShareViolation and OnOverwrite</span></span>

<span data-ttu-id="86f06-223">Si el usuario elige sobrescribir un archivo en el cuadro de diálogo **Guardar** o si un archivo que se está guardando o reemplazando está en uso y no se puede escribir en él (una infracción de uso compartido), la aplicación puede proporcionar funcionalidad personalizada para invalidar el comportamiento predeterminado del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-223">If the user chooses to overwrite a file in the **Save** dialog, or if a file being saved or replaced is in use and cannot be written to (a sharing violation), the application can provide custom functionality to override the default behavior of the dialog.</span></span> <span data-ttu-id="86f06-224">De forma predeterminada, al sobrescribir un archivo, el cuadro de diálogo muestra un mensaje que permite al usuario comprobar esta acción.</span><span class="sxs-lookup"><span data-stu-id="86f06-224">By default, when overwriting a file, the dialog displays a prompt allowing the user to verify this action.</span></span> <span data-ttu-id="86f06-225">Para las infracciones de uso compartido, de forma predeterminada el cuadro de diálogo muestra un mensaje de error, no se cierra y el usuario debe tomar otra decisión.</span><span class="sxs-lookup"><span data-stu-id="86f06-225">For sharing violations, by default the dialog displays an error message, it does not close, and the user is required to make another choice.</span></span> <span data-ttu-id="86f06-226">El proceso de llamada puede invalidar estos valores predeterminados y mostrar su propia interfaz de usuario si lo desea.</span><span class="sxs-lookup"><span data-stu-id="86f06-226">The calling process can override these defaults and display its own UI if desired.</span></span> <span data-ttu-id="86f06-227">Se puede indicar al cuadro de diálogo que rechace el archivo y que permanezca abierto o acepte el archivo y se cierre correctamente.</span><span class="sxs-lookup"><span data-stu-id="86f06-227">The dialog can be instructed to refuse the file and remain open or accept the file and close successfully.</span></span>

## <a name="customizing-the-dialog"></a><span data-ttu-id="86f06-228">Personalización del cuadro de diálogo</span><span class="sxs-lookup"><span data-stu-id="86f06-228">Customizing the Dialog</span></span>

<span data-ttu-id="86f06-229">Se pueden agregar varios controles al cuadro de diálogo sin proporcionar una plantilla de cuadro de diálogo de Win32.</span><span class="sxs-lookup"><span data-stu-id="86f06-229">A variety of controls can be added to the dialog without supplying a Win32 dialog template.</span></span> <span data-ttu-id="86f06-230">Estos controles incluyen PushButton, ComboBox, EditBox, CheckButton, listas de RadioButton, grupos, separadores y controles de texto estático.</span><span class="sxs-lookup"><span data-stu-id="86f06-230">These controls include PushButton, ComboBox, EditBox, CheckButton, RadioButton lists, Groups, Separators, and Static Text controls.</span></span> <span data-ttu-id="86f06-231">Llame a **QueryInterface** en el objeto de cuadro de diálogo ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)o [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) para obtener un puntero de [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) .</span><span class="sxs-lookup"><span data-stu-id="86f06-231">Call **QueryInterface** on the dialog object ([**IFileDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifiledialog), [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog), or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)) to obtain an [**IFileDialogCustomize**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) pointer.</span></span> <span data-ttu-id="86f06-232">Utilice esa interfaz para agregar controles.</span><span class="sxs-lookup"><span data-stu-id="86f06-232">Use that interface to add controls.</span></span> <span data-ttu-id="86f06-233">Cada control tiene asociado un identificador proporcionado por el autor de la llamada, así como un estado *visible* y *habilitado* que puede establecer el proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="86f06-233">Each control has an associated caller-supplied ID as well as a *visible* and *enabled* state that can be set by the calling process.</span></span> <span data-ttu-id="86f06-234">Algunos controles, como PushButton, también tienen texto asociado.</span><span class="sxs-lookup"><span data-stu-id="86f06-234">Some controls, such as PushButton, also have text associated with them.</span></span>

<span data-ttu-id="86f06-235">Se pueden agregar varios controles a un "grupo visual" que se mueve como una sola unidad en el diseño del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-235">Multiple controls can be added into a "visual group" that moves as a single unit in the layout of the dialog.</span></span> <span data-ttu-id="86f06-236">Los grupos pueden tener una etiqueta asociada.</span><span class="sxs-lookup"><span data-stu-id="86f06-236">Groups can have a label associated with them.</span></span>

<span data-ttu-id="86f06-237">Los controles solo se pueden agregar antes de que se muestre el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-237">Controls can be added only before the dialog is shown.</span></span> <span data-ttu-id="86f06-238">Sin embargo, una vez que se muestra el cuadro de diálogo, los controles pueden ocultarse o mostrarse como se desee, quizás en respuesta a la acción del usuario.</span><span class="sxs-lookup"><span data-stu-id="86f06-238">However, once the dialog is displayed, controls can be hidden or shown as desired, perhaps in response to user action.</span></span> <span data-ttu-id="86f06-239">En los siguientes ejemplos se muestra cómo agregar una lista de botones de radio al cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-239">The following examples show how to add a radio button list to the dialog.</span></span>


```C++
// Controls
#define CONTROL_GROUP           2000
#define CONTROL_RADIOBUTTONLIST 2
#define CONTROL_RADIOBUTTON1    1
#define CONTROL_RADIOBUTTON2    2       // It is OK for this to have the same ID
                    // as CONTROL_RADIOBUTTONLIST, because it 
                    // is a child control under CONTROL_RADIOBUTTONLIST


// This code snippet demonstrates how to add custom controls in the Common File Dialog.
HRESULT AddCustomControls()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    // Create a Visual Group.
                    hr = pfdc->StartVisualGroup(CONTROL_GROUP, L&quot;Sample Group&quot;);
                    if (SUCCEEDED(hr))
                    {
                        // Add a radio-button list.
                        hr = pfdc->AddRadioButtonList(CONTROL_RADIOBUTTONLIST);
                        if (SUCCEEDED(hr))
                        {
                            // Set the state of the added radio-button list.
                            hr = pfdc->SetControlState(CONTROL_RADIOBUTTONLIST, 
                                               CDCS_VISIBLE | CDCS_ENABLED);
                            if (SUCCEEDED(hr))
                            {
                                // Add individual buttons to the radio-button list.
                                hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                          CONTROL_RADIOBUTTON1,
                                                          L&quot;Change Title to ABC&quot;);
                                if (SUCCEEDED(hr))
                                {
                                    hr = pfdc->AddControlItem(CONTROL_RADIOBUTTONLIST,
                                                              CONTROL_RADIOBUTTON2,
                                                              L&quot;Change Title to XYZ&quot;);
                                    if (SUCCEEDED(hr))
                                    {
                                        // Set the default selection to option 1.
                                        hr = pfdc->SetSelectedControlItem(CONTROL_RADIOBUTTONLIST,
                                                                          CONTROL_RADIOBUTTON1);
                                    }
                                }
                            }
                        }
                        // End the visual group.
                        pfdc->EndVisualGroup();
                    }
                    pfdc->Release();
                }

                if (FAILED(hr))
                {
                    // Unadvise here in case we encounter failures 
                    // before we get a chance to show the dialog.
                    pfd->Unadvise(dwCookie);
                }
            }
            pfde->Release();
        }

        if (SUCCEEDED(hr))
        {
            // Now show the dialog.
            hr = pfd->Show(NULL);
            if (SUCCEEDED(hr))
            {
                //
                // You can add your own code here to handle the results.
                //
            }
            // Unhook the event handler.
            pfd->Unadvise(dwCookie);
        }
        pfd->Release();
    }
    return hr;
}
```





### <a name="adding-options-to-the-ok-button"></a><span data-ttu-id="86f06-240">Agregar opciones al botón Aceptar</span><span class="sxs-lookup"><span data-stu-id="86f06-240">Adding Options to the OK Button</span></span>

<span data-ttu-id="86f06-241">Del mismo modo, se pueden agregar opciones a los botones **abrir** o **Guardar** , que son el botón **Aceptar** para sus respectivos tipos de diálogo.</span><span class="sxs-lookup"><span data-stu-id="86f06-241">Similarly, choices can be added to the **Open** or **Save** buttons, which are the **OK** button for their respective dialog types.</span></span> <span data-ttu-id="86f06-242">Se puede tener acceso a las opciones a través de un cuadro de lista desplegable asociado al botón.</span><span class="sxs-lookup"><span data-stu-id="86f06-242">The options are accessible through a drop-down list box attached to the button.</span></span> <span data-ttu-id="86f06-243">El primer elemento de la lista se convierte en el texto del botón.</span><span class="sxs-lookup"><span data-stu-id="86f06-243">The first item in the list becomes the text for the button.</span></span> <span data-ttu-id="86f06-244">En el ejemplo siguiente se muestra cómo proporcionar un botón **abrir** con dos posibilidades: "abrir" y "abrir como solo lectura".</span><span class="sxs-lookup"><span data-stu-id="86f06-244">The following example shows how to provide an **Open** button with two possibilities: "Open" and "Open as read-only".</span></span>


```C++
// OpenChoices options
#define OPENCHOICES 0
#define OPEN 0
#define OPEN_AS_READONLY 1


HRESULT AddOpenChoices()
{
    // CoCreate the File Open Dialog object.
    IFileDialog *pfd = NULL;
    HRESULT hr = CoCreateInstance(CLSID_FileOpenDialog, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&pfd));
    if (SUCCEEDED(hr))
    {
        // Create an event handling object, and hook it up to the dialog.
        IFileDialogEvents   *pfde       = NULL;
        DWORD               dwCookie    = 0;
        hr = CDialogEventHandler_CreateInstance(IID_PPV_ARGS(&pfde));
        if (SUCCEEDED(hr))
        {
            // Hook up the event handler.
            hr = pfd->Advise(pfde, &dwCookie);
            if (SUCCEEDED(hr))
            {
                // Set up a Customization.
                IFileDialogCustomize *pfdc = NULL;
                hr = pfd->QueryInterface(IID_PPV_ARGS(&pfdc));
                if (SUCCEEDED(hr))
                {
                    hr = pfdc->EnableOpenDropDown(OPENCHOICES);
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, OPEN, L&quot;&Open&quot;);
                    }                    
                    if (SUCCEEDED(hr))
                    {
                        hr = pfdc->AddControlItem(OPENCHOICES, 
                                                OPEN_AS_READONLY, 
                                                L&quot;Open as &read-only&quot;);
                    }
                    if (SUCCEEDED(hr))
                    {
                        pfd->Show(NULL);
                    }
                }
                pfdc->Release();
            }
            pfd->Unadvise(dwCookie);
        }
        pfde->Release();
    }
    pfd->Release();
    return hr;
}
```





<span data-ttu-id="86f06-245">La elección del usuario puede comprobarse después de que el cuadro de diálogo vuelva del método [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) como lo haría para un ComboBox, o bien puede comprobarse como parte del control por [**IFileDialogEvents:: OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span><span class="sxs-lookup"><span data-stu-id="86f06-245">The user's choice can be verified after the dialog returns from the [**Show**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imodalwindow-show) method as you would for a ComboBox, or it can verified as part of the handling by [**IFileDialogEvents::OnFileOk**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifiledialogevents-onfileok).</span></span>

### <a name="responding-to-events-in-added-controls"></a><span data-ttu-id="86f06-246">Responder a eventos en controles agregados</span><span class="sxs-lookup"><span data-stu-id="86f06-246">Responding to Events in Added Controls</span></span>

<span data-ttu-id="86f06-247">El controlador de eventos proporcionado por el proceso de llamada puede implementar [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) además de [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span><span class="sxs-lookup"><span data-stu-id="86f06-247">The events handler provided by the calling process can implement [**IFileDialogControlEvents**](/windows/desktop/api/Shobjidl/nn-shobjidl-ifiledialogcontrolevents) in addition to [**IFileDialogEvents**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogevents).</span></span> <span data-ttu-id="86f06-248">**IFileDialogControlEvents** permite al proceso de llamada reaccionar a estos eventos:</span><span class="sxs-lookup"><span data-stu-id="86f06-248">**IFileDialogControlEvents** enables the calling process to react to these events:</span></span>

-   <span data-ttu-id="86f06-249">Clic en el pulsador</span><span class="sxs-lookup"><span data-stu-id="86f06-249">PushButton clicked</span></span>
-   <span data-ttu-id="86f06-250">Estado de CheckButton cambiado</span><span class="sxs-lookup"><span data-stu-id="86f06-250">CheckButton state changed</span></span>
-   <span data-ttu-id="86f06-251">Elemento seleccionado en un menú, cuadro combinado o lista de controles RadioButton</span><span class="sxs-lookup"><span data-stu-id="86f06-251">Item selected from a menu, ComboBox, or RadioButton list</span></span>
-   <span data-ttu-id="86f06-252">Control que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="86f06-252">Control activating.</span></span> <span data-ttu-id="86f06-253">Se envía cuando un menú está a punto de mostrar una lista desplegable, en caso de que el proceso de llamada desee cambiar los elementos de la lista.</span><span class="sxs-lookup"><span data-stu-id="86f06-253">This is sent when a menu is about to display a drop-down list, in case the calling process wants to change the items in the list.</span></span>

## <a name="full-samples"></a><span data-ttu-id="86f06-254">Ejemplos completos</span><span class="sxs-lookup"><span data-stu-id="86f06-254">Full Samples</span></span>

<span data-ttu-id="86f06-255">A continuación se muestran ejemplos de C++ completos y descargables del kit de desarrollo de software (SDK) de Windows que muestran el uso de e interacción con el cuadro de diálogo de elementos comunes.</span><span class="sxs-lookup"><span data-stu-id="86f06-255">The following are complete, downloadable C++ samples from the Windows Software Development Kit (SDK) which demonstrate the use of and interaction with the Common Item Dialog.</span></span>

-   [<span data-ttu-id="86f06-256">Ejemplo de cuadro de diálogo de archivo común</span><span class="sxs-lookup"><span data-stu-id="86f06-256">Common File Dialog Sample</span></span>](samples-commonfiledialog.md)
-   [<span data-ttu-id="86f06-257">Ejemplo de modos de cuadro de diálogo de archivo común</span><span class="sxs-lookup"><span data-stu-id="86f06-257">Common File Dialog Modes Sample</span></span>](samples-commonfiledialogmodes.md)

## <a name="related-topics"></a><span data-ttu-id="86f06-258">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86f06-258">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86f06-259">**IID \_ PPV \_ args**</span><span class="sxs-lookup"><span data-stu-id="86f06-259">**IID\_PPV\_ARGS**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args)
</dt> </dl>

 

 
