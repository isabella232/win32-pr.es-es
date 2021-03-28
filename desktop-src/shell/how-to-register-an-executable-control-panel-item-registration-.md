---
description: En el caso de los elementos del panel de control que se implementan como archivos. exe, no se requiere ninguna exportación especial ni control de mensajes. Cualquier archivo. exe se puede registrar como un objeto de comando para que aparezca con un punto de entrada en la carpeta del panel de control.
title: Cómo registrar elementos del panel de control ejecutable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082634"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="1add5-104">Cómo registrar elementos del panel de control ejecutable</span><span class="sxs-lookup"><span data-stu-id="1add5-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="1add5-105">En el caso de los elementos del panel de control que se implementan como archivos. exe, no se requiere ninguna exportación especial ni control de mensajes.</span><span class="sxs-lookup"><span data-stu-id="1add5-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="1add5-106">Cualquier archivo. exe se puede registrar como un objeto de comando para que aparezca con un punto de entrada en la carpeta del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="1add5-107">Aquí se usa un ejemplo para mostrar los requisitos de registro.</span><span class="sxs-lookup"><span data-stu-id="1add5-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="1add5-108">En el ejemplo se muestra cómo registrar un elemento del panel de control denominado **My Settings** como un objeto Command para que aparezca en la ventana Panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="1add5-109">La ventana **My Settings (mi configuración** ) también aparece cuando `MyApp.exe /settings` se ejecuta el comando.</span><span class="sxs-lookup"><span data-stu-id="1add5-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="1add5-110">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="1add5-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="1add5-111">Paso 1:</span><span class="sxs-lookup"><span data-stu-id="1add5-111">Step 1:</span></span>

