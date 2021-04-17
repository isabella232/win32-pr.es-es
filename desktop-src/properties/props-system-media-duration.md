---
description: Representa la hora real de reproducción de un archivo multimedia y se mide en unidades de 100 NS, no en milisegundos.
ms.assetid: 5548f421-6475-4419-b677-5d9eb625a373
title: System. Media. Duration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d14b461363346dd6214bc4e5a458995cda22bc3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105721335"
---
# <a name="systemmediaduration"></a><span data-ttu-id="2f778-103">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="2f778-103">System.Media.Duration</span></span>

<span data-ttu-id="2f778-104">Representa la hora real de reproducción de un archivo multimedia y se mide en unidades de 100 NS, no en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="2f778-104">Represents the actual play time of a media file and is measured in 100ns units, not milliseconds.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="2f778-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f778-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.Media.Duration
   shellPKey = PKEY_Media_Duration
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            name = VeryShort
            minValue = 0
            setValue = 0
            text = Very Short (under 1 min)
            defineToken = MEDIA_DURATION_VERYSHORT
            mnemonics = Very Short
         enumRange
            name = Short
            minValue = 600000000
            setValue = 600000000
            text = Short (1 - 5 mins)
            defineToken = MEDIA_DURATION_SHORT
            mnemonics = Short
         enumRange
            name = Medium
            minValue = 3000000000
            setValue = 3000000000
            text = Medium (5 - 30 mins)
            defineToken = MEDIA_DURATION_MEDIUM
            mnemonics = Medium
         enumRange
            name = Long
            minValue = 18000000000
            setValue = 18000000000
            text = Long (30 - 60 mins)
            defineToken = MEDIA_DURATION_LONG
            mnemonics = Long
         enumRange
            name = VeryLong
            minValue = 36000000000
            setValue = 36000000000
            text = Very Long (over 60 mins)
            defineToken = MEDIA_DURATION_VERYLONG
            mnemonics = Very Long
```

## <a name="windows-vista"></a><span data-ttu-id="2f778-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f778-106">Windows Vista</span></span>

```
propertyDescription
   name = System.Media.Duration
   shellPKey = PKEY_Media_Duration
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 3
   SearchInfo
      IsColumn = true
   typeInfo
      type = UInt64
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = Very Short (under 1 min)
         enumRange
            minValue = 600000000
            setValue = 600000000
            text = Short (1 - 5 mins)
         enumRange
            minValue = 3000000000
            setValue = 3000000000
            text = Medium (5 - 30 mins
         enumRange
            minValue = 18000000000
            setValue = 18000000000
            text = Long (30 - 60 mins)
         enumRange
            minValue = 36000000000
            setValue = 36000000000
            text = Very Long (over 60 mins)
```

## <a name="remarks"></a><span data-ttu-id="2f778-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f778-107">Remarks</span></span>

<span data-ttu-id="2f778-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="2f778-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f778-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2f778-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f778-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2f778-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2f778-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2f778-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2f778-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2f778-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2f778-113">Requerida</span><span class="sxs-lookup"><span data-stu-id="2f778-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2f778-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2f778-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2f778-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2f778-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2f778-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2f778-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2f778-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="2f778-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2f778-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2f778-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2f778-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2f778-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2f778-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="2f778-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2f778-121">editControl</span><span class="sxs-lookup"><span data-stu-id="2f778-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2f778-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="2f778-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2f778-123">Consulta</span><span class="sxs-lookup"><span data-stu-id="2f778-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
