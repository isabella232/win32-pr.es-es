---
description: Deshabilita la capacidad de anclar un acceso directo o una ventana en la barra de tareas o en el menú Inicio. Esta propiedad también hace que el elemento no sea válido para su inclusión en la lista de uso más frecuente (MFU) del menú Inicio.
ms.assetid: 86239BF8-BCFC-4e76-BF94-5ABA4639562C
title: System. AppUserModel. PreventPinning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7804c615bcb35909610b06622bd25fe3dccdd0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910182"
---
# <a name="systemappusermodelpreventpinning"></a><span data-ttu-id="e6031-104">System. AppUserModel. PreventPinning</span><span class="sxs-lookup"><span data-stu-id="e6031-104">System.AppUserModel.PreventPinning</span></span>

<span data-ttu-id="e6031-105">Deshabilita la capacidad de anclar un acceso directo o una ventana en la barra de tareas o en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="e6031-105">Disables the ability of a shortcut or window to be pinned to the taskbar or the **Start** menu.</span></span> <span data-ttu-id="e6031-106">Esta propiedad también hace que el elemento no sea válido para su inclusión en la lista de uso más frecuente (MFU) del menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="e6031-106">This property also makes the item ineligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span>

<span data-ttu-id="e6031-107">Esta propiedad se debe establecer en una ventana antes de la propiedad [PKEY \_ AppUserModel \_ ID](./props-system-appusermodel-id.md) .</span><span class="sxs-lookup"><span data-stu-id="e6031-107">This property must be set on a window before the [PKEY\_AppUserModel\_ID](./props-system-appusermodel-id.md) property.</span></span> <span data-ttu-id="e6031-108">Una vez \_ establecida la propiedad PKEY AppUserModel \_ ID, se omiten los cambios en [PKEY \_ AppUserModel \_ PreventPinning]() .</span><span class="sxs-lookup"><span data-stu-id="e6031-108">After the PKEY\_AppUserModel\_ID property is set, changes to [PKEY\_AppUserModel\_PreventPinning]() are ignored.</span></span>

<span data-ttu-id="e6031-109">Para obtener más información sobre los identificadores de modelo de usuario de la aplicación (AppUserModelIDs) y otros métodos para excluir un elemento de su anclaje a la barra de tareas y de la inclusión de MFU, vea [identificadores de modelo de usuario de aplicación (AppUserModelIDs)](../shell/appids.md).</span><span class="sxs-lookup"><span data-stu-id="e6031-109">For more information about Application User Model IDs (AppUserModelIDs) and other methods of excluding an item from being pinned to the taskbar and from MFU inclusion, see [Application User Model IDs (AppUserModelIDs)](../shell/appids.md).</span></span>

<span data-ttu-id="e6031-110">Para establecer esta propiedad en una ventana, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar el almacén de propiedades de la ventana y use los métodos de ese objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) recuperado para establecer la propiedad [System. AppUserModel. PreventPinning]() de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="e6031-110">To set this property on a window, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store, and use the methods of that retrieved [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) object to set the [System.AppUserModel.PreventPinning]() property of that window.</span></span>

<span data-ttu-id="e6031-111">Al establecer esta propiedad, se omiten las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="e6031-111">Setting this property causes the following properties to be ignored:</span></span>

-   [<span data-ttu-id="e6031-112">System. AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="e6031-112">System.AppUserModel.RelaunchCommand</span></span>](./props-system-appusermodel-relaunchcommand.md)
-   [<span data-ttu-id="e6031-113">System. AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="e6031-113">System.AppUserModel.RelaunchDisplayNameResource</span></span>](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [<span data-ttu-id="e6031-114">System. AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="e6031-114">System.AppUserModel.RelaunchIconResource</span></span>](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="e6031-115">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6031-115">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.PreventPinning
   shellPKey = PKEY_AppUserModel_PreventPinning
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="e6031-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6031-116">Remarks</span></span>

<span data-ttu-id="e6031-117">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="e6031-117">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6031-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e6031-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6031-119">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="e6031-119">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="e6031-120">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="e6031-120">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="e6031-121">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="e6031-121">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="e6031-122">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="e6031-122">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="e6031-123">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="e6031-123">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="e6031-124">searchInfo</span><span class="sxs-lookup"><span data-stu-id="e6031-124">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-125">labelInfo</span><span class="sxs-lookup"><span data-stu-id="e6031-125">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-126">Requerida</span><span class="sxs-lookup"><span data-stu-id="e6031-126">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-127">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e6031-127">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-128">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="e6031-128">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="e6031-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="e6031-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="e6031-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="e6031-131">Numérico</span><span class="sxs-lookup"><span data-stu-id="e6031-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="e6031-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="e6031-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="e6031-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="e6031-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="e6031-134">enum</span><span class="sxs-lookup"><span data-stu-id="e6031-134">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="e6031-135">enumRange</span><span class="sxs-lookup"><span data-stu-id="e6031-135">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="e6031-136">image</span><span class="sxs-lookup"><span data-stu-id="e6031-136">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="e6031-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="e6031-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="e6031-138">editControl</span><span class="sxs-lookup"><span data-stu-id="e6031-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="e6031-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="e6031-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="e6031-140">Consulta</span><span class="sxs-lookup"><span data-stu-id="e6031-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="e6031-141">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="e6031-141">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="e6031-142">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="e6031-142">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
