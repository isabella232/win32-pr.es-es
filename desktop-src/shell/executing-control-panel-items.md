---
description: Describe los métodos para abrir un Panel de control para Windows Vista y sistemas posteriores, así como para tratar los comandos Panel de control heredados.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ejecutar elementos Panel de control datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cb6ae2fa08231d3876e1a5a636e404f519f4a6
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581763"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="8137a-103">Ejecutar elementos Panel de control datos</span><span class="sxs-lookup"><span data-stu-id="8137a-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="8137a-104">Si busca la lista de nombres canónicos y de módulos para los Panel de control, vea Nombres canónicos [de Panel de control elementos](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="8137a-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="8137a-105">Hay dos maneras de abrir un Panel de control elemento:</span><span class="sxs-lookup"><span data-stu-id="8137a-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="8137a-106">El usuario puede abrir Panel de control y, a continuación, abrir un elemento haciendo clic o haciendo doble clic en el icono del elemento.</span><span class="sxs-lookup"><span data-stu-id="8137a-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="8137a-107">El usuario o una aplicación pueden iniciar un Panel de control elemento ejecutándose directamente desde el símbolo de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="8137a-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="8137a-108">Una aplicación puede abrir el Panel de control mediante programación mediante la [**función WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)</span><span class="sxs-lookup"><span data-stu-id="8137a-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="8137a-109">En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento Panel de control denominado **MyCpl.cpl** mediante la [**función WinExec.**](/windows/win32/api/winbase/nf-winbase-winexec)</span><span class="sxs-lookup"><span data-stu-id="8137a-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="8137a-110">Cuando un Panel de control se abre a través de una línea de comandos, puede indicarle que se abra en una pestaña determinada del elemento.</span><span class="sxs-lookup"><span data-stu-id="8137a-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="8137a-111">Debido a la adición y eliminación de ciertas pestañas en algunos elementos de Windows Vista Panel de control, la numeración de las pestañas podría haber cambiado a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8137a-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="8137a-112">Por ejemplo, en el ejemplo siguiente se inicia la cuarta pestaña del elemento Sistema en Windows XP y la tercera pestaña en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8137a-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="8137a-113">Este tema trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8137a-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="8137a-114">Windows Nombres canónicos de Vista</span><span class="sxs-lookup"><span data-stu-id="8137a-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="8137a-115">Nuevos comandos para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8137a-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="8137a-116">Comandos de Panel de control heredados</span><span class="sxs-lookup"><span data-stu-id="8137a-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="8137a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8137a-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="8137a-118">Windows Nombres canónicos de Vista</span><span class="sxs-lookup"><span data-stu-id="8137a-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="8137a-119">En Windows Vista y versiones posteriores, el método preferido para iniciar un elemento Panel de control desde una línea de comandos es usar el nombre canónico del elemento de Panel de control.</span><span class="sxs-lookup"><span data-stu-id="8137a-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="8137a-120">Un nombre canónico es una cadena no localizada que el elemento Panel de control declara en el Registro.</span><span class="sxs-lookup"><span data-stu-id="8137a-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="8137a-121">El valor de usar un nombre canónico es que abstrae el nombre del módulo del Panel de control elemento.</span><span class="sxs-lookup"><span data-stu-id="8137a-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="8137a-122">Un elemento se puede implementar en un .dll y posterior se puede volver a implementar como un .exe o cambiar su nombre de módulo.</span><span class="sxs-lookup"><span data-stu-id="8137a-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="8137a-123">Siempre que el nombre canónico siga siendo el mismo, no es necesario actualizar ningún programa que lo abra con ese nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="8137a-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="8137a-124">Por convención, el nombre canónico se forma como "CorporationName.ControlPanelItemName".</span><span class="sxs-lookup"><span data-stu-id="8137a-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="8137a-125">En el ejemplo siguiente se muestra cómo una aplicación puede iniciar Panel de control elemento **Windows Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="8137a-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="8137a-126">Para iniciar un Panel de control con su nombre canónico, use: "%systemroot% \\ system32 \\control.exe /name *canonicalName"*</span><span class="sxs-lookup"><span data-stu-id="8137a-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="8137a-127">Para abrir una subpáptica específica en un elemento o para abrirla con parámetros adicionales, use: "%systemroot% \\ system32 \\control.exe /name **canonicalName** /page **pageName"**</span><span class="sxs-lookup"><span data-stu-id="8137a-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="8137a-128">Una aplicación también puede implementar el método [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar Panel de control, incluida la capacidad de abrir una sub página específica.</span><span class="sxs-lookup"><span data-stu-id="8137a-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="8137a-129">Para obtener una lista completa de Panel de control de elementos canónicos, vea Nombres canónicos [de Panel de control elementos](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="8137a-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="8137a-130">Nuevos comandos para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8137a-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="8137a-131">En Windows Vista, algunas opciones a las que se ha accedido mediante un módulo .cpl en Windows XP ahora se implementan como .exe archivos.</span><span class="sxs-lookup"><span data-stu-id="8137a-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="8137a-132">Esto proporciona mayor seguridad al permitir que se pida a los usuarios estándar que proporcionen credenciales de administrador al intentar iniciar los archivos.</span><span class="sxs-lookup"><span data-stu-id="8137a-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="8137a-133">Se accede a las opciones que no requieren seguridad adicional mediante las mismas líneas de comandos que se usaron en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8137a-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="8137a-134">A continuación se muestra una lista de los comandos que se usan en Windows Vista para acceder a pestañas específicas de Panel de control elementos:</span><span class="sxs-lookup"><span data-stu-id="8137a-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="8137a-135">Personalization</span><span class="sxs-lookup"><span data-stu-id="8137a-135">Personalization</span></span>

-   <span data-ttu-id="8137a-136">Tamaño de fuente y PPP: %windir% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="8137a-137">Resolución de pantalla: %windir% \\ system32 \\control.exe desk.cpl,Configuración,@Settings</span><span class="sxs-lookup"><span data-stu-id="8137a-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="8137a-138">Configuración de visualización: %windir% \\ system32 \\control.exe desk.cpl,Configuración,@Settings</span><span class="sxs-lookup"><span data-stu-id="8137a-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="8137a-139">Temas: %windir% \\ system32 \\control.exe desk.cpl,Themes,@Themes</span><span class="sxs-lookup"><span data-stu-id="8137a-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="8137a-140">Protector de pantalla: %windir% \\ system32 \\control.exe desk.cpl,screensaver,@screensaver</span><span class="sxs-lookup"><span data-stu-id="8137a-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="8137a-141">Varios monitores: %windir% \\ system32 \\control.exe desk.cpl,Monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="8137a-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="8137a-142">Combinación de colores: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageColorization</span><span class="sxs-lookup"><span data-stu-id="8137a-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="8137a-143">Fondo del escritorio: %windir% \\ system32 \\control.exe /name Microsoft.Personalization /pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="8137a-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="8137a-144">Las ediciones Starter y Basic no admiten control.exe comando /name Microsoft.Personalization.</span><span class="sxs-lookup"><span data-stu-id="8137a-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="8137a-145">Sistema</span><span class="sxs-lookup"><span data-stu-id="8137a-145">System</span></span>

-   <span data-ttu-id="8137a-146">Rendimiento: %windir% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="8137a-147">Acceso remoto: %windir% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="8137a-148">Nombre del equipo: %windir% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="8137a-149">Protección del sistema: %windir% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="8137a-150">Propiedades avanzadas del sistema: %windir% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="8137a-151">Programas y características</span><span class="sxs-lookup"><span data-stu-id="8137a-151">Programs and Features</span></span>

-   <span data-ttu-id="8137a-152">Agregar o quitar programas: %windir% \\ system32 \\control.exe /name Microsoft.ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="8137a-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="8137a-153">Windows características: %windir% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="8137a-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="8137a-154">Configuración regional y de idioma</span><span class="sxs-lookup"><span data-stu-id="8137a-154">Regional and Language Options</span></span>

-   <span data-ttu-id="8137a-155">Teclado: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span><span class="sxs-lookup"><span data-stu-id="8137a-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="8137a-156">Ubicación: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span><span class="sxs-lookup"><span data-stu-id="8137a-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="8137a-157">Administrativo: %systemroot% \\ system32 \\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span><span class="sxs-lookup"><span data-stu-id="8137a-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="8137a-158">Opciones de carpeta</span><span class="sxs-lookup"><span data-stu-id="8137a-158">Folder Options</span></span>

-   <span data-ttu-id="8137a-159">Búsqueda de carpetas: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 2</span><span class="sxs-lookup"><span data-stu-id="8137a-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="8137a-160">Asociaciones de archivo: %windir% \\ system32 \\control.exe /name Microsoft.DefaultPrograms /pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="8137a-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="8137a-161">Vista: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 7</span><span class="sxs-lookup"><span data-stu-id="8137a-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="8137a-162">General: %windir% \\ system32 \\rundll32.exe shell32.dll,Options \_ RunDLL 0</span><span class="sxs-lookup"><span data-stu-id="8137a-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="8137a-163">Opciones de energía</span><span class="sxs-lookup"><span data-stu-id="8137a-163">Power Options</span></span>

-   <span data-ttu-id="8137a-164">Editar la configuración actual del plan: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="8137a-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="8137a-165">Configuración del sistema: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="8137a-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="8137a-166">Crear un plan de energía: %windir% \\ system32 \\control.exe /name Microsoft.PowerOptions /pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="8137a-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="8137a-167">No hay ningún comando canónico para la página advanced Configuración, se accede a él de la manera anterior: %windir% \\ system32 \\control.exe powercfg.cpl,3</span><span class="sxs-lookup"><span data-stu-id="8137a-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="8137a-168">Comandos de Panel de control heredados</span><span class="sxs-lookup"><span data-stu-id="8137a-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="8137a-169">Cuando se usa [**la función WinExec,**](/windows/win32/api/winbase/nf-winbase-winexec) el sistema puede reconocer comandos Panel de control especiales.</span><span class="sxs-lookup"><span data-stu-id="8137a-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="8137a-170">Estos comandos son anteriores a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8137a-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8137a-171">control.exe escritorio</span><span class="sxs-lookup"><span data-stu-id="8137a-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="8137a-172">Inicia la <strong>Propiedades de pantalla</strong> ventana.</span><span class="sxs-lookup"><span data-stu-id="8137a-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="8137a-173">Las ediciones Starter y Basic no admiten este comando.</span><span class="sxs-lookup"><span data-stu-id="8137a-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8137a-174">control.exe color</span><span class="sxs-lookup"><span data-stu-id="8137a-174">control.exe color</span></span></td>
<td><span data-ttu-id="8137a-175">Inicia la ventana <strong>Propiedades de pantalla</strong> con la <strong>pestaña</strong> Apariencia preseleccionada.</span><span class="sxs-lookup"><span data-stu-id="8137a-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8137a-176">control.exe fecha y hora</span><span class="sxs-lookup"><span data-stu-id="8137a-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="8137a-177">Inicia la ventana <strong>Propiedades de fecha y</strong> hora.</span><span class="sxs-lookup"><span data-stu-id="8137a-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8137a-178">control.exe internacional</span><span class="sxs-lookup"><span data-stu-id="8137a-178">control.exe international</span></span></td>
<td><span data-ttu-id="8137a-179">Inicia la ventana <strong>Opciones regionales y de</strong> idioma.</span><span class="sxs-lookup"><span data-stu-id="8137a-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8137a-180">control.exe mouse</span><span class="sxs-lookup"><span data-stu-id="8137a-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="8137a-181">Inicia la ventana <strong>Propiedades del</strong> mouse.</span><span class="sxs-lookup"><span data-stu-id="8137a-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8137a-182">control.exe teclado</span><span class="sxs-lookup"><span data-stu-id="8137a-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="8137a-183">Inicia la ventana <strong>Propiedades del</strong> teclado.</span><span class="sxs-lookup"><span data-stu-id="8137a-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8137a-184">control.exe impresoras</span><span class="sxs-lookup"><span data-stu-id="8137a-184">control.exe printers</span></span></td>
<td><span data-ttu-id="8137a-185">Muestra la <strong>carpeta Impresoras y faxes.</strong></span><span class="sxs-lookup"><span data-stu-id="8137a-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8137a-186">control.exe fuentes</span><span class="sxs-lookup"><span data-stu-id="8137a-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="8137a-187">Muestra la <strong>carpeta Fuentes.</strong></span><span class="sxs-lookup"><span data-stu-id="8137a-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8137a-188">Para Windows sistemas 2000 y posteriores:</span><span class="sxs-lookup"><span data-stu-id="8137a-188">For Windows 2000 and later systems:</span></span>



| <span data-ttu-id="8137a-189">Comando</span><span class="sxs-lookup"><span data-stu-id="8137a-189">Command</span></span>                    | <span data-ttu-id="8137a-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="8137a-190">Description</span></span>                                              |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="8137a-191">control.exe carpetas</span><span class="sxs-lookup"><span data-stu-id="8137a-191">control.exe folders</span></span>        | <span data-ttu-id="8137a-192">Inicia la ventana **Opciones de carpeta.**</span><span class="sxs-lookup"><span data-stu-id="8137a-192">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="8137a-193">control.exe netware</span><span class="sxs-lookup"><span data-stu-id="8137a-193">control.exe netware</span></span>        | <span data-ttu-id="8137a-194">Inicia la ventana **NetWare de Asíns** (si está instalada).</span><span class="sxs-lookup"><span data-stu-id="8137a-194">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="8137a-195">control.exe telefonía</span><span class="sxs-lookup"><span data-stu-id="8137a-195">control.exe telephony</span></span>      | <span data-ttu-id="8137a-196">Inicia la ventana **Teléfono y opciones de módem.**</span><span class="sxs-lookup"><span data-stu-id="8137a-196">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="8137a-197">control.exe admintools</span><span class="sxs-lookup"><span data-stu-id="8137a-197">control.exe admintools</span></span>     | <span data-ttu-id="8137a-198">Muestra la **carpeta Herramientas administrativas.**</span><span class="sxs-lookup"><span data-stu-id="8137a-198">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="8137a-199">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="8137a-199">control.exe schedtasks</span></span>     | <span data-ttu-id="8137a-200">Muestra la **carpeta Tareas programadas.**</span><span class="sxs-lookup"><span data-stu-id="8137a-200">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="8137a-201">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="8137a-201">control.exe netconnections</span></span> | <span data-ttu-id="8137a-202">Muestra la carpeta **Conexiones de** red.</span><span class="sxs-lookup"><span data-stu-id="8137a-202">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="8137a-203">control.exe de datos</span><span class="sxs-lookup"><span data-stu-id="8137a-203">control.exe infrared</span></span>       | <span data-ttu-id="8137a-204">Inicia la ventana **Monitor de inifijo** (si está instalado).</span><span class="sxs-lookup"><span data-stu-id="8137a-204">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="8137a-205">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="8137a-205">control.exe userpasswords</span></span>  | <span data-ttu-id="8137a-206">Inicia la ventana **Cuentas de** usuario.</span><span class="sxs-lookup"><span data-stu-id="8137a-206">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="8137a-207">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8137a-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8137a-208">Panel de control elementos</span><span class="sxs-lookup"><span data-stu-id="8137a-208">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="8137a-209">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="8137a-209">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="8137a-210">Registro de Panel de control elementos</span><span class="sxs-lookup"><span data-stu-id="8137a-210">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="8137a-211">Uso de CPLApplet</span><span class="sxs-lookup"><span data-stu-id="8137a-211">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="8137a-212">Panel de control de mensajes</span><span class="sxs-lookup"><span data-stu-id="8137a-212">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="8137a-213">Extender elementos de Panel de control sistema</span><span class="sxs-lookup"><span data-stu-id="8137a-213">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="8137a-214">Asignación de Panel de control categorías</span><span class="sxs-lookup"><span data-stu-id="8137a-214">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="8137a-215">Crear vínculos de tareas buscables para un elemento Panel de control búsqueda</span><span class="sxs-lookup"><span data-stu-id="8137a-215">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="8137a-216">Acceso al Panel de control en modo Caja fuerte en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8137a-216">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
