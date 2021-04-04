---
title: Marcas de registro
description: Marcas de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Complementos de Media Player de Windows, marcas de registro
- complementos, marcas de registro
- Complementos de la interfaz de usuario, marcas de registro
- Complementos de la interfaz de usuario, marcas de registro
- marcas, Complementos de la interfaz de usuario
- registro, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077327"
---
# <a name="registration-flags"></a><span data-ttu-id="04cab-109">Marcas de registro</span><span class="sxs-lookup"><span data-stu-id="04cab-109">Registration Flags</span></span>

<span data-ttu-id="04cab-110">Cuando el Asistente para complementos de Windows Media Player crea un nuevo proyecto de complemento de interfaz de usuario, crea una clave en el registro que contiene información sobre el complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="04cab-111">Esta clave se crea en la siguiente ubicación:</span><span class="sxs-lookup"><span data-stu-id="04cab-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="04cab-112">*ClassID* es el ID. de clase del complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="04cab-113">Esta clave incluye los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="04cab-113">This key includes the following values.</span></span>



| <span data-ttu-id="04cab-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="04cab-114">Name</span></span>                     | <span data-ttu-id="04cab-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="04cab-115">Type</span></span>       | <span data-ttu-id="04cab-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="04cab-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04cab-117">Funcionalidades</span><span class="sxs-lookup"><span data-stu-id="04cab-117">Capabilities</span></span>             | <span data-ttu-id="04cab-118">\_valor DWORD reg</span><span class="sxs-lookup"><span data-stu-id="04cab-118">REG\_DWORD</span></span> | <span data-ttu-id="04cab-119">Un valor DWORD que consta de al menos una marca de tipo de complemento que se puede combinar con una o más marcas de funciones de complemento mediante operaciones binarias o.</span><span class="sxs-lookup"><span data-stu-id="04cab-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="04cab-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="04cab-120">Description</span></span>              | <span data-ttu-id="04cab-121">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="04cab-121">REG\_SZ</span></span>    | <span data-ttu-id="04cab-122">Cadena que contiene la descripción del complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="04cab-123">El Asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor.</span><span class="sxs-lookup"><span data-stu-id="04cab-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="04cab-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="04cab-124">FriendlyName</span></span>             | <span data-ttu-id="04cab-125">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="04cab-125">REG\_SZ</span></span>    | <span data-ttu-id="04cab-126">Cadena que contiene el nombre legible por el usuario para el complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="04cab-127">El Asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor.</span><span class="sxs-lookup"><span data-stu-id="04cab-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="04cab-128">UninstallPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="04cab-128">UninstallPath (optional)</span></span> | <span data-ttu-id="04cab-129">Registro \_ SZ</span><span class="sxs-lookup"><span data-stu-id="04cab-129">REG\_SZ</span></span>    | <span data-ttu-id="04cab-130">Cadena que contiene la ruta de acceso a un archivo ejecutable que desinstala el complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="04cab-131">Para obtener más información sobre el protocolo res, vea el SDK de desarrollo de Internet.</span><span class="sxs-lookup"><span data-stu-id="04cab-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="04cab-132">En la tabla siguiente se detallan las marcas de tipo de complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="04cab-133">Marca de tipo de complemento</span><span class="sxs-lookup"><span data-stu-id="04cab-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="04cab-134">Value</span><span class="sxs-lookup"><span data-stu-id="04cab-134">Value</span></span> | <span data-ttu-id="04cab-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="04cab-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="04cab-136">**\_fondo de tipo de complemento \_**</span><span class="sxs-lookup"><span data-stu-id="04cab-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="04cab-137">0x1</span><span class="sxs-lookup"><span data-stu-id="04cab-137">0x1</span></span>   | <span data-ttu-id="04cab-138">El complemento de la interfaz de usuario no muestra una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="04cab-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="04cab-139">**tipo de complemento \_ \_ SEPARATEWINDOW**</span><span class="sxs-lookup"><span data-stu-id="04cab-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="04cab-140">0x2</span><span class="sxs-lookup"><span data-stu-id="04cab-140">0x2</span></span>   | <span data-ttu-id="04cab-141">El complemento de la interfaz de usuario es un complemento de ventana independiente.</span><span class="sxs-lookup"><span data-stu-id="04cab-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="04cab-142">**tipo de complemento \_ \_ DISPLAYAREA**</span><span class="sxs-lookup"><span data-stu-id="04cab-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="04cab-143">0x3</span><span class="sxs-lookup"><span data-stu-id="04cab-143">0x3</span></span>   | <span data-ttu-id="04cab-144">El complemento de la interfaz de usuario es un complemento de área de presentación.</span><span class="sxs-lookup"><span data-stu-id="04cab-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="04cab-145">**tipo de complemento \_ \_ SETTINGSAREA**</span><span class="sxs-lookup"><span data-stu-id="04cab-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="04cab-146">0x4</span><span class="sxs-lookup"><span data-stu-id="04cab-146">0x4</span></span>   | <span data-ttu-id="04cab-147">El complemento de la interfaz de usuario es un complemento de área de configuración.</span><span class="sxs-lookup"><span data-stu-id="04cab-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="04cab-148">**tipo de complemento \_ \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="04cab-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="04cab-149">0X5</span><span class="sxs-lookup"><span data-stu-id="04cab-149">0x5</span></span>   | <span data-ttu-id="04cab-150">El complemento de la interfaz de usuario es un complemento de área de metadatos.</span><span class="sxs-lookup"><span data-stu-id="04cab-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="04cab-151">En la tabla siguiente se detallan las marcas de funcionalidades del complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="04cab-152">Marca de capacidades del complemento</span><span class="sxs-lookup"><span data-stu-id="04cab-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="04cab-153">Value</span><span class="sxs-lookup"><span data-stu-id="04cab-153">Value</span></span>      | <span data-ttu-id="04cab-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="04cab-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04cab-155">**marcas de COMPLEMENTOs \_ \_ ACCEPTSMEDIA**</span><span class="sxs-lookup"><span data-stu-id="04cab-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="04cab-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="04cab-156">0x10000000</span></span> | <span data-ttu-id="04cab-157">El complemento de interfaz de usuario puede aceptar matrices de punteros de objetos **multimedia** cuando Windows Media Player llama a [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="04cab-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="04cab-158">**marcas de COMPLEMENTOs \_ \_ ACCEPTSPLAYLISTS**</span><span class="sxs-lookup"><span data-stu-id="04cab-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="04cab-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="04cab-159">0x8000000</span></span>  | <span data-ttu-id="04cab-160">El complemento de interfaz de usuario puede aceptar matrices de punteros de objeto de **lista de reproducción** cuando Windows Media Player llama a [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="04cab-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="04cab-161">**marcas de COMPLEMENTOs \_ \_ HASPRESETS**</span><span class="sxs-lookup"><span data-stu-id="04cab-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="04cab-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="04cab-162">0x4000000</span></span>  | <span data-ttu-id="04cab-163">El complemento de la interfaz de usuario usa valores preestablecidos.</span><span class="sxs-lookup"><span data-stu-id="04cab-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="04cab-164">Si el complemento especifica esta marca, Windows Media Player consultará el complemento para obtener información preestablecida mediante una llamada a [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="04cab-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="04cab-165">**marcas de COMPLEMENTOs \_ \_ HASPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="04cab-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="04cab-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="04cab-166">0x80000000</span></span> | <span data-ttu-id="04cab-167">El complemento de la interfaz de usuario proporciona un cuadro de diálogo de página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="04cab-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="04cab-168">Windows Media Player llamará a [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) si esta marca se establece cuando se invoca la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="04cab-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="04cab-169">**marcas de complemento \_ \_ ocultas**</span><span class="sxs-lookup"><span data-stu-id="04cab-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="04cab-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="04cab-170">0x02000000</span></span> | <span data-ttu-id="04cab-171">El complemento de la interfaz de usuario de fondo no aparece en el menú **Complementos** al que se tiene acceso desde los menús **Ver** o **herramientas** o el botón **seleccionar ahora opciones de reproducción** en reproducción en curso.</span><span class="sxs-lookup"><span data-stu-id="04cab-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="04cab-172">Aparece en la pestaña complementos del **cuadro de diálogo** opciones.</span><span class="sxs-lookup"><span data-stu-id="04cab-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="04cab-173">Esto hace que el icono de ejecución del complemento de fondo aparezca en la barra de estado. Esta marca no tiene ningún efecto en los complementos que no sean los complementos de la interfaz de usuario de fondo.</span><span class="sxs-lookup"><span data-stu-id="04cab-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="04cab-174">**marcas de COMPLEMENTOs \_ \_ INSTALLAUTORUN**</span><span class="sxs-lookup"><span data-stu-id="04cab-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="04cab-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="04cab-175">0x40000000</span></span> | <span data-ttu-id="04cab-176">Windows Media Player ejecuta el complemento de la interfaz de usuario automáticamente cuando se instala el complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="04cab-177">**marcas de COMPLEMENTOs \_ \_ LAUNCHPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="04cab-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="04cab-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="04cab-178">0x20000000</span></span> | <span data-ttu-id="04cab-179">Windows Media Player llama a [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) cuando el complemento de la interfaz de usuario se ejecuta por primera vez. Si se especifica esta marca, también se deben especificar las **marcas de complemento \_ \_ HASPROPERTYPAGE** .</span><span class="sxs-lookup"><span data-stu-id="04cab-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="04cab-180">Las siguientes constantes se definen en wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="04cab-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="04cab-181">No cambie los valores asociados a estas constantes.</span><span class="sxs-lookup"><span data-stu-id="04cab-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="04cab-182">Nombre</span><span class="sxs-lookup"><span data-stu-id="04cab-182">Name</span></span>                                    | <span data-ttu-id="04cab-183">Descripción</span><span class="sxs-lookup"><span data-stu-id="04cab-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="04cab-184">**COMPLEMENTO \_ INSTALLREGKEY**</span><span class="sxs-lookup"><span data-stu-id="04cab-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="04cab-185">Ubicación de la clave del registro del complemento.</span><span class="sxs-lookup"><span data-stu-id="04cab-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="04cab-186">**COMPLEMENTO \_ INSTALLREGKEY \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="04cab-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="04cab-187">Nombre del valor de nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="04cab-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="04cab-188">**\_Descripción de INSTALLREGKEY de complemento \_**</span><span class="sxs-lookup"><span data-stu-id="04cab-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="04cab-189">Nombre del valor de descripción.</span><span class="sxs-lookup"><span data-stu-id="04cab-189">The name of the description value.</span></span>        |
| <span data-ttu-id="04cab-190">**\_funcionalidades de INSTALLREGKEY de complementos \_**</span><span class="sxs-lookup"><span data-stu-id="04cab-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="04cab-191">Nombre del valor de capacidades.</span><span class="sxs-lookup"><span data-stu-id="04cab-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="04cab-192">**desinstalación de INSTALLREGKEY de COMPLEMENTOs \_ \_**</span><span class="sxs-lookup"><span data-stu-id="04cab-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="04cab-193">Nombre del valor de la ruta de desinstalación.</span><span class="sxs-lookup"><span data-stu-id="04cab-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="04cab-194">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04cab-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04cab-195">**IWMPPluginUI::D isplayPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="04cab-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="04cab-196">**IWMPPluginUI:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="04cab-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="04cab-197">**IWMPPluginUI:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="04cab-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="04cab-198">**Referencia de programación de complementos de interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="04cab-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





