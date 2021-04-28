---
description: System.OfflineStatus
ms.assetid: 0badb5dd-6342-4110-b7a9-0b291dfe8578
title: System.OfflineStatus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11789e1bdf11787c363bcfb4e714494d2ab6647d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097313"
---
# <a name="systemofflinestatus"></a><span data-ttu-id="5f996-103">System.OfflineStatus</span><span class="sxs-lookup"><span data-stu-id="5f996-103">System.OfflineStatus</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="5f996-104">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="5f996-104">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.OfflineStatus
   shellPKey = PKEY_OfflineStatus
   formatID = 6D24888F-4718-4BDA-AFED-EA0FB4386CD8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Online
            value = 0
            text = Online
            defineToken = OFFLINESTATUS_ONLINE
         enum
            name = Offline
            value = 1
            text = Offline
            defineToken = OFFLINESTATUS_OFFLINE
         enum
            name = OfflineForced
            value = 2
            text = Offline (working offline)
            defineToken = OFFLINESTATUS_OFFLINE_FORCED
         enum
            name = OfflineSlow
            value = 3
            text = Offline (background sync)
            defineToken = OFFLINESTATUS_OFFLINE_SLOW
         enum
            name = OfflineError
            value = 4
            text = Offline (not connected)
            defineToken = OFFLINESTATUS_OFFLINE_ERROR
         enum
            name = OfflineConflict
            value = 5
            text = Offline (need to sync)
            defineToken = OFFLINESTATUS_OFFLINE_ITEM_VERSION_CONFLICT
         enum
            name = OfflineSuspended
            value = 6
            text = Offline (always)
            defineToken = OFFLINESTATUS_OFFLINE_SUSPENDED
```

## <a name="windows-7"></a><span data-ttu-id="5f996-105">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5f996-105">Windows 7</span></span>

```
propertyDescription
   name = System.OfflineStatus
   shellPKey = PKEY_OfflineStatus
   formatID = 6D24888F-4718-4BDA-AFED-EA0FB4386CD8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Online
            value = 0
            text = Online
            defineToken = OFFLINESTATUS_ONLINE
         enum
            name = Offline
            value = 1
            text = Offline
            defineToken = OFFLINESTATUS_OFFLINE
         enum
            name = OfflineForced
            value = 2
            text = Offline (working offline)
            defineToken = OFFLINESTATUS_OFFLINE_FORCED
         enum
            name = OfflineSlow
            value = 3
            text = Offline (slow connection)
            defineToken = OFFLINESTATUS_OFFLINE_SLOW
         enum
            name = OfflineError
            value = 4
            text = Offline (not connected)
            defineToken = OFFLINESTATUS_OFFLINE_ERROR
         enum
            name = OfflineConflict
            value = 5
            text = Offline (need to sync)
            defineToken = OFFLINESTATUS_OFFLINE_ITEM_VERSION_CONFLICT
         enum
            name = OfflineSuspended
            value = 6
            text = Offline (always)
            defineToken = OFFLINESTATUS_OFFLINE_SUSPENDED
```

## <a name="windows-vista"></a><span data-ttu-id="5f996-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5f996-106">Windows Vista</span></span>

```
propertyDescription
   name = System.OfflineStatus
   shellPKey = PKEY_OfflineStatus
   formatID = 6D24888F-4718-4BDA-AFED-EA0FB4386CD8
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 0
            text = Online
            defineName = OFFLINESTATUS_ONLINE
         enum
            value = 1
            text = Offline
            defineName = OFFLINESTATUS_OFFLINE
         enum
            value = 2
            text = Offline (working offline)
            defineName = OFFLINESTATUS_OFFLINE_FORCED
         enum
            value = 3
            text = Offline (slow connection)
            defineName = OFFLINESTATUS_OFFLINE_SLOW
         enum
            value = 4
            text = Offline (not connected)
            defineName = OFFLINESTATUS_OFFLINE_ERROR
         enum
            value = 5
            text = Offline (need to sync)
            defineName = OFFLINESTATUS_OFFLINE_ITEM_VERSION_CONFLICT
         enum
            value = 6
            text = Offline (always)
            defineName = OFFLINESTATUS_OFFLINE_SUSPENDED
```

## <a name="remarks"></a><span data-ttu-id="5f996-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f996-107">Remarks</span></span>

<span data-ttu-id="5f996-108">Los valores PKEY se definen en Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="5f996-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f996-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5f996-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f996-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="5f996-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="5f996-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="5f996-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="5f996-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="5f996-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="5f996-113">typeInfo</span><span class="sxs-lookup"><span data-stu-id="5f996-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="5f996-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="5f996-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="5f996-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="5f996-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="5f996-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="5f996-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="5f996-117">numberFormat</span><span class="sxs-lookup"><span data-stu-id="5f996-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="5f996-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="5f996-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="5f996-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="5f996-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="5f996-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="5f996-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="5f996-121">editControl</span><span class="sxs-lookup"><span data-stu-id="5f996-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="5f996-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="5f996-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="5f996-123">queryControl</span><span class="sxs-lookup"><span data-stu-id="5f996-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
