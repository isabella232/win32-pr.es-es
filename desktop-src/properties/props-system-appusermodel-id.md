---
description: Un identificador de modelo de usuario de aplicación explícito (AppUserModelID) que se usa para asociar procesos, archivos y ventanas a una aplicación determinada.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c636b2c946f1138f4a25c3129a7a3b44d31558
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360555"
---
# <a name="systemappusermodelid"></a><span data-ttu-id="9add1-103">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="9add1-103">System.AppUserModel.ID</span></span>

<span data-ttu-id="9add1-104">Un identificador de modelo de usuario de aplicación explícito (AppUserModelID) que se usa para asociar procesos, archivos y ventanas a una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="9add1-104">An explicit Application User Model ID (AppUserModelID) used to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="9add1-105">En algunos casos, es suficiente confiar en el AppUserModelID interno asignado a un proceso por el sistema.</span><span class="sxs-lookup"><span data-stu-id="9add1-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="9add1-106">Sin embargo, una aplicación que posee varios procesos o una aplicación que se ejecuta en un proceso de host puede tener que identificarse explícitamente a través de esta propiedad para que pueda agrupar las ventanas dispares de otro modo en un solo botón de la barra de tareas y controlar el contenido de la Jump List de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="9add1-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself through this property so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

<span data-ttu-id="9add1-107">Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System.AppUserModel.ID]() de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="9add1-107">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.ID]() property of that window.</span></span>

<span data-ttu-id="9add1-108">Para obtener más información, vea [identificadores de modelo de usuario de la aplicación (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="9add1-108">For more information, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="9add1-109">En el momento en que se establece la propiedad [System.AppUserModel.ID]() , se notifica a la barra de tareas que actualice su información en la ventana o el acceso directo dado ese AppUserModelID.</span><span class="sxs-lookup"><span data-stu-id="9add1-109">At the time the [System.AppUserModel.ID]() property is set, the taskbar is notified to refresh its information on the window or shortcut given that AppUserModelID.</span></span>

<span data-ttu-id="9add1-110">Otras propiedades de ventana y acceso directo se pueden usar junto con un AppUserModelID explícito para controlar aún más la agrupación y el anclaje asociados a una ventana, el nombre para mostrar y el icono que se usan en la barra de tareas, y el comando para iniciar una aplicación anclada a la barra de tareas o una nueva instancia de la aplicación a través de la Jump List de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="9add1-110">Other window and shortcut properties can be used in conjunction with an explicit AppUserModelID to further control the grouping and pinning associated with a window, the display name and icon used for it in the taskbar, and the command to launch either an application pinned to the taskbar or a new instance of the application through that application's Jump List.</span></span> <span data-ttu-id="9add1-111">Estas propiedades se deben establecer antes de establecer la propiedad [System.AppUserModel.ID]() .</span><span class="sxs-lookup"><span data-stu-id="9add1-111">These properties should be set before setting the [System.AppUserModel.ID]() property.</span></span> <span data-ttu-id="9add1-112">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9add1-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9add1-113">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="9add1-113">System.AppUserModel.PreventPinning</span></span>](./props-system-appusermodel-preventpinning.md)
-   [<span data-ttu-id="9add1-114">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="9add1-114">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="9add1-115">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="9add1-115">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="9add1-116">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="9add1-116">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="9add1-117">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="9add1-117">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="9add1-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9add1-118">Remarks</span></span>

<span data-ttu-id="9add1-119">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="9add1-119">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9add1-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9add1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9add1-121">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="9add1-121">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="9add1-122">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="9add1-122">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="9add1-123">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="9add1-123">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="9add1-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="9add1-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="9add1-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="9add1-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="9add1-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-127">Requerida</span><span class="sxs-lookup"><span data-stu-id="9add1-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="9add1-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-129">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="9add1-129">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-130">stringFormat</span><span class="sxs-lookup"><span data-stu-id="9add1-130">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="9add1-131">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="9add1-131">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="9add1-132">Numérico</span><span class="sxs-lookup"><span data-stu-id="9add1-132">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="9add1-133">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="9add1-133">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="9add1-134">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="9add1-134">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="9add1-135">enum</span><span class="sxs-lookup"><span data-stu-id="9add1-135">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="9add1-136">enumRange</span><span class="sxs-lookup"><span data-stu-id="9add1-136">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="9add1-137">image</span><span class="sxs-lookup"><span data-stu-id="9add1-137">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="9add1-138">drawControl</span><span class="sxs-lookup"><span data-stu-id="9add1-138">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="9add1-139">editControl</span><span class="sxs-lookup"><span data-stu-id="9add1-139">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="9add1-140">filterControl</span><span class="sxs-lookup"><span data-stu-id="9add1-140">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="9add1-141">Consulta</span><span class="sxs-lookup"><span data-stu-id="9add1-141">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="9add1-142">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="9add1-142">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="9add1-143">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="9add1-143">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
