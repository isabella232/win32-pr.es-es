---
description: Especifica el nombre para mostrar utilizado para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276904"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a><span data-ttu-id="ff76f-103">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="ff76f-103">System.AppUserModel.RelaunchDisplayNameResource</span></span>

<span data-ttu-id="ff76f-104">Especifica el nombre para mostrar utilizado para el acceso directo creado en la barra de tareas cuando el usuario elige anclar una aplicación a la barra de tareas o iniciar una nueva instancia a través de la Jump List del botón.</span><span class="sxs-lookup"><span data-stu-id="ff76f-104">Specifies the display name used for the shortcut created on the taskbar when the user chooses to pin an application to the taskbar or launch a new instance through its button's Jump List.</span></span> <span data-ttu-id="ff76f-105">El valor de esta propiedad debe ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="ff76f-105">The value of this property must be one of the following:</span></span>

-   <span data-ttu-id="ff76f-106">Cadena de recursos indirecta como "@% systemdir% \\ system32 \\shell32.dll,-19263".</span><span class="sxs-lookup"><span data-stu-id="ff76f-106">An indirect resource string such as "@%systemdir%\\system32\\shell32.dll,-19263".</span></span> <span data-ttu-id="ff76f-107">Tenga en cuenta que el carácter ' @ ' es necesario para distinguir una cadena indirecta de una cadena de texto sin formato (descrita en el párrafo siguiente con viñetas).</span><span class="sxs-lookup"><span data-stu-id="ff76f-107">Note that the '@' character is required to distinguish an indirect string from a plain-text string (described in the next bulleted paragraph).</span></span> <span data-ttu-id="ff76f-108">Esta cadena indirecta se compone de un archivo binario y un identificador de recurso de la cadena contenida en ese binario.</span><span class="sxs-lookup"><span data-stu-id="ff76f-108">This indirect string consists of a binary file and a resource ID of the string contained in that binary.</span></span> <span data-ttu-id="ff76f-109">Se recomienda encarecidamente que utilice esta forma de cadena indirecta, lo que garantiza que el nombre para mostrar cambie correctamente cuando se cambie el idioma del sistema a través de la interfaz de usuario multilingüe (MUI).</span><span class="sxs-lookup"><span data-stu-id="ff76f-109">We strongly recommend that you use this indirect string form, which ensures that the display name changes appropriately when the system language is changed through the Multilingual User Interface (MUI).</span></span> <span data-ttu-id="ff76f-110">El carácter "-" antes del identificador de recurso es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ff76f-110">The '-' character before the resource ID is required.</span></span>
-   <span data-ttu-id="ff76f-111">Cadena de texto sin formato que no señala a un recurso.</span><span class="sxs-lookup"><span data-stu-id="ff76f-111">A plain-text string that does not point to a resource.</span></span> <span data-ttu-id="ff76f-112">Solo se debe usar cuando el nombre para mostrar se calcula o se obtiene dinámicamente a partir de un origen de datos que no admite MUI.</span><span class="sxs-lookup"><span data-stu-id="ff76f-112">This should only be used when the display name is dynamically calculated or obtained from a data source that does not support MUI.</span></span> <span data-ttu-id="ff76f-113">Por ejemplo, la cadena podría ser el nombre de un dispositivo, como "Microsoft Zune", en los casos en los que la aplicación aparece cuando el dispositivo está conectado al equipo.</span><span class="sxs-lookup"><span data-stu-id="ff76f-113">For example, the string could be the name of a device, such as "Microsoft Zune", in cases where the application appears when that device is attached to the computer.</span></span>

> [!Note]  
> <span data-ttu-id="ff76f-114">[System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) y [System. AppUserModel. RelaunchDisplayNameResource]() siempre se deben establecer juntos.</span><span class="sxs-lookup"><span data-stu-id="ff76f-114">[System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) and [System.AppUserModel.RelaunchDisplayNameResource]() must always be set together.</span></span> <span data-ttu-id="ff76f-115">Si no se establece una de esas propiedades, no se utiliza ninguna.</span><span class="sxs-lookup"><span data-stu-id="ff76f-115">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="ff76f-116">Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="ff76f-116">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="ff76f-117">Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y se ancla como si formara parte del proceso que la posee.</span><span class="sxs-lookup"><span data-stu-id="ff76f-117">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="ff76f-118">Para obtener más información sobre la aplicación de AppUserModelIDs explícitos y su efecto en el anclaje de la barra de tareas, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="ff76f-118">For more information on the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span> <span data-ttu-id="ff76f-119">Esta propiedad está pensada para ser utilizada por aplicaciones o ventanas que deseen proporcionar información de reinicio no predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ff76f-119">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span> <span data-ttu-id="ff76f-120">Para obtener más información, vea [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span><span class="sxs-lookup"><span data-stu-id="ff76f-120">For more information, see [System.AppUserModel.RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).</span></span>

> [!Note]  
> <span data-ttu-id="ff76f-121">Esta propiedad se omite si se establece [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="ff76f-121">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="ff76f-122">Esto permite que una aplicación controle la agrupación de sus ventanas asignándoles explícitamente AppUserModelIDs, pero evitando que esas ventanas se anclen.</span><span class="sxs-lookup"><span data-stu-id="ff76f-122">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="ff76f-123">Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. RelaunchDisplayNameResource]() de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="ff76f-123">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchDisplayNameResource]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="ff76f-124">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ff76f-124">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="ff76f-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff76f-125">Remarks</span></span>

<span data-ttu-id="ff76f-126">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="ff76f-126">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff76f-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff76f-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff76f-128">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="ff76f-128">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="ff76f-129">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="ff76f-129">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="ff76f-130">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="ff76f-130">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="ff76f-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ff76f-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ff76f-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ff76f-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ff76f-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-134">Requerida</span><span class="sxs-lookup"><span data-stu-id="ff76f-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ff76f-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-136">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="ff76f-136">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ff76f-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ff76f-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ff76f-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ff76f-139">Numérico</span><span class="sxs-lookup"><span data-stu-id="ff76f-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ff76f-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ff76f-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ff76f-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ff76f-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ff76f-142">enum</span><span class="sxs-lookup"><span data-stu-id="ff76f-142">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="ff76f-143">enumRange</span><span class="sxs-lookup"><span data-stu-id="ff76f-143">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="ff76f-144">image</span><span class="sxs-lookup"><span data-stu-id="ff76f-144">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="ff76f-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="ff76f-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ff76f-146">editControl</span><span class="sxs-lookup"><span data-stu-id="ff76f-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ff76f-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="ff76f-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ff76f-148">Consulta</span><span class="sxs-lookup"><span data-stu-id="ff76f-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="ff76f-149">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="ff76f-149">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="ff76f-150">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="ff76f-150">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
