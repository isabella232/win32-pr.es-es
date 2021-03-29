---
description: Si esta propiedad es true, el dispositivo está conectado a una red.
ms.assetid: 4d0aa672-1ff8-4fb1-82d2-76553c2b0209
title: System. Devices. IsNetworkConnected
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c016b97dc3e966407582e0447ddeae1c4ffb86d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813523"
---
# <a name="systemdevicesisnetworkconnected"></a><span data-ttu-id="c11e0-103">System. Devices. IsNetworkConnected</span><span class="sxs-lookup"><span data-stu-id="c11e0-103">System.Devices.IsNetworkConnected</span></span>

<span data-ttu-id="c11e0-104">Si esta propiedad es true, el dispositivo está conectado a una red.</span><span class="sxs-lookup"><span data-stu-id="c11e0-104">If this property is true, the device is connected to a network.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="c11e0-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="c11e0-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkConnected
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
```

## <a name="windows-7"></a><span data-ttu-id="c11e0-106">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c11e0-106">Windows 7</span></span>

```
propertyDescription
   name = System.Devices.IsNetworkConnected
   shellPKey = PKEY_Devices_IsNetworkDevice
   formatID = 78C34FC8-104A-4ACA-9EA4-524D52996E57
   propID = 85
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = NetworkConnected
            value = #TRUE#
            text = Network Connected
            defineToken = ISNETWORKDEVICE_NETWORKDEVICE
         enum
            name = NotNetworkConnected
            value = #FALSE#
            text = Not Network Connected
            defineToken = ISNETWORKDEVICE_NOTNETWORKDEVICE
```

## <a name="remarks"></a><span data-ttu-id="c11e0-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c11e0-107">Remarks</span></span>

<span data-ttu-id="c11e0-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c11e0-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c11e0-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c11e0-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c11e0-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c11e0-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c11e0-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c11e0-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c11e0-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c11e0-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c11e0-113">Requerida</span><span class="sxs-lookup"><span data-stu-id="c11e0-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c11e0-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c11e0-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c11e0-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c11e0-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c11e0-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c11e0-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c11e0-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="c11e0-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c11e0-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c11e0-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c11e0-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c11e0-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c11e0-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="c11e0-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c11e0-121">editControl</span><span class="sxs-lookup"><span data-stu-id="c11e0-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c11e0-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="c11e0-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c11e0-123">Consulta</span><span class="sxs-lookup"><span data-stu-id="c11e0-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