<span data-ttu-id="1add5-112">Genere un GUID para el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="1add5-113">El GUID identifica de forma única el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="1add5-114">En este ejemplo, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` es el GUID del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="1add5-115">Paso 2:</span><span class="sxs-lookup"><span data-stu-id="1add5-115">Step 2:</span></span>

<span data-ttu-id="1add5-116">Con el GUID como nombre, agregue una subclave al registro como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="1add5-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="1add5-117">Los datos de la entrada predeterminada son simplemente el \_ nombre de reg SZ del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="1add5-118">La entrada predeterminada puede ser útil para identificar la entrada de GUID, pero es opcional.</span><span class="sxs-lookup"><span data-stu-id="1add5-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="1add5-119">Paso 3:</span><span class="sxs-lookup"><span data-stu-id="1add5-119">Step 3:</span></span>

<span data-ttu-id="1add5-120">Con el GUID como nombre, agregue una subclave y sus entradas al registro como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="1add5-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="1add5-121">**Default**.</span><span class="sxs-lookup"><span data-stu-id="1add5-121">**Default**.</span></span> <span data-ttu-id="1add5-122">REG \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-122">REG\_SZ.</span></span> <span data-ttu-id="1add5-123">Nombre para mostrar del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="1add5-124">**LocalizedString**.</span><span class="sxs-lookup"><span data-stu-id="1add5-124">**LocalizedString**.</span></span> <span data-ttu-id="1add5-125">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1add5-125">Optional.</span></span> <span data-ttu-id="1add5-126">REG \_ SZ o REG \_ Expand \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="1add5-127">El nombre del módulo y el identificador de la tabla de cadenas del nombre localizado del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="1add5-128">El formato es un signo "arroba" (@) seguido del nombre del archivo. exe o. dll que contiene la tabla de cadenas de la interfaz de usuario multilingüe (MUI).</span><span class="sxs-lookup"><span data-stu-id="1add5-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="1add5-129">Las variables de entorno se pueden usar como sustituto de una parte de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1add5-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="1add5-130">La ruta de acceso y el nombre de archivo van seguidos de una coma (,) y un guión (-), seguido del identificador de la tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="1add5-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="1add5-131">Si el módulo no tiene una tabla de cadenas, esta entrada puede ser simplemente la cadena del nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="1add5-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="1add5-132">Si solo usa la cadena de nombre para mostrar en lugar de una tabla de cadenas, el nombre no se ajusta al idioma para mostrar actual.</span><span class="sxs-lookup"><span data-stu-id="1add5-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="1add5-133">Recuadro informativo.</span><span class="sxs-lookup"><span data-stu-id="1add5-133">**InfoTip**.</span></span> <span data-ttu-id="1add5-134">REG \_ SZ o REG \_ Expand \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="1add5-135">Descripción del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-135">A description of the Control Panel item.</span></span> <span data-ttu-id="1add5-136">Esta información se muestra en un recuadro informativo que se muestra cuando se mantiene el mouse sobre el icono del elemento.</span><span class="sxs-lookup"><span data-stu-id="1add5-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="1add5-137">La sintaxis es la misma que la que se usa para LocalizedString, incluida la opción de simplemente proporcionar una cadena en lugar de una referencia de tabla de cadenas.</span><span class="sxs-lookup"><span data-stu-id="1add5-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="1add5-138">**System. ApplicationName**.</span><span class="sxs-lookup"><span data-stu-id="1add5-138">**System.ApplicationName**.</span></span> <span data-ttu-id="1add5-139">REG \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-139">REG\_SZ.</span></span> <span data-ttu-id="1add5-140">El nombre canónico del elemento.</span><span class="sxs-lookup"><span data-stu-id="1add5-140">The canonical name of the item.</span></span> <span data-ttu-id="1add5-141">El comando del formulario `control.exe /name System.ApplicationName` abre el elemento; por ejemplo, `control.exe /name MyCorporation.MySettings` .</span><span class="sxs-lookup"><span data-stu-id="1add5-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="1add5-142">Vea [Ejecutar elementos del panel de control](executing-control-panel-items.md) para obtener más información sobre el uso de Control.exe.</span><span class="sxs-lookup"><span data-stu-id="1add5-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="1add5-143">**System. ControlPanel. Category**.</span><span class="sxs-lookup"><span data-stu-id="1add5-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="1add5-144">REG \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-144">REG\_SZ.</span></span> <span data-ttu-id="1add5-145">Valor que declara las categorías del panel de control donde aparece el elemento.</span><span class="sxs-lookup"><span data-stu-id="1add5-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="1add5-146">Varias categorías se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="1add5-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="1add5-147">En el caso del ejemplo anterior, la entrada especifica que el elemento **My Settings** debe aparecer en las categorías **Appearance y personalización** y **programas** .</span><span class="sxs-lookup"><span data-stu-id="1add5-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="1add5-148">Vea [asignar categorías del panel de control](assigning-control-panel-categories.md) para posibles valores de categoría.</span><span class="sxs-lookup"><span data-stu-id="1add5-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="1add5-149">**System. software. TasksFileUrl**.</span><span class="sxs-lookup"><span data-stu-id="1add5-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="1add5-150">REG \_ SZ o REG \_ Expand \_ .</span><span class="sxs-lookup"><span data-stu-id="1add5-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="1add5-151">Ruta de acceso del archivo XML que define los [vínculos de tarea](creating-searchable-task-links.md).</span><span class="sxs-lookup"><span data-stu-id="1add5-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="1add5-152">Puede ser una ruta de acceso de archivo directa, tal como se muestra en el ejemplo, o un recurso incrustado especificado como un nombre de módulo y un identificador de recurso como "% ProgramFiles% \\ Corp \\ MyApp \\MyApp.exe,-31".</span><span class="sxs-lookup"><span data-stu-id="1add5-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="1add5-153">Paso 4:</span><span class="sxs-lookup"><span data-stu-id="1add5-153">Step 4:</span></span>

<span data-ttu-id="1add5-154">En la misma subclave GUID, agregue la siguiente subclave al registro para proporcionar la ruta de acceso del archivo que contiene el icono y el identificador de recurso de la imagen dentro de ese archivo.</span><span class="sxs-lookup"><span data-stu-id="1add5-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="1add5-155">Tenga en cuenta que, aunque la sintaxis es similar a las entradas LocalizedString y de la sugerencia que se han descrito anteriormente, no se usa ningún carácter ' @ ' como prefijo en la \_ entrada reg SZ o REG \_ Expand, \_ que especifica la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="1add5-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="1add5-156">Paso 5:</span><span class="sxs-lookup"><span data-stu-id="1add5-156">Step 5:</span></span>

<span data-ttu-id="1add5-157">Agregue la siguiente información al registro para proporcionar el comando al que llama el sistema cuando el usuario abre el panel de control.</span><span class="sxs-lookup"><span data-stu-id="1add5-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="1add5-158">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1add5-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1add5-159">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="1add5-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="1add5-160">Cómo registrar elementos del panel de control DLL</span><span class="sxs-lookup"><span data-stu-id="1add5-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



