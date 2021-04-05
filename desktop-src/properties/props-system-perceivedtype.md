---
description: El tipo de archivo percibido basado en su tipo canónico.
ms.assetid: dc5122a1-43b3-4c91-a44f-315fec5b4862
title: System.PerceivedType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fc0be5e2ba481d113981efc264c4da66428e675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001794"
---
# <a name="systemperceivedtype"></a><span data-ttu-id="a0177-103">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="a0177-103">System.PerceivedType</span></span>

<span data-ttu-id="a0177-104">El tipo de archivo percibido basado en su tipo canónico.</span><span class="sxs-lookup"><span data-stu-id="a0177-104">The perceived file type based on its canonical type.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="a0177-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0177-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Custom
            value = -3
            text = Custom
         enum
            name = Unspecified
            value = -2
            text = Unspecified
         enum
            name = Folder
            value = -1
            text = Folder
            mnemonics = folders
         enum
            name = Unknown
            value = 0
            text = Unknown
         enum
            name = Text
            value = 1
            text = Text
         enum
            name = Image
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            name = Audio
            value = 3
            text = Audio
         enum
            name = Video
            value = 4
            text = Video
            mnemonics = videos
         enum
            name = Compressed
            value = 5
            text = Compressed
         enum
            name = Document
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            name = System
            value = 7
            text = System
         enum
            name = Application
            value = 8
            text = Application
         enum
            name = GameMedia
            value = 9
            text = Game Media
         enum
            name = Contacts
            value = 10
            text = Contacts
```

## <a name="windows-vista"></a><span data-ttu-id="a0177-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0177-106">Windows Vista</span></span>

```
propertyDescription
   name = System.PerceivedType
   shellPKey = PKEY_PerceivedType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 9
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Int32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = -3
            text = Custom
         enum
            value = -2
            text = Unspecified
         enum
            value = -1
            text = Folder
            mnemonics = folders
         enum
            value = 0
            text = Unknown
         enum
            value = 1
            text = Text
         enum
            value = 2
            text = Image
            mnemonics = images|picture|pictures|pic|pics
         enum
            value = 3
            text = Audio
         enum
            value = 4
            text = Video
            mnemonics = videos
         enum
            value = 5
            text = Compressed
         enum
            value = 6
            text = Document
            mnemonics = documents|doc|docs
         enum
            value = 7
            text = System
         enum
            value = 8
            text = Application
         enum
            value = 9
            text = Game Media
         enum
            value = 10
            text = Contacts
```

## <a name="remarks"></a><span data-ttu-id="a0177-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0177-107">Remarks</span></span>

<span data-ttu-id="a0177-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="a0177-108">PKEY values are defined in Propkey.h.</span></span> <span data-ttu-id="a0177-109">El shell asigna automáticamente este valor.</span><span class="sxs-lookup"><span data-stu-id="a0177-109">This value is automatically assigned by the Shell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a0177-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0177-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0177-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="a0177-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="a0177-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="a0177-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="a0177-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="a0177-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="a0177-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="a0177-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="a0177-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="a0177-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="a0177-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="a0177-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="a0177-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="a0177-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="a0177-118">Numérico</span><span class="sxs-lookup"><span data-stu-id="a0177-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="a0177-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a0177-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="a0177-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="a0177-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="a0177-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="a0177-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0177-122">editControl</span><span class="sxs-lookup"><span data-stu-id="a0177-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="a0177-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="a0177-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="a0177-124">Consulta</span><span class="sxs-lookup"><span data-stu-id="a0177-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
