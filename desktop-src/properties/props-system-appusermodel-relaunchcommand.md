---
description: Especifica un comando que se puede ejecutar a través de ShellExecute para iniciar una aplicación cuando está anclada a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la Jump List de la aplicación.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706111"
---
# <a name="systemappusermodelrelaunchcommand"></a><span data-ttu-id="ee4f8-103">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="ee4f8-103">System.AppUserModel.RelaunchCommand</span></span>

<span data-ttu-id="ee4f8-104">Especifica un comando que se puede ejecutar a través de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar una aplicación cuando está anclada a la barra de tareas o cuando se inicia una nueva instancia de la aplicación a través de la Jump List de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-104">Specifies a command that can be executed through [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to launch an application when it is pinned to the taskbar or when a new instance of the application is launched through the application's Jump List.</span></span>

<span data-ttu-id="ee4f8-105">Entre otros, se incluyen los siguientes ejemplos:</span><span class="sxs-lookup"><span data-stu-id="ee4f8-105">Examples include the following:</span></span>


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



<span data-ttu-id="ee4f8-106">Esta propiedad solo se usa si una ventana tiene un identificador de modelo de usuario de aplicación explícito (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), establecido a través de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span><span class="sxs-lookup"><span data-stu-id="ee4f8-106">This property is used only if a window has an explicit Application User Model ID (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), set through [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)).</span></span> <span data-ttu-id="ee4f8-107">Si la ventana no tiene un AppUserModelID explícito, esta propiedad se omite y la ventana se agrupa y se ancla como si formara parte del proceso que la posee.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-107">If the window does not have an explicit AppUserModelID, this property is ignored and the window is grouped and pinned as if it were part of the process that owns it.</span></span> <span data-ttu-id="ee4f8-108">Para obtener más información sobre la aplicación de AppUserModelIDs explícitos y su efecto en el anclaje de la barra de tareas, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="ee4f8-108">For more information about the application of explicit AppUserModelIDs and their effect on taskbar pinning, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="ee4f8-109">Esta propiedad está pensada para ser utilizada por aplicaciones o ventanas que deseen proporcionar información de reinicio no predeterminada.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-109">This property is meant to be used by applications or windows that want to provide non-default relaunch information.</span></span>

> [!Note]  
> <span data-ttu-id="ee4f8-110">[System. AppUserModel. RelaunchCommand]() y [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) siempre se deben establecer juntos.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-110">[System.AppUserModel.RelaunchCommand]() and [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) must always be set together.</span></span> <span data-ttu-id="ee4f8-111">Si no se establece una de esas propiedades, no se utiliza ninguna.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-111">If one of those properties is not set, then neither is used.</span></span>

 

<span data-ttu-id="ee4f8-112">Esta propiedad, junto con [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) y [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) se puede usar para definir visualmente una ventana como una aplicación para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-112">This property, together with [System.AppUserModel.RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) and [System.AppUserModel.RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) can be used to visually define a window as an application to the user.</span></span> <span data-ttu-id="ee4f8-113">Esto resulta útil para escenarios de aplicaciones host, donde una sola instancia de host ejecuta varias aplicaciones secundarias.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-113">This is useful for host application scenarios, where a single host instance runs multiple child applications.</span></span> <span data-ttu-id="ee4f8-114">Por ejemplo, una máquina virtual que hospede varias aplicaciones virtualizadas podría querer que esas aplicaciones virtualizadas aparezcan como aplicaciones individuales para el usuario.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-114">For example, a virtual machine that hosts several virtualized applications might want those virtualized applications to appear as individual applications to the user.</span></span> <span data-ttu-id="ee4f8-115">La máquina virtual podría etiquetar cada ventana con un AppUserModelID explícito y las propiedades de reinicio adecuadas para que aparezcan como aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-115">The virtual machine could label each window with an explicit AppUserModelID and the appropriate relaunch properties to make them appear as applications.</span></span> <span data-ttu-id="ee4f8-116">Después, el usuario podría anclarlos a la barra de tareas y "volver a iniciar" la instancia anclada.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-116">The user could then pin them to the taskbar and "relaunch" the pinned instance.</span></span>

> [!Note]  
> <span data-ttu-id="ee4f8-117">Esta propiedad se omite si se establece [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) .</span><span class="sxs-lookup"><span data-stu-id="ee4f8-117">This property is ignored if [System.AppUserModel.PreventPinning](./props-system-appusermodel-preventpinning.md) is set.</span></span> <span data-ttu-id="ee4f8-118">Esto permite que una aplicación controle la agrupación de sus ventanas asignándoles explícitamente AppUserModelIDs, pero evitando que esas ventanas se anclen.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-118">This enables an application to control the grouping of its windows by assigning them explicit AppUserModelIDs but preventing those windows from being pinned.</span></span>

 

<span data-ttu-id="ee4f8-119">Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. RelaunchCommand]() de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-119">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.RelaunchCommand]() property of that window.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="ee4f8-120">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="ee4f8-120">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="ee4f8-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee4f8-121">Remarks</span></span>

<span data-ttu-id="ee4f8-122">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="ee4f8-122">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee4f8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee4f8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4f8-124">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="ee4f8-124">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-125">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="ee4f8-125">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-126">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="ee4f8-126">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="ee4f8-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-130">Requerida</span><span class="sxs-lookup"><span data-stu-id="ee4f8-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-132">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-132">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-133">stringFormat</span><span class="sxs-lookup"><span data-stu-id="ee4f8-133">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-134">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="ee4f8-134">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-135">Numérico</span><span class="sxs-lookup"><span data-stu-id="ee4f8-135">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-136">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="ee4f8-136">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-137">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="ee4f8-137">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-138">enum</span><span class="sxs-lookup"><span data-stu-id="ee4f8-138">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-139">enumRange</span><span class="sxs-lookup"><span data-stu-id="ee4f8-139">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-140">image</span><span class="sxs-lookup"><span data-stu-id="ee4f8-140">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="ee4f8-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-142">editControl</span><span class="sxs-lookup"><span data-stu-id="ee4f8-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="ee4f8-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-144">Consulta</span><span class="sxs-lookup"><span data-stu-id="ee4f8-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-145">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="ee4f8-145">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="ee4f8-146">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="ee4f8-146">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
