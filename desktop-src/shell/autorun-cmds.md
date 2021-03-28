---
description: Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun. inf. Una entrada consta de una clave y un valor.
ms.assetid: 5b8fd559-b1be-4552-a7be-19ad107855af
title: Entradas Autorun. inf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56d93244f177d107bddc720fab1d0c774fd94735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275248"
---
# <a name="autoruninf-entries"></a><span data-ttu-id="b8565-104">Entradas Autorun. inf</span><span class="sxs-lookup"><span data-stu-id="b8565-104">Autorun.inf Entries</span></span>

<span data-ttu-id="b8565-105">Este tema es una referencia para las entradas que se pueden usar en un archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="b8565-105">This topic is a reference for the entries that can be used in an Autorun.inf file.</span></span> <span data-ttu-id="b8565-106">Una entrada consta de una clave y un valor.</span><span class="sxs-lookup"><span data-stu-id="b8565-106">An entry consists of a key and a value.</span></span>

-   <span data-ttu-id="b8565-107">[\[Claves de ejecución automática \]](#autorun-keys)</span><span class="sxs-lookup"><span data-stu-id="b8565-107">[\[AutoRun\] Keys](#autorun-keys)</span></span>
    -   [<span data-ttu-id="b8565-108">action</span><span class="sxs-lookup"><span data-stu-id="b8565-108">action</span></span>](#parameters)
    -   [<span data-ttu-id="b8565-109">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="b8565-109">CustomEvent</span></span>](#customevent)
    -   [<span data-ttu-id="b8565-110">icono</span><span class="sxs-lookup"><span data-stu-id="b8565-110">icon</span></span>](#parameters)
    -   [<span data-ttu-id="b8565-111">label</span><span class="sxs-lookup"><span data-stu-id="b8565-111">label</span></span>](#parameters)
    -   [<span data-ttu-id="b8565-112">open</span><span class="sxs-lookup"><span data-stu-id="b8565-112">open</span></span>](#parameters)
    -   [<span data-ttu-id="b8565-113">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="b8565-113">UseAutoPlay</span></span>](#parameters)
    -   [<span data-ttu-id="b8565-114">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="b8565-114">shellexecute</span></span>](#shellexecute)
    -   [<span data-ttu-id="b8565-115">interfaz</span><span class="sxs-lookup"><span data-stu-id="b8565-115">shell</span></span>](#autoruninf-entries)
    -   [<span data-ttu-id="b8565-116">verbo de Shell \\</span><span class="sxs-lookup"><span data-stu-id="b8565-116">shell\\verb</span></span>](#shellverb)
-   <span data-ttu-id="b8565-117">[\[Claves de contenido \]](#content-keys)</span><span class="sxs-lookup"><span data-stu-id="b8565-117">[\[Content\] Keys](#content-keys)</span></span>
-   <span data-ttu-id="b8565-118">[\[Claves de ExclusiveContentPaths \]](#exclusivecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="b8565-118">[\[ExclusiveContentPaths\] Keys](#exclusivecontentpaths-keys)</span></span>
-   <span data-ttu-id="b8565-119">[\[Claves de IgnoreContentPaths \]](#ignorecontentpaths-keys)</span><span class="sxs-lookup"><span data-stu-id="b8565-119">[\[IgnoreContentPaths\] Keys](#ignorecontentpaths-keys)</span></span>
-   <span data-ttu-id="b8565-120">[\[Claves de DeviceInstall \]](#deviceinstall-keys)</span><span class="sxs-lookup"><span data-stu-id="b8565-120">[\[DeviceInstall\] Keys](#deviceinstall-keys)</span></span>
    -   [<span data-ttu-id="b8565-121">DriverPath</span><span class="sxs-lookup"><span data-stu-id="b8565-121">DriverPath</span></span>](#driverpath)

## <a name="autorun-keys"></a><span data-ttu-id="b8565-122">\[Claves de ejecución automática \]</span><span class="sxs-lookup"><span data-stu-id="b8565-122">\[AutoRun\] Keys</span></span>

-   [<span data-ttu-id="b8565-123">action</span><span class="sxs-lookup"><span data-stu-id="b8565-123">action</span></span>](#parameters)
-   [<span data-ttu-id="b8565-124">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="b8565-124">CustomEvent</span></span>](#customevent)
-   [<span data-ttu-id="b8565-125">icono</span><span class="sxs-lookup"><span data-stu-id="b8565-125">icon</span></span>](#parameters)
-   [<span data-ttu-id="b8565-126">label</span><span class="sxs-lookup"><span data-stu-id="b8565-126">label</span></span>](#parameters)
-   [<span data-ttu-id="b8565-127">open</span><span class="sxs-lookup"><span data-stu-id="b8565-127">open</span></span>](#parameters)
-   [<span data-ttu-id="b8565-128">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="b8565-128">UseAutoPlay</span></span>](#parameters)
-   [<span data-ttu-id="b8565-129">ShellExecute</span><span class="sxs-lookup"><span data-stu-id="b8565-129">shellexecute</span></span>](#shellexecute)
-   [<span data-ttu-id="b8565-130">interfaz</span><span class="sxs-lookup"><span data-stu-id="b8565-130">shell</span></span>](#autoruninf-entries)
-   [<span data-ttu-id="b8565-131">verbo de Shell \\</span><span class="sxs-lookup"><span data-stu-id="b8565-131">shell\\verb</span></span>](#shellverb)

### <a name="action"></a><span data-ttu-id="b8565-132">action</span><span class="sxs-lookup"><span data-stu-id="b8565-132">action</span></span>

<span data-ttu-id="b8565-133">La entrada de **acción** especifica el texto que se utiliza en el cuadro de diálogo reproducción automática del controlador que representa el programa especificado en la entrada [Open](#parameters) o [ShellExecute](#shellexecute) del archivo Autorun. inf del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-133">The **action** entry specifies the text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span> <span data-ttu-id="b8565-134">El valor se puede expresar como texto o como un recurso almacenado en un archivo binario.</span><span class="sxs-lookup"><span data-stu-id="b8565-134">The value can be expressed as either text or as a resource stored in a binary.</span></span>


```
action=ActionText
```




```
action=@[filepath\]filename,-resourceID
```



### <a name="parameters"></a><span data-ttu-id="b8565-135">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-135">Parameters</span></span>

-   <span data-ttu-id="b8565-136">*ActionText*</span><span class="sxs-lookup"><span data-stu-id="b8565-136">*ActionText*</span></span>

    <span data-ttu-id="b8565-137">Texto que se usa en el cuadro de diálogo reproducción automática del controlador que representa el programa especificado en la entrada [Open](#parameters) o [ShellExecute](#shellexecute) del archivo Autorun. inf del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-137">Text that is used in the Autoplay dialog for the handler representing the program specified in the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file.</span></span>

-   <span data-ttu-id="b8565-138">*filepath*</span><span class="sxs-lookup"><span data-stu-id="b8565-138">*filepath*</span></span>

    <span data-ttu-id="b8565-139">Cadena que contiene la ruta de acceso completa del directorio que contiene el archivo binario que contiene la cadena.</span><span class="sxs-lookup"><span data-stu-id="b8565-139">A string that contains the fully qualified path of the directory that contains the binary file containing the string.</span></span> <span data-ttu-id="b8565-140">Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-140">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="b8565-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="b8565-141">*filename*</span></span>

    <span data-ttu-id="b8565-142">Cadena que contiene el nombre del archivo binario.</span><span class="sxs-lookup"><span data-stu-id="b8565-142">A string that contains the binary file's name.</span></span>

-   <span data-ttu-id="b8565-143">*Identificador*</span><span class="sxs-lookup"><span data-stu-id="b8565-143">*resourceID*</span></span>

    <span data-ttu-id="b8565-144">IDENTIFICADOR de la cadena dentro del archivo binario.</span><span class="sxs-lookup"><span data-stu-id="b8565-144">The ID of the string within the binary file.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-145">Remarks</span></span>

<span data-ttu-id="b8565-146">La clave de **acción** solo se utiliza en Windows XP Service Pack 2 (SP2) o posterior.</span><span class="sxs-lookup"><span data-stu-id="b8565-146">The **action** key is only used in Windows XP Service Pack 2 (SP2) or later.</span></span> <span data-ttu-id="b8565-147">Solo se admite para las unidades de tipo unidad \_ extraíble y unidad \_ fija.</span><span class="sxs-lookup"><span data-stu-id="b8565-147">It is only supported for drives of type DRIVE\_REMOVABLE and DRIVE\_FIXED.</span></span> <span data-ttu-id="b8565-148">En el caso de la unidad \_ extraíble, se requiere la clave de **acción** .</span><span class="sxs-lookup"><span data-stu-id="b8565-148">In the case of DRIVE\_REMOVABLE, the **action** key is required.</span></span> <span data-ttu-id="b8565-149">Se omite un comando de **acción** en el archivo Autorun. inf de un CD de audio o un DVD de película, y estos medios continúan comportados como en Windows XP Service Pack 1 (SP1) y versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="b8565-149">An **action** command in the Autorun.inf file of an audio CD or movie DVD is ignored, and these media continue to behave as in Windows XP Service Pack 1 (SP1) and earlier.</span></span>

<span data-ttu-id="b8565-150">La cadena mostrada en el cuadro de diálogo reproducción automática se construye combinando el texto especificado en la entrada de **acción** con el nombre de texto codificado de forma rígida del proveedor, proporcionado por el shell.</span><span class="sxs-lookup"><span data-stu-id="b8565-150">The string displayed in the Autoplay dialog is constructed by combining the text specified in the **action** entry with hard-coded text naming the provider, provided by the Shell.</span></span> <span data-ttu-id="b8565-151">Se muestra el [icono](#parameters) junto a él.</span><span class="sxs-lookup"><span data-stu-id="b8565-151">The [icon](#parameters) is displayed next to it.</span></span> <span data-ttu-id="b8565-152">Esta entrada siempre aparece como la primera opción en el cuadro de diálogo reproducción automática y está seleccionada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="b8565-152">This entry always appears as the first option in the Autoplay dialog and is selected by default.</span></span> <span data-ttu-id="b8565-153">Si el usuario acepta la opción, se inicia la aplicación especificada por la entrada [Open](#parameters) o [ShellExecute](#shellexecute) en el archivo Autorun. inf del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-153">If the user accepts the option, the application specified by the [open](#parameters) or [shellexecute](#shellexecute) entry in the media's Autorun.inf file is launched.</span></span> <span data-ttu-id="b8565-154">La opción **siempre la acción seleccionada** no está disponible en esta situación.</span><span class="sxs-lookup"><span data-stu-id="b8565-154">The **Always do the selected action** option is not available in this situation.</span></span>

<span data-ttu-id="b8565-155">Las claves de [acción](#parameters) y [icono](#parameters) definen conjuntamente la representación de la aplicación que el usuario final verá en el cuadro de diálogo reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-155">The [action](#parameters) and [icon](#parameters) keys together define the representation of the application that is seen by the end user in the Autoplay dialog.</span></span> <span data-ttu-id="b8565-156">Deberían estar compuestas de forma que los usuarios puedan identificarlas fácilmente.</span><span class="sxs-lookup"><span data-stu-id="b8565-156">They should be composed in such a way that users can easily identify them.</span></span> <span data-ttu-id="b8565-157">Deben indicar la aplicación que se va a ejecutar, la compañía que la creó y cualquier personalización de marca asociada.</span><span class="sxs-lookup"><span data-stu-id="b8565-157">They should indicate the application to be run, the company that created it, and any associated branding.</span></span>

<span data-ttu-id="b8565-158">Por compatibilidad con versiones anteriores, la entrada de **acción** es opcional para los dispositivos de tipo Drive \_ fixed.</span><span class="sxs-lookup"><span data-stu-id="b8565-158">For backward compatibility, the **action** entry is optional for devices of type DRIVE\_FIXED.</span></span> <span data-ttu-id="b8565-159">Para este tipo, se usa una entrada predeterminada en el cuadro de diálogo reproducción automática si no hay ninguna entrada de **acción** en el archivo Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="b8565-159">For this type, a default entry is used in the Autoplay dialog if no **action** entry is present in the Autorun.inf file.</span></span>

<span data-ttu-id="b8565-160">La entrada de **acción** es obligatoria para los dispositivos de tipo unidad \_ extraíbles, que hasta ahora no tienen compatibilidad con Autorun. inf.</span><span class="sxs-lookup"><span data-stu-id="b8565-160">The **action** entry is mandatory for devices of type DRIVE\_REMOVABLE, which until now did not have Autorun.inf support.</span></span> <span data-ttu-id="b8565-161">Si no hay ninguna entrada de **acción** , se muestra el cuadro de diálogo reproducción automática, pero sin ninguna opción para iniciar el contenido adicional.</span><span class="sxs-lookup"><span data-stu-id="b8565-161">If no **action** entry is present, the Autoplay dialog is displayed but with no option to launch the additional content.</span></span>

### <a name="customevent"></a><span data-ttu-id="b8565-162">CustomEvent</span><span class="sxs-lookup"><span data-stu-id="b8565-162">CustomEvent</span></span>

<span data-ttu-id="b8565-163">La entrada **CustomEvent** especifica un evento de contenido personalizado de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-163">The **CustomEvent** entry specifies a custom AutoPlay content event.</span></span>


```
CustomEvent=CustomEventName
```



### <a name="parameters"></a><span data-ttu-id="b8565-164">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-164">Parameters</span></span>

-   <span data-ttu-id="b8565-165">*CustomEventName*</span><span class="sxs-lookup"><span data-stu-id="b8565-165">*CustomEventName*</span></span>

    <span data-ttu-id="b8565-166">Cadena de texto que contiene el nombre del evento de contenido de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-166">A text string containing the name of the AutoPlay content event.</span></span> <span data-ttu-id="b8565-167">El nombre no debe tener más de 100 caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="b8565-167">The name must be no more than 100 alphanumeric characters.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-168">Remarks</span></span>

<span data-ttu-id="b8565-169">Puede incluir un nombre de evento personalizado en el archivo Autorun. inf de un volumen.</span><span class="sxs-lookup"><span data-stu-id="b8565-169">You can include a custom event name in the Autorun.inf file of a volume.</span></span> <span data-ttu-id="b8565-170">Cuando la reproducción automática solicita al usuario una aplicación para usarla con el volumen, solo muestra las aplicaciones que se han registrado para el nombre de evento personalizado especificado.</span><span class="sxs-lookup"><span data-stu-id="b8565-170">When AutoPlay prompts the user for an application to use with the volume, it displays only applications that have registered for the specified custom event name.</span></span> <span data-ttu-id="b8565-171">Para obtener información sobre cómo registrar una aplicación como un controlador para el evento personalizado de contenido de reproducción automática, consulte [Inicio automático con reproducción automática](/previous-versions/windows/apps/hh452731(v=win.10)) o [registro de un controlador de eventos](how-to-register-an-event-handler.md).</span><span class="sxs-lookup"><span data-stu-id="b8565-171">For information on how you can register an application as a handler for your custom AutoPlay content event, see [Auto-launching with AutoPlay](/previous-versions/windows/apps/hh452731(v=win.10)) or [How to Register an Event Handler](how-to-register-an-event-handler.md).</span></span>

<span data-ttu-id="b8565-172">En el ejemplo siguiente se especifica el valor "MyContentOnArrival" como nuevo evento de contenido de reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-172">The following example specifies the value "MyContentOnArrival" as a new AutoPlay content event.</span></span>


```
CustomEvent=MyContentOnArrival
```



### <a name="icon"></a><span data-ttu-id="b8565-173">icon</span><span class="sxs-lookup"><span data-stu-id="b8565-173">icon</span></span>

<span data-ttu-id="b8565-174">La entrada **Icon** especifica un icono que representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8565-174">The **icon** entry specifies an icon which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
icon=iconfilename[,index]
```



### <a name="parameters"></a><span data-ttu-id="b8565-175">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-175">Parameters</span></span>

-   <span data-ttu-id="b8565-176">*IconFileName*</span><span class="sxs-lookup"><span data-stu-id="b8565-176">*iconfilename*</span></span>

    <span data-ttu-id="b8565-177">Nombre de un archivo. ico,. bmp,. exe o. dll que contiene la información del icono.</span><span class="sxs-lookup"><span data-stu-id="b8565-177">Name of an .ico, .bmp, .exe, or .dll file containing the icon information.</span></span> <span data-ttu-id="b8565-178">Si un archivo contiene más de un icono, también debe especificar un índice basado en cero del icono.</span><span class="sxs-lookup"><span data-stu-id="b8565-178">If a file contains more than one icon, you must also specify zero-based index of the icon.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-179">Remarks</span></span>

<span data-ttu-id="b8565-180">El icono, junto con la etiqueta, representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8565-180">The icon, together with the label, represents the AutoRun-enabled drive in the Windows user interface.</span></span> <span data-ttu-id="b8565-181">Por ejemplo, en el explorador de Windows, la unidad está representada por este icono en lugar del icono de la unidad estándar.</span><span class="sxs-lookup"><span data-stu-id="b8565-181">For instance, in Windows Explorer, the drive is represented by this icon instead of the standard drive icon.</span></span> <span data-ttu-id="b8565-182">El archivo del icono debe estar en el mismo directorio que el archivo especificado por el comando [abrir](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="b8565-182">The icon's file must be in the same directory as the file specified by the [open](#parameters) command.</span></span>

<span data-ttu-id="b8565-183">En el ejemplo siguiente se especifica el segundo icono del archivo de MyProg.exe.</span><span class="sxs-lookup"><span data-stu-id="b8565-183">The following example specifies the second icon in the MyProg.exe file.</span></span>


```
icon=MyProg.exe,1
```



### <a name="label"></a><span data-ttu-id="b8565-184">etiqueta</span><span class="sxs-lookup"><span data-stu-id="b8565-184">label</span></span>

<span data-ttu-id="b8565-185">La entrada **etiqueta** especifica una etiqueta de texto que representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8565-185">The **label** entry specifies a text label which represents the AutoRun-enabled drive in the Windows user interface.</span></span>


```
label=LabelText
```



### <a name="parameters"></a><span data-ttu-id="b8565-186">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-186">Parameters</span></span>

-   <span data-ttu-id="b8565-187">*LabelText*</span><span class="sxs-lookup"><span data-stu-id="b8565-187">*LabelText*</span></span>

    <span data-ttu-id="b8565-188">Cadena de texto que contiene la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="b8565-188">A text string containing the label.</span></span> <span data-ttu-id="b8565-189">Puede contener espacios y no debe tener más de 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b8565-189">It can contain spaces and should be no longer than 32 characters.</span></span>

> [!Note]  
> <span data-ttu-id="b8565-190">Es posible colocar un valor en el parámetro **LabelText** que supere los 32 caracteres y no reciba ningún mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="b8565-190">It is possible to put a value in the **LabelText** parameter which exceeds 32 characters and receive no error message.</span></span> <span data-ttu-id="b8565-191">Sin embargo, el sistema solo muestra los primeros 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="b8565-191">However, the system only displays the first 32 characters.</span></span> <span data-ttu-id="b8565-192">Los caracteres situados después del 32 º se truncan y no se muestran.</span><span class="sxs-lookup"><span data-stu-id="b8565-192">Any characters after the 32nd are truncated and not displayed.</span></span> <span data-ttu-id="b8565-193">Por ejemplo, si el **LabelText** es el siguiente: etiqueta = "este CD está diseñado para ser el CD de música Ultimate".</span><span class="sxs-lookup"><span data-stu-id="b8565-193">For example, if the **LabelText** is as follows: label="This CD is designed to be the ultimate music CD."</span></span> <span data-ttu-id="b8565-194">se mostrará lo siguiente: "este CD está diseñado para ser el UL".</span><span class="sxs-lookup"><span data-stu-id="b8565-194">the following will be displayed, "This CD is designed to be the ul".</span></span>

 

### <a name="remarks"></a><span data-ttu-id="b8565-195">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-195">Remarks</span></span>

<span data-ttu-id="b8565-196">La etiqueta, junto con un icono, representa la unidad habilitada para la ejecución automática en la interfaz de usuario de Windows.</span><span class="sxs-lookup"><span data-stu-id="b8565-196">The label, together with an icon, represents the AutoRun-enabled drive in the Windows user interface.</span></span>

<span data-ttu-id="b8565-197">En el ejemplo siguiente se especifica el valor "mi etiqueta de unidad" como etiqueta de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-197">The following example specifies the value "My Drive Label" as the drive's label.</span></span>


```
label=My Drive Label
```



### <a name="open"></a><span data-ttu-id="b8565-198">abrir</span><span class="sxs-lookup"><span data-stu-id="b8565-198">open</span></span>

<span data-ttu-id="b8565-199">La entrada **Open** especifica la ruta de acceso y el nombre de archivo de la aplicación que se inicia automáticamente cuando un usuario inserta un disco en la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-199">The **open** entry specifies the path and file name of the application that AutoRun launches when a user inserts a disc in the drive.</span></span>


```
open=[exepath\]exefile [param1 [param2] ...] 
```



### <a name="parameters"></a><span data-ttu-id="b8565-200">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-200">Parameters</span></span>

-   <span data-ttu-id="b8565-201">*exefile*</span><span class="sxs-lookup"><span data-stu-id="b8565-201">*exefile*</span></span>

    <span data-ttu-id="b8565-202">Ruta de acceso completa de un archivo ejecutable que se ejecuta cuando se inserta el CD.</span><span class="sxs-lookup"><span data-stu-id="b8565-202">Fully qualified path of an executable file that runs when the CD is inserted.</span></span> <span data-ttu-id="b8565-203">Si solo se especifica un nombre de archivo, debe estar en el directorio raíz de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-203">If only a file name is specified, it must be in drive's root directory.</span></span> <span data-ttu-id="b8565-204">Para buscar el archivo en un subdirectorio, debe especificar una ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b8565-204">To locate the file in a subdirectory, you must specify a path.</span></span> <span data-ttu-id="b8565-205">También puede incluir uno o varios parámetros de la línea de comandos para pasarlos a la aplicación de inicio.</span><span class="sxs-lookup"><span data-stu-id="b8565-205">You can also include one or more command-line parameters to pass to the startup application.</span></span>

### <a name="useautoplay"></a><span data-ttu-id="b8565-206">UseAutoPlay</span><span class="sxs-lookup"><span data-stu-id="b8565-206">UseAutoPlay</span></span>

<span data-ttu-id="b8565-207">En Windows XP, la entrada **UseAutoPlay** especifica que se debe usar la reproducción automática en lugar de la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-207">On Windows XP, the **UseAutoPlay** entry specifies that AutoPlay should be used instead of AutoRun.</span></span>

<span data-ttu-id="b8565-208">En Windows Vista y versiones posteriores, esta entrada hace que se eliminen todas las acciones especificadas para la ejecución automática (mediante las entradas **Open** o **ShellExecute** ) en el cuadro de diálogo reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-208">On Windows Vista and later, this entry causes any actions specified for AutoRun (by using either the **open** or **shellexecute** entries) to be suppressed from the AutoPlay dialog.</span></span> <span data-ttu-id="b8565-209">Esta entrada no tiene ningún efecto en las versiones de Windows anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8565-209">This entry has no effect on versions of Windows earlier than Windows XP.</span></span>

<span data-ttu-id="b8565-210">En Windows 8 y versiones posteriores, si se especifica un valor de 0, se deshabilitará la reproducción automática para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8565-210">On Windows 8 and later, specifying a value of 0 will disable autoplay for this device.</span></span>

### <a name="parameters"></a><span data-ttu-id="b8565-211">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-211">Parameters</span></span>

<span data-ttu-id="b8565-212">Para usar esta opción, agregue una entrada para **UseAutoPlay** al archivo Autorun. inf y establezca la entrada igual a 1.</span><span class="sxs-lookup"><span data-stu-id="b8565-212">To use this option, add an entry for **UseAutoPlay** to the Autorun.inf file and set the entry equal to 1.</span></span> <span data-ttu-id="b8565-213">No se admite ningún otro valor en versiones de Windows anteriores a Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b8565-213">No other value is supported on versions of Windows earlier than Windows 8.</span></span>

<span data-ttu-id="b8565-214">En Windows 8 y versiones posteriores, especifique un valor de 0 para deshabilitar la reproducción automática para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8565-214">On Windows 8 and later, specify a value of 0 to disable autoplay for this device.</span></span>


```
UseAutoPlay=1
```



### <a name="remarks"></a><span data-ttu-id="b8565-215">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-215">Remarks</span></span>

<span data-ttu-id="b8565-216">Actualmente, **UseAutoPlay** solo es aplicable en Windows XP o posterior y solo en una unidad que [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determina como de tipo **unidad \_ CDROM**.</span><span class="sxs-lookup"><span data-stu-id="b8565-216">Currently, **UseAutoPlay** is applicable only on Windows XP or later and only on a drive that [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) determines to be of type **DRIVE\_CDROM**.</span></span>

<span data-ttu-id="b8565-217">Cuando se utiliza **UseAutoPlay** , cualquier acción especificada por las entradas **Open** o **ShellExecute** en Autorun. inf se omite en Windows XP y se omite en el cuadro de diálogo reproducción automática en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b8565-217">When **UseAutoPlay** is used, any action specified by the **open** or **shellexecute** entries in Autorun.inf is ignored on Windows XP and omitted from the AutoPlay dialog on Windows Vista.</span></span>

<span data-ttu-id="b8565-218">La ejecución automática se usa normalmente para ejecutar automáticamente o cargar algo incluido en el medio insertado, mientras que la reproducción automática presenta un cuadro de diálogo que incluye una lista de las acciones pertinentes que se pueden realizar y permite al usuario elegir qué acción debe realizar.</span><span class="sxs-lookup"><span data-stu-id="b8565-218">AutoRun is typically used to automatically run or load something contained on the inserted media, whereas AutoPlay presents a dialog that includes a list of relevant actions that may be taken and enables the user to choose which action to take.</span></span> <span data-ttu-id="b8565-219">Para obtener más información acerca de la diferencia entre la ejecución automática y la reproducción automática, consulte [crear una aplicación de CD-ROM habilitada para Autorun](autoplay.md) y [usar y configurar la reproducción automática](autoplay2k-using.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b8565-219">For more information about the difference between AutoRun and AutoPlay, see [Creating an AutoRun-enabled CD-ROM Application](autoplay.md) and [Using and Configuring AutoPlay](autoplay2k-using.md), respectively.</span></span>

### <a name="usage-example"></a><span data-ttu-id="b8565-220">Ejemplo de uso</span><span class="sxs-lookup"><span data-stu-id="b8565-220">Usage Example</span></span>

<span data-ttu-id="b8565-221">Un CD contiene tres archivos: Autorun. inf, Readme.txt y Music. WMA.</span><span class="sxs-lookup"><span data-stu-id="b8565-221">A CD contains three files: Autorun.inf, Readme.txt, and Music.wma.</span></span> <span data-ttu-id="b8565-222">Dependiendo de la versión de Windows en uso y de las opciones especificadas en Autorun. inf, el CD se puede controlar mediante la ejecución automática o la reproducción automática cuando se inserte (suponiendo que la ejecución automática o la reproducción automática esté habilitada para la unidad en la que se inserta el CD).</span><span class="sxs-lookup"><span data-stu-id="b8565-222">Depending on the version of Windows in use and options specified in Autorun.inf, the CD may be handled by either AutoRun or AutoPlay when it is inserted (assuming AutoRun/AutoPlay is enabled for the drive into which the CD is inserted).</span></span>

<span data-ttu-id="b8565-223">En primer lugar, considere un archivo Autorun. inf con el siguiente contenido, teniendo en cuenta que no se especifica **UseAutoPlay = 1** :</span><span class="sxs-lookup"><span data-stu-id="b8565-223">First, consider an Autorun.inf file with the following contents, noting that **UseAutoPlay=1** is not specified:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
```



<span data-ttu-id="b8565-224">La acción realizada por el shell al insertar este CD depende de la versión de Windows en uso:</span><span class="sxs-lookup"><span data-stu-id="b8565-224">The action taken by the Shell when this CD is inserted depends on the version of Windows in use:</span></span>

-   <span data-ttu-id="b8565-225">En Windows XP o versiones anteriores, este CD se administra mediante la ejecución automática cuando se inserta.</span><span class="sxs-lookup"><span data-stu-id="b8565-225">On Windows XP or earlier, this CD is handled by AutoRun when it is inserted.</span></span> <span data-ttu-id="b8565-226">En este caso, se lee la entrada **ShellExecute** y el shell invoca el controlador de archivos asociado a los archivos. txt. Normalmente, se abriría Readme.txt en el Bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="b8565-226">In this case, the **shellexecute** entry is read, and the Shell invokes the file handler associated with .txt files; typically this would open Readme.txt in Notepad.</span></span>
-   <span data-ttu-id="b8565-227">En Windows Vista, la presencia de un archivo Autorun. inf con una entrada **ShellExecute** hace que los medios se identifiquen como tipo de reproducción automática "Software and Games".</span><span class="sxs-lookup"><span data-stu-id="b8565-227">On Windows Vista, the presence of an Autorun.inf file with a **shellexecute** entry causes the media to be identified as AutoPlay type "Software and games".</span></span> <span data-ttu-id="b8565-228">En este caso, se muestra al usuario un cuadro de diálogo de reproducción automática que incluye la acción especificada por la entrada **ShellExecute** (presentada como "cargar Readme.txt" en el cuadro de diálogo), junto con las acciones predeterminadas asociadas a los medios de tipo "Software and Games".</span><span class="sxs-lookup"><span data-stu-id="b8565-228">In this case the user is presented with an AutoPlay dialog that includes the action specified by the **shellexecute** entry (presented as "Load Readme.txt" in the dialog), along with default actions associated with media of type "Software and games".</span></span>

<span data-ttu-id="b8565-229">Para indicar que se debe usar la reproducción automática en lugar de la ejecución automática en Windows XP, y que la acción especificada por la entrada ShellExecute de ejecución se debe suprimir en el cuadro de diálogo reproducción automática en Windows Vista, inserte **UseAutoPlay** en el archivo Autorun. inf de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="b8565-229">To indicate that AutoPlay should be used rather than AutoRun on Windows XP, and that the action specified by the AutoRun shellexecute entry should be suppressed from the AutoPlay dialog on Windows Vista, insert **UseAutoPlay** into the Autorun.inf file as follows:</span></span>


```
[AutoRun]
shellexecute="Readme.txt"
UseAutoPlay=1
```



<span data-ttu-id="b8565-230">Una vez más, la acción realizada por el shell al insertar este CD depende de la versión de Windows en uso.</span><span class="sxs-lookup"><span data-stu-id="b8565-230">Once again, the action taken by the Shell when this CD is inserted depends on the version of Windows in use.</span></span>

-   <span data-ttu-id="b8565-231">En las versiones de Windows anteriores a Windows XP, se sigue usando la ejecución automática y se realiza la acción especificada por **ShellExecute** , tal y como se describió anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b8565-231">On versions of Windows earlier than Windows XP, AutoRun is still used and the action specified by **shellexecute** is performed, as described previously.</span></span> <span data-ttu-id="b8565-232">(Tenga en cuenta que solo AutoRun está disponible en versiones de Windows anteriores a Windows XP).</span><span class="sxs-lookup"><span data-stu-id="b8565-232">(Note that only AutoRun is available on versions of Windows earlier than Windows XP.)</span></span>
-   <span data-ttu-id="b8565-233">En Windows XP, la entrada **UseAutoPlay** hace que se use la reproducción automática en lugar de la ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-233">On Windows XP, the **UseAutoPlay** entry causes AutoPlay to be used in place of AutoRun.</span></span> <span data-ttu-id="b8565-234">En este caso, la reproducción automática determina que el medio contiene un archivo Windows Media Audio (. WMA) y clasifica el contenido como "archivos de música".</span><span class="sxs-lookup"><span data-stu-id="b8565-234">In this case, AutoPlay determines that the media contains a Windows Media Audio (.wma) file and categorizes the content as "Music files".</span></span> <span data-ttu-id="b8565-235">Se presenta al usuario un cuadro de diálogo de reproducción automática que contiene controladores registrados para el tipo de medio de reproducción automática "archivos de música"; se omite la entrada ShellExecute de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-235">The user is presented with an AutoPlay dialog containing registered handlers for the "Music files" AutoPlay media type; the AutoRun shellexecute entry is ignored.</span></span>

### <a name="shellexecute"></a><span data-ttu-id="b8565-236">shellexecute</span><span class="sxs-lookup"><span data-stu-id="b8565-236">shellexecute</span></span>

[<span data-ttu-id="b8565-237">Versión 5,0.</span><span class="sxs-lookup"><span data-stu-id="b8565-237">Version 5.0.</span></span>](versions.md) <span data-ttu-id="b8565-238">La entrada **ShellExecute** especifica una aplicación o un archivo de datos que Autorun usará para llamar a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="b8565-238">The **shellexecute** entry specifies an application or data file that AutoRun will use to call [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>


```
shellexecute=[filepath\]filename[param1, [param2]...] 
```



### <a name="parameters"></a><span data-ttu-id="b8565-239">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-239">Parameters</span></span>

-   <span data-ttu-id="b8565-240">*filepath*</span><span class="sxs-lookup"><span data-stu-id="b8565-240">*filepath*</span></span>

    <span data-ttu-id="b8565-241">Cadena que contiene la ruta de acceso completa del directorio que contiene los datos o el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="b8565-241">A string that contains the fully qualified path of the directory that contains the data or executable file.</span></span> <span data-ttu-id="b8565-242">Si no se especifica ninguna ruta de acceso, el archivo debe estar en el directorio raíz de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-242">If no path is specified, the file must be in the drive's root directory.</span></span>

-   <span data-ttu-id="b8565-243">*filename*</span><span class="sxs-lookup"><span data-stu-id="b8565-243">*filename*</span></span>

    <span data-ttu-id="b8565-244">Cadena que contiene el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="b8565-244">A string that contains the file's name.</span></span> <span data-ttu-id="b8565-245">Si es un archivo ejecutable, se inicia.</span><span class="sxs-lookup"><span data-stu-id="b8565-245">If it is an executable file, it is launched.</span></span> <span data-ttu-id="b8565-246">Si es un archivo de datos, debe ser miembro de un tipo de [archivo](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="b8565-246">If it is a data file, it must be a member of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="b8565-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) inicia el comando predeterminado asociado al tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="b8565-247">[**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) launches the default command associated with the file type.</span></span>

-   <span data-ttu-id="b8565-248">*paramx*</span><span class="sxs-lookup"><span data-stu-id="b8565-248">*paramx*</span></span>

    <span data-ttu-id="b8565-249">Contiene los parámetros adicionales que se deben pasar a [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="b8565-249">Contains any additional parameters that should be passed to [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-250">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-250">Remarks</span></span>

<span data-ttu-id="b8565-251">Esta entrada es similar a [abrir](#parameters), pero le permite usar la información de [Asociación de archivos](fa-intro.md) para ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b8565-251">This entry is similar to [open](#parameters), but it allows you to use [file association](fa-intro.md) information to run the application.</span></span>

### <a name="shell"></a><span data-ttu-id="b8565-252">shell</span><span class="sxs-lookup"><span data-stu-id="b8565-252">shell</span></span>

<span data-ttu-id="b8565-253">La entrada de **Shell** especifica un comando predeterminado para el menú contextual de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-253">The **shell** entry specifies a default command for the drive's shortcut menu.</span></span>


```
shell=verb
```



### <a name="parameters"></a><span data-ttu-id="b8565-254">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-254">Parameters</span></span>

-   <span data-ttu-id="b8565-255">*Verbo*</span><span class="sxs-lookup"><span data-stu-id="b8565-255">*verb*</span></span>

    <span data-ttu-id="b8565-256">Verbo que corresponde al comando de menú.</span><span class="sxs-lookup"><span data-stu-id="b8565-256">The verb that corresponds to the menu command.</span></span> <span data-ttu-id="b8565-257">El verbo y su comando de menú asociado deben definirse en el archivo Autorun. inf con una entrada de [ \\ verbo de Shell](#shellverb) .</span><span class="sxs-lookup"><span data-stu-id="b8565-257">The verb and its associated menu command must be defined in the Autorun.inf file with a [shell\\verb](#shellverb) entry.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-258">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-258">Remarks</span></span>

<span data-ttu-id="b8565-259">Cuando un usuario hace clic con el botón secundario en el icono de la unidad, aparece un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-259">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="b8565-260">Si hay un archivo Autorun. inf, se toma el comando de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b8565-260">If an Autorun.inf file is present, the default shortcut menu command is taken from it.</span></span> <span data-ttu-id="b8565-261">Este comando también se ejecuta cuando el usuario hace doble clic en el icono de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-261">This command also executes when the user double-clicks the drive's icon.</span></span>

<span data-ttu-id="b8565-262">Para especificar el comando de menú contextual predeterminado, defina primero el verbo, la cadena de comando y el texto de menú con el [ \\ verbo de Shell](#shellverb).</span><span class="sxs-lookup"><span data-stu-id="b8565-262">To specify the default shortcut menu command, first define its verb, command string, and menu text with [shell\\verb](#shellverb).</span></span> <span data-ttu-id="b8565-263">A continuación, use Shell para convertirlo en el comando de menú contextual predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b8565-263">Then use shell to make it the default shortcut menu command.</span></span> <span data-ttu-id="b8565-264">De lo contrario, el texto del elemento de menú predeterminado será "reproducción automática", que inicia la aplicación especificada por la entrada [abierta](#parameters) .</span><span class="sxs-lookup"><span data-stu-id="b8565-264">Otherwise, the default menu item text will be "AutoPlay", which launches the application specified by the [open](#parameters) entry.</span></span>

### <a name="shellverb"></a><span data-ttu-id="b8565-265">verbo de Shell \\</span><span class="sxs-lookup"><span data-stu-id="b8565-265">shell\\verb</span></span>

<span data-ttu-id="b8565-266">La entrada de **\\ verbo de Shell** agrega un comando personalizado al menú contextual de la unidad.</span><span class="sxs-lookup"><span data-stu-id="b8565-266">The **shell\\verb** entry adds a custom command to the drive's shortcut menu.</span></span>


```
shell\verb\command=Filename.exe 
shell\verb=MenuText
```



### <a name="parameters"></a><span data-ttu-id="b8565-267">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-267">Parameters</span></span>

-   <span data-ttu-id="b8565-268">*Verbo*</span><span class="sxs-lookup"><span data-stu-id="b8565-268">*verb*</span></span>

    <span data-ttu-id="b8565-269">Verbo del comando de menú.</span><span class="sxs-lookup"><span data-stu-id="b8565-269">The menu command's verb.</span></span> <span data-ttu-id="b8565-270">La entrada de *_\\ comando_* de _verbo_ de **Shell \\** asocia el verbo con un archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="b8565-270">The **shell\\**_verb_*_\\command_* entry associates the verb with an executable file.</span></span> <span data-ttu-id="b8565-271">Los verbos no deben contener espacios incrustados.</span><span class="sxs-lookup"><span data-stu-id="b8565-271">Verbs must not contain embedded spaces.</span></span> <span data-ttu-id="b8565-272">De forma predeterminada, *Verb* es el texto que se muestra en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-272">By default, *verb* is the text that is displayed in the shortcut menu.</span></span>

-   <span data-ttu-id="b8565-273">*Filename.exe*</span><span class="sxs-lookup"><span data-stu-id="b8565-273">*Filename.exe*</span></span>

    <span data-ttu-id="b8565-274">Ruta de acceso y nombre de archivo de la aplicación que realiza la acción.</span><span class="sxs-lookup"><span data-stu-id="b8565-274">The path and file name of the application that performs the action.</span></span>

-   <span data-ttu-id="b8565-275">*MenuText*</span><span class="sxs-lookup"><span data-stu-id="b8565-275">*MenuText*</span></span>

    <span data-ttu-id="b8565-276">Este parámetro especifica el texto que se muestra en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-276">This parameter specifies the text that is displayed in the shortcut menu.</span></span> <span data-ttu-id="b8565-277">Si se omite, se muestra el *verbo* .</span><span class="sxs-lookup"><span data-stu-id="b8565-277">If it is omitted, *verb* is displayed.</span></span> <span data-ttu-id="b8565-278">*MenuText* puede ser una combinación de mayúsculas y minúsculas y puede contener espacios.</span><span class="sxs-lookup"><span data-stu-id="b8565-278">*MenuText* can be mixed-case and can contain spaces.</span></span> <span data-ttu-id="b8565-279">Puede establecer una tecla de método abreviado para el elemento de menú colocando una y comercial (&) delante de la letra.</span><span class="sxs-lookup"><span data-stu-id="b8565-279">You can set a shortcut key for the menu item by putting an ampersand (&) in front of the letter.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-280">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-280">Remarks</span></span>

<span data-ttu-id="b8565-281">Cuando un usuario hace clic con el botón secundario en el icono de la unidad, aparece un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-281">When a user right-clicks the drive icon, a shortcut menu appears.</span></span> <span data-ttu-id="b8565-282">La adición de entradas de **\\ verbo de Shell** al archivo Autorun. inf de la unidad permite agregar comandos a este menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-282">Adding **shell\\verb** entries to the drive's Autorun.inf file allows you to add commands to this shortcut menu.</span></span>

<span data-ttu-id="b8565-283">Esta entrada tiene dos partes, que deben estar en líneas independientes.</span><span class="sxs-lookup"><span data-stu-id="b8565-283">There are two parts to this entry, which must be on separate lines.</span></span> <span data-ttu-id="b8565-284">La primera parte es el *_\\ comando_* de _verbo_ de **Shell \\**.</span><span class="sxs-lookup"><span data-stu-id="b8565-284">The first part is **shell\\**_verb_*_\\command_*.</span></span> <span data-ttu-id="b8565-285">Es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8565-285">It is required.</span></span> <span data-ttu-id="b8565-286">Asocia una cadena, denominada *verbo*, a la aplicación para iniciar cuando se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="b8565-286">It associates a string, called a *verb*, with the application to launch when the command runs.</span></span> <span data-ttu-id="b8565-287">La segunda parte es la entrada del _verbo_ de **Shell \\**.</span><span class="sxs-lookup"><span data-stu-id="b8565-287">The second part is the **shell\\**_verb_ entry.</span></span> <span data-ttu-id="b8565-288">Es opcional.</span><span class="sxs-lookup"><span data-stu-id="b8565-288">It is optional.</span></span> <span data-ttu-id="b8565-289">Puede incluirlo para especificar el texto que se muestra en el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="b8565-289">You can include it to specify the text that displays in the shortcut menu.</span></span>

<span data-ttu-id="b8565-290">Para especificar un comando de menú contextual predeterminado, defina el verbo con el **\\ verbo de Shell** y conviértalo en el comando predeterminado con la entrada de [Shell](#autoruninf-entries) .</span><span class="sxs-lookup"><span data-stu-id="b8565-290">To specify a default shortcut menu command, define the verb with **shell\\verb**, and make it the default command with the [shell](#autoruninf-entries) entry.</span></span>

<span data-ttu-id="b8565-291">En el fragmento siguiente de Autorun. inf de ejemplo se asocia el verbo *readit* a la cadena de comando "Notepad ABC \\readme.txt".</span><span class="sxs-lookup"><span data-stu-id="b8565-291">The following sample Autorun.inf fragment associates the *readit* verb with the command string "Notepad abc\\readme.txt".</span></span> <span data-ttu-id="b8565-292">El texto del menú es "Read Me" y "m" se define como la tecla de método abreviado del elemento.</span><span class="sxs-lookup"><span data-stu-id="b8565-292">The menu text is "Read Me", and 'M' is defined as the item's shortcut key.</span></span> <span data-ttu-id="b8565-293">Cuando el usuario selecciona este comando, se abre el archivo dereadme.txt ABC de la unidad \\ con el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8565-293">When the user selects this command, the drive's abc\\readme.txt file opens with Microsoft Notepad.</span></span>


```
shell\readit\command=notepad abc\readme.txt 
shell\readit=Read &Me
```



## <a name="content-keys"></a><span data-ttu-id="b8565-294">\[Claves de contenido \]</span><span class="sxs-lookup"><span data-stu-id="b8565-294">\[Content\] Keys</span></span>

<span data-ttu-id="b8565-295">Hay tres claves de tipo de archivo: **MusicFiles**, **PictureFiles** y **videofiles**.</span><span class="sxs-lookup"><span data-stu-id="b8565-295">There are three file type keys: **MusicFiles**, **PictureFiles**, and **VideoFiles**.</span></span>

<span data-ttu-id="b8565-296">Si uno de estos contenidos se establece en true a través de uno de los valores 1, y, sí, t o true, la interfaz de usuario de reproducción automática muestra los controladores asociados a ese tipo de contenido, independientemente de si el contenido de ese tipo existe en el medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-296">If one of these contents is set to true through one the case-insensitive values 1, y, yes, t, or true, the Autoplay UI displays the handlers associated with that content type regardless of whether content of that type exists on the media.</span></span>

<span data-ttu-id="b8565-297">Si uno de estos contenidos se establece en false a través de uno de los valores 0, n, no, f o false, no distingue mayúsculas de minúsculas, la interfaz de usuario de reproducción automática no muestra los controladores asociados a ese tipo de contenido, aunque se detecte el contenido de ese tipo en el medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-297">If one of these contents is set to false through one the case-insensitive values 0, n, no, f, or false, the Autoplay UI does not display the handlers associated with that content type even if content of that type is detected on the media.</span></span>

<span data-ttu-id="b8565-298">El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-298">Use of this section is intended to allow content authors to communicate the intent of content to Autoplay.</span></span> <span data-ttu-id="b8565-299">Por ejemplo, un CD se puede clasificar como que solo contenga contenido de música, aunque también tenga imágenes y vídeos y, de lo contrario, se vería como contenido mixto.</span><span class="sxs-lookup"><span data-stu-id="b8565-299">For instance, a CD can be categorized as containing only music content even though it also has pictures and videos and would otherwise be seen as having mixed content.</span></span>

<span data-ttu-id="b8565-300">La sección de **\[ contenido \]** solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8565-300">The **\[Content\]** section is only supported under Windows Vista and later.</span></span>


```
[Content]
MusicFiles=Y
PictureFiles=0
VideoFiles=false
```



## <a name="exclusivecontentpaths-keys"></a><span data-ttu-id="b8565-301">\[Claves de ExclusiveContentPaths \]</span><span class="sxs-lookup"><span data-stu-id="b8565-301">\[ExclusiveContentPaths\] Keys</span></span>

<span data-ttu-id="b8565-302">Las carpetas que aparecen en esta sección limitan la reproducción automática para buscar solo las carpetas y las subcarpetas del contenido.</span><span class="sxs-lookup"><span data-stu-id="b8565-302">Folders listed in this section limit Autoplay to searching only those folders and their subfolders for content.</span></span> <span data-ttu-id="b8565-303">Se pueden proporcionar con o sin una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="b8565-303">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="b8565-304">En cualquier caso, se toman como rutas de acceso absolutas del directorio raíz del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-304">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="b8565-305">En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b8565-305">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="b8565-306">El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática y acortar el tiempo de examen limitando el análisis a ciertas áreas significativas del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-306">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="b8565-307">Todas las rutas de acceso válidas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8565-307">The following are all valid paths</span></span>


```
[ExclusiveContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="b8565-308">La sección **\[ ExclusiveContentPaths \]** solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8565-308">The **\[ExclusiveContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="ignorecontentpaths-keys"></a><span data-ttu-id="b8565-309">\[Claves de IgnoreContentPaths \]</span><span class="sxs-lookup"><span data-stu-id="b8565-309">\[IgnoreContentPaths\] Keys</span></span>

<span data-ttu-id="b8565-310">La reproducción automática omite las carpetas que aparecen en esta sección y sus subcarpetas al buscar contenido en un medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-310">Folders listed in this section, and their subfolders, are ignored by Autoplay when searching a media for content.</span></span> <span data-ttu-id="b8565-311">Se pueden proporcionar con o sin una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="b8565-311">They can be given with or without a leading backslash (\\).</span></span> <span data-ttu-id="b8565-312">En cualquier caso, se toman como rutas de acceso absolutas del directorio raíz del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-312">In either case they are taken as absolute paths from the root directory of the media.</span></span> <span data-ttu-id="b8565-313">En el caso de las carpetas con espacios en sus nombres, no las incluya entre comillas, ya que las comillas se toman literalmente como parte de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="b8565-313">In the case of folders with spaces in their names, do not enclose them in quotes as the quotes are taken literally as part of the path.</span></span>

<span data-ttu-id="b8565-314">Las rutas de acceso de esta sección tienen prioridad sobre las rutas de acceso de la sección **\[ ExclusiveContentPaths \]** .</span><span class="sxs-lookup"><span data-stu-id="b8565-314">Paths in this section take precedence over paths in the **\[ExclusiveContentPaths\]** section.</span></span> <span data-ttu-id="b8565-315">Si una ruta de acceso proporcionada en **\[ IgnoreContentPaths \]** es una subcarpeta de una ruta de acceso proporcionada en **\[ ExclusiveContentPaths \]**, se omitirá.</span><span class="sxs-lookup"><span data-stu-id="b8565-315">If a path given in **\[IgnoreContentPaths\]** is a subfolder of a path given in **\[ExclusiveContentPaths\]**, it is still ignored.</span></span>

<span data-ttu-id="b8565-316">El uso de esta sección está diseñado para permitir que los autores de contenido comuniquen la intención del contenido con la reproducción automática y acortar el tiempo de examen limitando el análisis a ciertas áreas significativas del medio.</span><span class="sxs-lookup"><span data-stu-id="b8565-316">Use of this section is intended to allow content authors both to communicate the intent of content to Autoplay and to shorten its scan time by limiting the scan to certain significant areas of the media.</span></span>

<span data-ttu-id="b8565-317">Todas las rutas de acceso válidas son las siguientes:</span><span class="sxs-lookup"><span data-stu-id="b8565-317">The following are all valid paths</span></span>


```
[IgnoreContentPaths]
\music
\music\more music
music2
```



<span data-ttu-id="b8565-318">La sección **\[ IgnoreContentPaths \]** solo se admite en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8565-318">The **\[IgnoreContentPaths\]** section is only supported under Windows Vista and later.</span></span>

## <a name="deviceinstall-keys"></a><span data-ttu-id="b8565-319">\[Claves de DeviceInstall \]</span><span class="sxs-lookup"><span data-stu-id="b8565-319">\[DeviceInstall\] Keys</span></span>

### <a name="driverpath"></a><span data-ttu-id="b8565-320">DriverPath</span><span class="sxs-lookup"><span data-stu-id="b8565-320">DriverPath</span></span>

<span data-ttu-id="b8565-321">La entrada **DriverPath** especifica un directorio para buscar archivos de controlador de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="b8565-321">The **DriverPath** entry specifies a directory to search recursively for driver files.</span></span> <span data-ttu-id="b8565-322">Este comando se usa durante la instalación de un controlador y no es parte de una operación de ejecución automática.</span><span class="sxs-lookup"><span data-stu-id="b8565-322">This command is used during a driver installation and is not part of an AutoRun operation.</span></span> <span data-ttu-id="b8565-323">La sección **\[ DeviceInstall \]** solo se admite en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b8565-323">The **\[DeviceInstall\]** section is only supported under Windows XP.</span></span>


```
[DeviceInstall]
DriverPath=directorypath
```



### <a name="parameters"></a><span data-ttu-id="b8565-324">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8565-324">Parameters</span></span>

-   <span data-ttu-id="b8565-325">*directoryPath*</span><span class="sxs-lookup"><span data-stu-id="b8565-325">*directorypath*</span></span>

    <span data-ttu-id="b8565-326">Una ruta de acceso a un directorio en el que Windows busca archivos de controlador, junto con todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="b8565-326">A path to a directory that Windows searches for driver files, along with all of its subdirectories.</span></span>

### <a name="remarks"></a><span data-ttu-id="b8565-327">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8565-327">Remarks</span></span>

<span data-ttu-id="b8565-328">No use Letras de unidad en *directoryPath* cuando cambien de un equipo a otro.</span><span class="sxs-lookup"><span data-stu-id="b8565-328">Do not use drive letters in *directorypath* as they change from one computer to the next.</span></span>

<span data-ttu-id="b8565-329">Para buscar en varios directorios, agregue una entrada **DriverPath** para cada directorio como en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b8565-329">To search multiple directories, add a **DriverPath** entry for each directory as in this example.</span></span>


```
[DeviceInstall]
DriverPath=drivers\video 
DriverPath=drivers\audio
```



<span data-ttu-id="b8565-330">Si no se proporciona ninguna entrada **DriverPath** en la sección **\[ \] DeviceInstall** o la entrada **DriverPath** no tiene ningún valor, esa unidad se omite durante una búsqueda de archivos de controlador.</span><span class="sxs-lookup"><span data-stu-id="b8565-330">If no **DriverPath** entry is provided in the **\[DeviceInstall\]** section or the **DriverPath** entry has no value, then that drive is skipped during a search for driver files.</span></span>

 

 
