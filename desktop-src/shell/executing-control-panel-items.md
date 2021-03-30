---
description: Describe los métodos para abrir un elemento del panel de control para Windows Vista y sistemas posteriores, así como para abarcar los comandos heredados del panel de control.
ms.assetid: c17167ab-e9a0-4290-955c-484d038b82af
title: Ejecutar elementos del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaaac4b782273e0b4444fb2b5b6d3cab0b3599ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997833"
---
# <a name="executing-control-panel-items"></a><span data-ttu-id="47f49-103">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-103">Executing Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="47f49-104">Si busca la lista de nombres canónicos y de módulos para los elementos del panel de control, consulte [nombres canónicos de elementos del panel de control](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="47f49-104">If you are looking for the list of canonical and module names for Control Panel items, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

 

<span data-ttu-id="47f49-105">Hay dos maneras de abrir un elemento del panel de control:</span><span class="sxs-lookup"><span data-stu-id="47f49-105">There are two ways to open a Control Panel item:</span></span>

-   <span data-ttu-id="47f49-106">El usuario puede abrir el panel de control y, a continuación, abrir un elemento haciendo clic o haciendo doble clic en el icono del elemento.</span><span class="sxs-lookup"><span data-stu-id="47f49-106">The user can open Control Panel and then open an item by clicking or double-clicking the item's icon.</span></span>
-   <span data-ttu-id="47f49-107">El usuario o una aplicación puede iniciar un elemento del panel de control si lo ejecuta directamente desde el símbolo de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="47f49-107">The user or an application can start a Control Panel item by executing it directly from the command line prompt.</span></span>

