---
description: Intensidad de la señal del dispositivo.
ms.assetid: 662d39a6-f2f5-4556-a6de-bbcc655b4adb
title: System. Devices. SignalStrength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901179dcf142f03ffceea14778f2763f73f16276
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649235"
---
# <a name="systemdevicessignalstrength"></a><span data-ttu-id="bbc18-103">System. Devices. SignalStrength</span><span class="sxs-lookup"><span data-stu-id="bbc18-103">System.Devices.SignalStrength</span></span>

<span data-ttu-id="bbc18-104">Intensidad de la señal del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bbc18-104">Device signal strength.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="bbc18-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="bbc18-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Devices.SignalStrength
   shellPKey = PKEY_Devices_SignalStrength
   formatID = 49CD1F76-5626-4B17-A4E8-18B4AA1A2213
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Byte
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = None
            value = 0
            text = No signal
            defineToken = SIGNALSTRENGTH_NONE
         enum
            name = Weak
            value = 1
            text = Weak signal
            defineToken = SIGNALSTRENGTH_WEAK
         enum
            name = Average
            value = 2
            text = Average signal
            defineToken = SIGNALSTRENGTH_AVERAGE
         enum
            name = Strong
            value = 3
            text = Strong signal
            defineToken = SIGNALSTRENGTH_STRONG
         enum
            name = Excellent
            value = 4
            text = Excellent signal
            defineToken = SIGNALSTRENGTH_EXCELLENT
```

## <a name="remarks"></a><span data-ttu-id="bbc18-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbc18-106">Remarks</span></span>

<span data-ttu-id="bbc18-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="bbc18-107">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbc18-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bbc18-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbc18-109">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="bbc18-109">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="bbc18-110">searchInfo</span><span class="sxs-lookup"><span data-stu-id="bbc18-110">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="bbc18-111">labelInfo</span><span class="sxs-lookup"><span data-stu-id="bbc18-111">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="bbc18-112">Requerida</span><span class="sxs-lookup"><span data-stu-id="bbc18-112">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="bbc18-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="bbc18-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="bbc18-114">stringFormat</span><span class="sxs-lookup"><span data-stu-id="bbc18-114">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="bbc18-115">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="bbc18-115">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="bbc18-116">Numérico</span><span class="sxs-lookup"><span data-stu-id="bbc18-116">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="bbc18-117">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bbc18-117">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="bbc18-118">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="bbc18-118">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="bbc18-119">drawControl</span><span class="sxs-lookup"><span data-stu-id="bbc18-119">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbc18-120">editControl</span><span class="sxs-lookup"><span data-stu-id="bbc18-120">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="bbc18-121">filterControl</span><span class="sxs-lookup"><span data-stu-id="bbc18-121">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="bbc18-122">Consulta</span><span class="sxs-lookup"><span data-stu-id="bbc18-122">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
