---
description: Especifica si se comprueba la ruta de acceso del vínculo en System. Link. TargetParsingPath.
ms.assetid: 38c73501-6376-41bb-8ad0-8f94ad42dfc9
title: System. Link. status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9b4a6b398ba022f9f62a0860262028ced49a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677718"
---
# <a name="systemlinkstatus"></a><span data-ttu-id="57a29-103">System. Link. status</span><span class="sxs-lookup"><span data-stu-id="57a29-103">System.Link.Status</span></span>

<span data-ttu-id="57a29-104">Especifica si se comprueba la ruta de acceso del vínculo en [System. Link. TargetParsingPath](./props-system-link-targetparsingpath.md) .</span><span class="sxs-lookup"><span data-stu-id="57a29-104">Specifies whether the link path in [System.Link.TargetParsingPath](./props-system-link-targetparsingpath.md) is verified.</span></span> <span data-ttu-id="57a29-105">Estos valores se definen.</span><span class="sxs-lookup"><span data-stu-id="57a29-105">These values are defined.</span></span>

-   <span data-ttu-id="57a29-106">**Sin resolver** (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="57a29-106">**Unresolved** (default)</span></span>
-   <span data-ttu-id="57a29-107">Resuelto</span><span class="sxs-lookup"><span data-stu-id="57a29-107">Resolved</span></span>
-   <span data-ttu-id="57a29-108">Deteriora</span><span class="sxs-lookup"><span data-stu-id="57a29-108">Broken</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="57a29-109">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="57a29-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Resolved
            value = 1
            text = Resolved
            defineToken = LINK_STATUS_RESOLVED
         enum
            name = Broken
            value = 2
            text = Broken
            defineToken = LINK_STATUS_BROKEN
```

## <a name="windows-vista"></a><span data-ttu-id="57a29-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57a29-110">Windows Vista</span></span>

```
propertyDescription
   name = System.Link.Status
   shellPKey = PKEY_Link_Status
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = Resolved
            defineName = LINK_STATUS_RESOLVED
         enum
            value = 2
            text = Broken
            defineName = LINK_STATUS_BROKEN
```

## <a name="remarks"></a><span data-ttu-id="57a29-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57a29-111">Remarks</span></span>

<span data-ttu-id="57a29-112">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="57a29-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57a29-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="57a29-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a29-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="57a29-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="57a29-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="57a29-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="57a29-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="57a29-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="57a29-117">Requerida</span><span class="sxs-lookup"><span data-stu-id="57a29-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="57a29-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="57a29-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="57a29-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="57a29-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="57a29-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="57a29-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="57a29-121">Numérico</span><span class="sxs-lookup"><span data-stu-id="57a29-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="57a29-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="57a29-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="57a29-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="57a29-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="57a29-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="57a29-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="57a29-125">editControl</span><span class="sxs-lookup"><span data-stu-id="57a29-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="57a29-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="57a29-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="57a29-127">Consulta</span><span class="sxs-lookup"><span data-stu-id="57a29-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