<span data-ttu-id="47f49-108">Una aplicación puede abrir el panel de control mediante programación con la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="47f49-108">An application can open the Control Panel programmatically by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe", SW_NORMAL);
```



<span data-ttu-id="47f49-109">En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento del panel de control denominado **MyCpl.cpl** mediante la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) .</span><span class="sxs-lookup"><span data-stu-id="47f49-109">The following example shows how an application can start the Control Panel item named **MyCpl.cpl** by using the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function.</span></span>


```
WinExec("c:\windows\system32\control.exe MyCpl.cpl", SW_NORMAL);
```



<span data-ttu-id="47f49-110">Cuando un elemento del panel de control se abre a través de una línea de comandos, puede indicarle que se abra en una pestaña determinada del elemento.</span><span class="sxs-lookup"><span data-stu-id="47f49-110">When a Control Panel item is opened through a command line, you can instruct it to open to a particular tab in the item.</span></span> <span data-ttu-id="47f49-111">Debido a la adición y eliminación de ciertas pestañas en algunos elementos del panel de control de Windows Vista, es posible que la numeración de las pestañas haya cambiado en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47f49-111">Due to the addition and removal of certain tabs in some Windows Vista Control Panel items, the numbering of the tabs might have changed from that in Windows XP.</span></span> <span data-ttu-id="47f49-112">Por ejemplo, en el ejemplo siguiente se inicia la cuarta pestaña en el elemento del sistema en Windows XP y la tercera pestaña en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="47f49-112">For instance, the following example launches the fourth tab in the System item on Windows XP and the third tab on Windows Vista.</span></span>


```
control.exe sysdm.cpl,,3
```



<span data-ttu-id="47f49-113">Este tema trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="47f49-113">This topic discusses the following:</span></span>

-   [<span data-ttu-id="47f49-114">Nombres canónicos de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f49-114">Windows Vista Canonical Names</span></span>](#windows-vista-canonical-names)
-   [<span data-ttu-id="47f49-115">Nuevos comandos para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f49-115">New Commands for Windows Vista</span></span>](#new-commands-for-windows-vista)
-   [<span data-ttu-id="47f49-116">Comandos del panel de control heredado</span><span class="sxs-lookup"><span data-stu-id="47f49-116">Legacy Control Panel Commands</span></span>](#legacy-control-panel-commands)
-   [<span data-ttu-id="47f49-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47f49-117">Related topics</span></span>](#related-topics)

## <a name="windows-vista-canonical-names"></a><span data-ttu-id="47f49-118">Nombres canónicos de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f49-118">Windows Vista Canonical Names</span></span>

<span data-ttu-id="47f49-119">En Windows Vista y versiones posteriores, el método preferido para iniciar un elemento del panel de control desde una línea de comandos es usar el nombre canónico del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="47f49-119">In Windows Vista and later, the preferred method of launching a Control Panel item from a command line is to use the Control Panel item's canonical name.</span></span> <span data-ttu-id="47f49-120">Un nombre canónico es una cadena no localizada que el elemento del panel de control declara en el registro.</span><span class="sxs-lookup"><span data-stu-id="47f49-120">A canonical name is a non-localized string that the Control Panel item declares in the registry.</span></span> <span data-ttu-id="47f49-121">El valor de usar un nombre canónico es que abstrae el nombre del módulo del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="47f49-121">The value of using a canonical name is that it abstracts the module name of the Control Panel item.</span></span> <span data-ttu-id="47f49-122">Un elemento se puede implementar en un archivo. dll y, posteriormente, volver a implementarse como un archivo. exe o cambiar su nombre de módulo.</span><span class="sxs-lookup"><span data-stu-id="47f49-122">An item can be implemented in a .dll and later be reimplemented as a .exe or change its module name.</span></span> <span data-ttu-id="47f49-123">Siempre que el nombre canónico siga siendo el mismo, no es necesario actualizar ningún programa que lo abra con ese nombre canónico.</span><span class="sxs-lookup"><span data-stu-id="47f49-123">As long as the canonical name remains the same, then any program that opens it by using that canonical name does not need to be updated.</span></span>

<span data-ttu-id="47f49-124">Por Convención, el nombre canónico tiene el formato "CorporationName. ControlPanelItemName".</span><span class="sxs-lookup"><span data-stu-id="47f49-124">By convention, the canonical name is formed as "CorporationName.ControlPanelItemName".</span></span>

<span data-ttu-id="47f49-125">En el ejemplo siguiente se muestra cómo una aplicación puede iniciar el elemento del panel de control **Windows Update** con [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span><span class="sxs-lookup"><span data-stu-id="47f49-125">The following example shows how an application can start the Control Panel item **Windows Update** with [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec).</span></span>


```
WinExec("%systemroot%\system32\control.exe /name Microsoft.WindowsUpdate", SW_NORMAL);
```



<span data-ttu-id="47f49-126">Para iniciar un elemento del panel de control con su nombre canónico, use: "% SystemRoot% \\ system32 \\control.exe/name *canonicalName*"</span><span class="sxs-lookup"><span data-stu-id="47f49-126">To start a Control Panel item with its canonical name, use: "%systemroot%\\system32\\control.exe /name *canonicalName*"</span></span>

<span data-ttu-id="47f49-127">Para abrir una subpágina específica de un elemento, o para abrirla con parámetros adicionales, use: "% SystemRoot% \\ system32 \\control.exe/name **canonicalName** /Page **pagename**"</span><span class="sxs-lookup"><span data-stu-id="47f49-127">To open a specific sub-page in an item, or to open it with additional parameters, use: "%systemroot%\\system32\\control.exe /name **canonicalName** /page **pageName**"</span></span>

<span data-ttu-id="47f49-128">Una aplicación también puede implementar el método [**IOpenControlPanel:: Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) para iniciar elementos del panel de control, incluida la capacidad de abrir una subpágina concreta.</span><span class="sxs-lookup"><span data-stu-id="47f49-128">An application can also implement the [**IOpenControlPanel::Open**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iopencontrolpanel-open) method to launch Control Panel items, including the ability to open a specific sub-page.</span></span>

<span data-ttu-id="47f49-129">Para obtener una lista completa de los nombres canónicos de los elementos del panel de control, consulte [nombres canónicos de elementos del panel de control](controlpanel-canonical-names.md).</span><span class="sxs-lookup"><span data-stu-id="47f49-129">For a complete list of Control Panel item canonical names, see [Canonical Names of Control Panel Items](controlpanel-canonical-names.md).</span></span>

## <a name="new-commands-for-windows-vista"></a><span data-ttu-id="47f49-130">Nuevos comandos para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f49-130">New Commands for Windows Vista</span></span>

<span data-ttu-id="47f49-131">En Windows Vista, algunas de las opciones a las que tenía acceso un módulo. cpl en Windows XP se implementan ahora como archivos. exe.</span><span class="sxs-lookup"><span data-stu-id="47f49-131">On Windows Vista, some options that were accessed by a .cpl module on Windows XP are now implemented as .exe files.</span></span> <span data-ttu-id="47f49-132">Esto proporciona seguridad adicional al permitir que se pida a los usuarios estándar que proporcionen credenciales de administrador al intentar iniciar los archivos.</span><span class="sxs-lookup"><span data-stu-id="47f49-132">This provides added security by allowing standard users to be prompted to provide administrator credentials when trying to launch the files.</span></span> <span data-ttu-id="47f49-133">Las opciones que no requieren seguridad adicional tienen acceso a las mismas líneas de comandos que se usaron en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47f49-133">Options that do not require extra security are accessed by the same command lines that were used in Windows XP.</span></span> <span data-ttu-id="47f49-134">A continuación se muestra una lista de comandos usados en Windows Vista para tener acceso a pestañas específicas de elementos del panel de control:</span><span class="sxs-lookup"><span data-stu-id="47f49-134">The following is a list of commands used in Windows Vista to access specific tabs of Control Panel items:</span></span>

### <a name="personalization"></a><span data-ttu-id="47f49-135">Personalización</span><span class="sxs-lookup"><span data-stu-id="47f49-135">Personalization</span></span>

-   <span data-ttu-id="47f49-136">Tamaño de fuente y PPP:% WINDIR% \\ system32 \\DpiScaling.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-136">Font size and DPI: %windir%\\system32\\DpiScaling.exe</span></span>
-   <span data-ttu-id="47f49-137">Resolución de pantalla:% WINDIR% \\ system32 \\control.exe desk.cpl, configuración@Settings</span><span class="sxs-lookup"><span data-stu-id="47f49-137">Screen resolution: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="47f49-138">Configuración de pantalla:% WINDIR% \\ system32 \\control.exe desk.cpl, configuración@Settings</span><span class="sxs-lookup"><span data-stu-id="47f49-138">Display settings: %windir%\\system32\\control.exe desk.cpl,Settings,@Settings</span></span>
-   <span data-ttu-id="47f49-139">Temas:% WINDIR% \\ system32 \\control.exe desk.cpl, temas@Themes</span><span class="sxs-lookup"><span data-stu-id="47f49-139">Themes: %windir%\\system32\\control.exe desk.cpl,Themes,@Themes</span></span>
-   <span data-ttu-id="47f49-140">Protector de la:% WINDIR% \\ system32 \\control.exe desk.cpl, protector de la@screensaver</span><span class="sxs-lookup"><span data-stu-id="47f49-140">Screensaver: %windir%\\system32\\control.exe desk.cpl,screensaver,@screensaver</span></span>
-   <span data-ttu-id="47f49-141">Varios monitores:% WINDIR% \\ system32 \\control.exe desk.cpl, monitor,@Monitor</span><span class="sxs-lookup"><span data-stu-id="47f49-141">Multi-monitor: %windir%\\system32\\control.exe desk.cpl,Monitor,@Monitor</span></span>
-   <span data-ttu-id="47f49-142">Combinación de colores:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personalization/Page pageColorization</span><span class="sxs-lookup"><span data-stu-id="47f49-142">Color Scheme: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageColorization</span></span>
-   <span data-ttu-id="47f49-143">Fondo de escritorio:% WINDIR% \\ system32 \\control.exe/Name Microsoft. Personalization/Page pageWallpaper</span><span class="sxs-lookup"><span data-stu-id="47f49-143">Desktop background: %windir%\\system32\\control.exe /name Microsoft.Personalization /page pageWallpaper</span></span>

> [!Note]  
> <span data-ttu-id="47f49-144">Las ediciones Starter y Basic no admiten el comando control.exe/Name Microsoft. Personalization.</span><span class="sxs-lookup"><span data-stu-id="47f49-144">Starter and Basic Editions do not support control.exe /name Microsoft.Personalization command.</span></span>

 

### <a name="system"></a><span data-ttu-id="47f49-145">Sistema</span><span class="sxs-lookup"><span data-stu-id="47f49-145">System</span></span>

-   <span data-ttu-id="47f49-146">Rendimiento:% WINDIR% \\ system32 \\SystemPropertiesPerformance.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-146">Performance: %windir%\\system32\\SystemPropertiesPerformance.exe</span></span>
-   <span data-ttu-id="47f49-147">Acceso remoto:% WINDIR% \\ system32 \\SystemPropertiesRemote.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-147">Remote access: %windir%\\system32\\SystemPropertiesRemote.exe</span></span>
-   <span data-ttu-id="47f49-148">Nombre de equipo:% WINDIR% \\ system32 \\SystemPropertiesComputerName.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-148">Computer name: %windir%\\system32\\SystemPropertiesComputerName.exe</span></span>
-   <span data-ttu-id="47f49-149">Protección del sistema:% WINDIR% \\ system32 \\SystemPropertiesProtection.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-149">System protection: %windir%\\system32\\SystemPropertiesProtection.exe</span></span>
-   <span data-ttu-id="47f49-150">Propiedades avanzadas del sistema:% WINDIR% \\ system32 \\SystemPropertiesAdvanced.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-150">Advanced system properties: %windir%\\system32\\SystemPropertiesAdvanced.exe</span></span>

### <a name="programs-and-features"></a><span data-ttu-id="47f49-151">Programas y características</span><span class="sxs-lookup"><span data-stu-id="47f49-151">Programs and Features</span></span>

-   <span data-ttu-id="47f49-152">Agregar o quitar programas:% WINDIR% \\ system32 \\control.exe/Name Microsoft. ProgramsAndFeatures</span><span class="sxs-lookup"><span data-stu-id="47f49-152">Add or remove programs: %windir%\\system32\\control.exe /name Microsoft.ProgramsAndFeatures</span></span>
-   <span data-ttu-id="47f49-153">Características de Windows:% WINDIR% \\ system32 \\OptionalFeatures.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-153">Windows features: %windir%\\system32\\OptionalFeatures.exe</span></span>

### <a name="regional-and-language-options"></a><span data-ttu-id="47f49-154">Configuración regional y de idioma</span><span class="sxs-lookup"><span data-stu-id="47f49-154">Regional and Language Options</span></span>

-   <span data-ttu-id="47f49-155">Teclado:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Keyboard"</span><span class="sxs-lookup"><span data-stu-id="47f49-155">Keyboard: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"keyboard"</span></span>
-   <span data-ttu-id="47f49-156">Ubicación:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Location"</span><span class="sxs-lookup"><span data-stu-id="47f49-156">Location: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"location"</span></span>
-   <span data-ttu-id="47f49-157">Administrativo:% SystemRoot% \\ system32 \\control.exe/Name Microsoft. RegionalAndLanguageOptions/Page/p: "Administrative"</span><span class="sxs-lookup"><span data-stu-id="47f49-157">Administrative: %systemroot%\\system32\\control.exe /name Microsoft.RegionalAndLanguageOptions /page /p:"administrative"</span></span>

### <a name="folder-options"></a><span data-ttu-id="47f49-158">Opciones de carpeta</span><span class="sxs-lookup"><span data-stu-id="47f49-158">Folder Options</span></span>

-   <span data-ttu-id="47f49-159">Búsqueda de carpetas:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 2</span><span class="sxs-lookup"><span data-stu-id="47f49-159">Folder searching: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 2</span></span>
-   <span data-ttu-id="47f49-160">Asociaciones de archivo:% WINDIR% \\ system32 \\control.exe/Name Microsoft. DefaultPrograms/Page pageFileAssoc</span><span class="sxs-lookup"><span data-stu-id="47f49-160">File associations: %windir%\\system32\\control.exe /name Microsoft.DefaultPrograms /page pageFileAssoc</span></span>
-   <span data-ttu-id="47f49-161">Vista:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 7</span><span class="sxs-lookup"><span data-stu-id="47f49-161">View: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 7</span></span>
-   <span data-ttu-id="47f49-162">General:% WINDIR% \\ system32 \\rundll32.exe shell32.dll, opciones \_ RunDLL 0</span><span class="sxs-lookup"><span data-stu-id="47f49-162">General: %windir%\\system32\\rundll32.exe shell32.dll,Options\_RunDLL 0</span></span>

### <a name="power-options"></a><span data-ttu-id="47f49-163">Opciones de energía</span><span class="sxs-lookup"><span data-stu-id="47f49-163">Power Options</span></span>

-   <span data-ttu-id="47f49-164">Editar la configuración del plan actual:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pagePlanSettings</span><span class="sxs-lookup"><span data-stu-id="47f49-164">Edit current plan settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pagePlanSettings</span></span>
-   <span data-ttu-id="47f49-165">Configuración del sistema:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pageGlobalSettings</span><span class="sxs-lookup"><span data-stu-id="47f49-165">System settings: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageGlobalSettings</span></span>
-   <span data-ttu-id="47f49-166">Crear un plan de energía:% WINDIR% \\ system32 \\control.exe/Name Microsoft. PowerOptions/Page pageCreateNewPlan</span><span class="sxs-lookup"><span data-stu-id="47f49-166">Create a power plan: %windir%\\system32\\control.exe /name Microsoft.PowerOptions /page pageCreateNewPlan</span></span>
-   <span data-ttu-id="47f49-167">No hay ningún comando canónico para la página Configuración avanzada, se tiene acceso a ella de la manera más antigua:% WINDIR% \\ system32 \\control.exe powercfg.cpl,, 3</span><span class="sxs-lookup"><span data-stu-id="47f49-167">There is no canonical command for the Advanced Settings page, it is accessed in the older manner: %windir%\\system32\\control.exe powercfg.cpl,,3</span></span>

## <a name="legacy-control-panel-commands"></a><span data-ttu-id="47f49-168">Comandos del panel de control heredado</span><span class="sxs-lookup"><span data-stu-id="47f49-168">Legacy Control Panel Commands</span></span>

<span data-ttu-id="47f49-169">Cuando se usa la función [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) , el sistema puede reconocer comandos especiales del panel de control.</span><span class="sxs-lookup"><span data-stu-id="47f49-169">When you use the [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec) function, the system can recognize special Control Panel commands.</span></span> <span data-ttu-id="47f49-170">Estos comandos preparan Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="47f49-170">These commands predate Windows Vista.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="47f49-171">Escritorio control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-171">control.exe desktop</span></span></td>
<td><span data-ttu-id="47f49-172">Inicia la ventana <strong>propiedades de pantalla</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-172">Launches the <strong>Display Properties</strong> window.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="47f49-173">Las ediciones Starter y Basic no admiten este comando.</span><span class="sxs-lookup"><span data-stu-id="47f49-173">Starter and Basic Editions do not support this command.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f49-174">Color de control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-174">control.exe color</span></span></td>
<td><span data-ttu-id="47f49-175">Inicia la ventana <strong>propiedades de pantalla</strong> con la pestaña <strong>apariencia</strong> preseleccionada.</span><span class="sxs-lookup"><span data-stu-id="47f49-175">Launches the <strong>Display Properties</strong> window with the <strong>Appearance</strong> tab preselected.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47f49-176">control.exe fecha y hora</span><span class="sxs-lookup"><span data-stu-id="47f49-176">control.exe date/time</span></span></td>
<td><span data-ttu-id="47f49-177">Inicia la ventana <strong>propiedades de fecha y hora</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-177">Launches the <strong>Date and Time Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f49-178">control.exe internacional</span><span class="sxs-lookup"><span data-stu-id="47f49-178">control.exe international</span></span></td>
<td><span data-ttu-id="47f49-179">Inicia la ventana <strong>Opciones regionales y de idioma</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-179">Launches the <strong>Regional and Language Options</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47f49-180">Mouse control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-180">control.exe mouse</span></span></td>
<td><span data-ttu-id="47f49-181">Inicia la ventana <strong>propiedades del mouse</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-181">Launches the <strong>Mouse Properties</strong> window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f49-182">Teclado control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-182">control.exe keyboard</span></span></td>
<td><span data-ttu-id="47f49-183">Inicia la ventana <strong>propiedades del teclado</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-183">Launches the <strong>Keyboard Properties</strong> window.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47f49-184">control.exe impresoras</span><span class="sxs-lookup"><span data-stu-id="47f49-184">control.exe printers</span></span></td>
<td><span data-ttu-id="47f49-185">Muestra la carpeta <strong>impresoras y faxes</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-185">Displays the <strong>Printers and Faxes</strong> folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47f49-186">Fuentes de control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-186">control.exe fonts</span></span></td>
<td><span data-ttu-id="47f49-187">Muestra la carpeta <strong>fuentes</strong> .</span><span class="sxs-lookup"><span data-stu-id="47f49-187">Displays the <strong>Fonts</strong> folder.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="47f49-188">Para sistemas Windows 2000 y versiones posteriores:</span><span class="sxs-lookup"><span data-stu-id="47f49-188">For Windows 2000 and later systems:</span></span>



|                            |                                                          |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="47f49-189">Carpetas de control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-189">control.exe folders</span></span>        | <span data-ttu-id="47f49-190">Inicia la ventana **Opciones de carpeta** .</span><span class="sxs-lookup"><span data-stu-id="47f49-190">Launches the **Folder Options** window.</span></span>                  |
| <span data-ttu-id="47f49-191">control.exe NetWare</span><span class="sxs-lookup"><span data-stu-id="47f49-191">control.exe netware</span></span>        | <span data-ttu-id="47f49-192">Inicia la ventana de **Novell NetWare** (si está instalado).</span><span class="sxs-lookup"><span data-stu-id="47f49-192">Launches the **Novell NetWare** window (if installed).</span></span>   |
| <span data-ttu-id="47f49-193">Telefonía control.exe</span><span class="sxs-lookup"><span data-stu-id="47f49-193">control.exe telephony</span></span>      | <span data-ttu-id="47f49-194">Inicia la ventana **Opciones de teléfono y módem** .</span><span class="sxs-lookup"><span data-stu-id="47f49-194">Launches the **Phone and Modem Options** window.</span></span>         |
| <span data-ttu-id="47f49-195">control.exe AdminTools</span><span class="sxs-lookup"><span data-stu-id="47f49-195">control.exe admintools</span></span>     | <span data-ttu-id="47f49-196">Muestra la carpeta **herramientas administrativas** .</span><span class="sxs-lookup"><span data-stu-id="47f49-196">Displays the **Administrative Tools** folder.</span></span>            |
| <span data-ttu-id="47f49-197">control.exe schedtasks</span><span class="sxs-lookup"><span data-stu-id="47f49-197">control.exe schedtasks</span></span>     | <span data-ttu-id="47f49-198">Muestra la carpeta **tareas programadas** .</span><span class="sxs-lookup"><span data-stu-id="47f49-198">Displays the **Scheduled Tasks** folder.</span></span>                 |
| <span data-ttu-id="47f49-199">control.exe netconnections</span><span class="sxs-lookup"><span data-stu-id="47f49-199">control.exe netconnections</span></span> | <span data-ttu-id="47f49-200">Muestra la carpeta **conexiones de red** .</span><span class="sxs-lookup"><span data-stu-id="47f49-200">Displays the **Network Connections** folder.</span></span>             |
| <span data-ttu-id="47f49-201">control.exe infrarrojos</span><span class="sxs-lookup"><span data-stu-id="47f49-201">control.exe infrared</span></span>       | <span data-ttu-id="47f49-202">Inicia la ventana **monitor de infrarrojos** (si está instalado).</span><span class="sxs-lookup"><span data-stu-id="47f49-202">Launches the **Infrared Monitor** window (if installed).</span></span> |
| <span data-ttu-id="47f49-203">control.exe userpasswords</span><span class="sxs-lookup"><span data-stu-id="47f49-203">control.exe userpasswords</span></span>  | <span data-ttu-id="47f49-204">Inicia la ventana **cuentas de usuario** .</span><span class="sxs-lookup"><span data-stu-id="47f49-204">Launches the **User Accounts** window.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="47f49-205">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="47f49-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47f49-206">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-206">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="47f49-207">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="47f49-207">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="47f49-208">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-208">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="47f49-209">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="47f49-209">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="47f49-210">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-210">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="47f49-211">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="47f49-211">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="47f49-212">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-212">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="47f49-213">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="47f49-213">Creating Searchable Task Links for a Control Panel Item</span></span>](creating-searchable-task-links.md)
</dt> <dt>

[<span data-ttu-id="47f49-214">Acceder al panel de control en modo seguro en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="47f49-214">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
