---
description: Impide que una entrada del menú Inicio para un acceso directo de la aplicación recién instalado reciba un resaltado.
ms.assetid: ff85da6f-a506-4225-8ac9-4a8a7be8d599
title: System. AppUserModel. ExcludeFromShowInNewInstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206cbbc6b07b0d3fec5833c046d4cb44c1e5e4e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706347"
---
# <a name="systemappusermodelexcludefromshowinnewinstall"></a><span data-ttu-id="3353b-103">System. AppUserModel. ExcludeFromShowInNewInstall</span><span class="sxs-lookup"><span data-stu-id="3353b-103">System.AppUserModel.ExcludeFromShowInNewInstall</span></span>

<span data-ttu-id="3353b-104">Impide que una entrada del menú **Inicio** para un acceso directo de la aplicación recién instalado reciba un resaltado.</span><span class="sxs-lookup"><span data-stu-id="3353b-104">Prevents a **Start** menu entry for a newly installed application shortcut from receiving a highlight.</span></span> <span data-ttu-id="3353b-105">Esto es equivalente a desactivar la opción **resaltar programas recién instalados** en la ventana **personalizar el menú Inicio** en un elemento individual.</span><span class="sxs-lookup"><span data-stu-id="3353b-105">This is equivalent to clearing the **Highlight newly installed programs** option in the **Customize Start Menu** window on an individual item.</span></span> <span data-ttu-id="3353b-106">Esta propiedad se debe establecer en métodos abreviados para las herramientas y aplicaciones secundarias.</span><span class="sxs-lookup"><span data-stu-id="3353b-106">This property should be set on shortcuts for tools and secondary applications.</span></span>

> [!Note]  
> <span data-ttu-id="3353b-107">Esta propiedad solo se usa en el menú Inicio de Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3353b-107">This property is property is only used by the Start menu on Windows Vista and Windows 7.</span></span> <span data-ttu-id="3353b-108">La propiedad no se usa en la pantalla Inicio o el menú Inicio en Windows 8 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="3353b-108">The property is not used by the Start screen or Start menu on Windows 8 and later</span></span>

 

<span data-ttu-id="3353b-109">.</span><span class="sxs-lookup"><span data-stu-id="3353b-109">.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="3353b-110">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="3353b-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.AppUserModel.ExcludeFromShowInNewInstall
   shellPKey = PKEY_AppUserModel_ExcludeFromShowInNewInstall
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = false
```

## <a name="remarks"></a><span data-ttu-id="3353b-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3353b-111">Remarks</span></span>

<span data-ttu-id="3353b-112">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="3353b-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3353b-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3353b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3353b-114">Identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</span><span class="sxs-lookup"><span data-stu-id="3353b-114">Application User Model IDs (AppUserModelIDs)</span></span>](../shell/appids.md)
</dt> <dt>

[<span data-ttu-id="3353b-115">System.AppUserModel.ID</span><span class="sxs-lookup"><span data-stu-id="3353b-115">System.AppUserModel.ID</span></span>](./props-system-appusermodel-id.md)
</dt> <dt>

[<span data-ttu-id="3353b-116">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="3353b-116">**SHGetPropertyStoreForWindow**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> <dt>

[<span data-ttu-id="3353b-117">propertyDescriptionList</span><span class="sxs-lookup"><span data-stu-id="3353b-117">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="3353b-118">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="3353b-118">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="3353b-119">searchInfo</span><span class="sxs-lookup"><span data-stu-id="3353b-119">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-120">labelInfo</span><span class="sxs-lookup"><span data-stu-id="3353b-120">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-121">Requerida</span><span class="sxs-lookup"><span data-stu-id="3353b-121">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-122">displayInfo</span><span class="sxs-lookup"><span data-stu-id="3353b-122">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-123">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="3353b-123">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="3353b-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="3353b-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="3353b-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="3353b-126">Numérico</span><span class="sxs-lookup"><span data-stu-id="3353b-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="3353b-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3353b-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="3353b-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="3353b-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="3353b-129">enum</span><span class="sxs-lookup"><span data-stu-id="3353b-129">enum</span></span>](./propdesc-schema-enum.md)
</dt> <dt>

[<span data-ttu-id="3353b-130">enumRange</span><span class="sxs-lookup"><span data-stu-id="3353b-130">enumRange</span></span>](./propdesc-schema-enumrange.md)
</dt> <dt>

[<span data-ttu-id="3353b-131">image</span><span class="sxs-lookup"><span data-stu-id="3353b-131">image</span></span>](./propdesc-schema-image.md)
</dt> <dt>

[<span data-ttu-id="3353b-132">drawControl</span><span class="sxs-lookup"><span data-stu-id="3353b-132">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="3353b-133">editControl</span><span class="sxs-lookup"><span data-stu-id="3353b-133">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="3353b-134">filterControl</span><span class="sxs-lookup"><span data-stu-id="3353b-134">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="3353b-135">Consulta</span><span class="sxs-lookup"><span data-stu-id="3353b-135">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="3353b-136">relatedPropertyInfo</span><span class="sxs-lookup"><span data-stu-id="3353b-136">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[<span data-ttu-id="3353b-137">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="3353b-137">relatedProperty</span></span>](./propdesc-schema-relatedproperty.md)
</dt> <dt>

<span data-ttu-id="3353b-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3353b-138">[startPinOption](/previous-versions//jj553605(v=vs.85))</span></span>
</dt> </dl>

 

 
