---
description: Especifica el icono que se usa para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc79c246fef7be5641c6488dcc34169cd5bbf98b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666847"
---
# <a name="systemappusermodelrelaunchiconresource"></a><span data-ttu-id="f6d2a-103">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="f6d2a-103">System.AppUserModel.RelaunchIconResource</span></span>

<span data-ttu-id="f6d2a-104">Especifica el icono que se usa para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-104">Specifies the icon used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="f6d2a-105">Este es el icono que se usa para el grupo de la barra de tareas y se muestra para una aplicación anclada si esa aplicación se está ejecutando o no.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-105">This is the icon used for the taskbar group and is shown for a pinned application whether that application is running or not.</span></span> <span data-ttu-id="f6d2a-106">Debe especificarse en uno de los siguientes formatos:</span><span class="sxs-lookup"><span data-stu-id="f6d2a-106">This should be specified in one of the following formats:</span></span>

-   <span data-ttu-id="f6d2a-107">Formato de recursos estándar, como "% systemdir% \\ system32 \\shell32.dll,-128".</span><span class="sxs-lookup"><span data-stu-id="f6d2a-107">Standard resource format, such as "%systemdir%\\system32\\shell32.dll,-128".</span></span> <span data-ttu-id="f6d2a-108">El carácter "-" antes del identificador de recurso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-108">The '-' character before the resource ID is required.</span></span> <span data-ttu-id="f6d2a-109">No use el carácter ' @ ' situado al principio de la cadena de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-109">Do not use the '@' character at the front of the path string.</span></span>
-   <span data-ttu-id="f6d2a-110">Ruta de acceso directa a un archivo de icono, como "% ProgramFiles% \\ Microsoft \\ Notepad \\ Notepad. ico, 0".</span><span class="sxs-lookup"><span data-stu-id="f6d2a-110">Direct path to an icon file, such as "%programfiles%\\Microsoft\\Notepad\\Notepad.ico,0".</span></span> <span data-ttu-id="f6d2a-111">Tenga en cuenta que, dado que los archivos. ico pueden contener varios recursos de icono, se requiere un identificador de recurso en la cadena.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-111">Note that because .ico files can contain multiple icon resources, a resource ID is required in the string.</span></span> <span data-ttu-id="f6d2a-112">Si el archivo. ico es una sola imagen, use "0" (sin el carácter "-") como identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-112">If the .ico file is a single image, use "0" (without the '-' character) as the resource ID.</span></span>

<span data-ttu-id="f6d2a-113">[System. AppUserModel. RelaunchIconResource]() es una propiedad opcional.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-113">[System.AppUserModel.RelaunchIconResource]() is an optional property.</span></span> <span data-ttu-id="f6d2a-114">Si no se establece, se usa el icono del destino del comando de reinicio ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)).</span><span class="sxs-lookup"><span data-stu-id="f6d2a-114">If it is not set, the icon of the target of the relaunch command ([System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) is used.</span></span> <span data-ttu-id="f6d2a-115">Sin embargo, dado que esto puede dar lugar a resultados no deseados, le recomendamos encarecidamente que proporcione un icono explícitamente a través de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-115">However, because that can lead to undesired results, we strongly encourage you to provide an icon explicitly through this property.</span></span>

<span data-ttu-id="f6d2a-116">Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="f6d2a-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="f6d2a-117">Si la ventana no tiene un AppUserModelID explícito (System.AppUserModel.ID), esta propiedad se omite y la ventana se agrupa y se ancla como si formara parte de su proceso propietario.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-117">If the window does not have an explicit AppUserModelID (System.AppUserModel.ID), this property is ignored and the window is grouped and pinned as if it were part of its owning process.</span></span> <span data-ttu-id="f6d2a-118">Para obtener más información sobre la aplicación de AppUserModelIDs explícitos y su efecto en el anclaje de la barra de tareas, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="f6d2a-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="f6d2a-119">Esta propiedad está pensada para ser utilizada por aplicaciones o ventanas que deseen proporcionar información de reinicio no predeterminada.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="f6d2a-120">Para obtener más información, vea [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="f6d2a-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

<span data-ttu-id="f6d2a-121">Si se establece un AppUserModelID explícito en la ventana, pero no se establece esta propiedad, el sistema intenta encontrar un acceso directo con el mismo AppUserModelID y ancla ese acceso directo a la barra de tareas para representar la ventana.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-121">If an explicit AppUserModelID is set on the window, but this property is not set, the system attempts to find a shortcut with the same AppUserModelID, and pins that shortcut to the taskbar to represent the window.</span></span> <span data-ttu-id="f6d2a-122">Si no se puede encontrar este método abreviado, se utiliza el ejecutable de respaldo del proceso que lo posee.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-122">If no such shortcut can be located, then the backing executable of the process that owns it is used.</span></span>

> [!Note]  
> <span data-ttu-id="f6d2a-123">Esta propiedad se omite si se establece [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="f6d2a-123">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="f6d2a-124">Esto permite que una aplicación controle la agrupación de sus ventanas asignándoles explícitamente AppUserModelIDs, pero evitando que esas ventanas se anclen.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-124">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="f6d2a-125">Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. RelaunchIconResource]() de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="f6d2a-125">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchIconResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a><span data-ttu-id="f6d2a-126">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f6d2a-126">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a><span data-ttu-id="f6d2a-127">Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f6d2a-127">Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a><span data-ttu-id="f6d2a-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f6d2a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6d2a-129">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="f6d2a-129">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-130">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="f6d2a-130">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-131">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="f6d2a-131">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f6d2a-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f6d2a-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f6d2a-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-135">Requerida</span><span class="sxs-lookup"><span data-stu-id="f6d2a-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f6d2a-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-137">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="f6d2a-137">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f6d2a-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f6d2a-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-140">Numérico</span><span class="sxs-lookup"><span data-stu-id="f6d2a-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f6d2a-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f6d2a-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-143">enum</span><span class="sxs-lookup"><span data-stu-id="f6d2a-143">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-144">enumRange</span><span class="sxs-lookup"><span data-stu-id="f6d2a-144">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-145">image</span><span class="sxs-lookup"><span data-stu-id="f6d2a-145">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-146">drawControl</span><span class="sxs-lookup"><span data-stu-id="f6d2a-146">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-147">editControl</span><span class="sxs-lookup"><span data-stu-id="f6d2a-147">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-148">filterControl</span><span class="sxs-lookup"><span data-stu-id="f6d2a-148">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-149">Consulta</span><span class="sxs-lookup"><span data-stu-id="f6d2a-149">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-150">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="f6d2a-150">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="f6d2a-151">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="f6d2a-151">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
