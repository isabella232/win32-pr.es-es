---
description: Identifica si el elemento se ha leído.
ms.assetid: 2efa6dd9-8521-48c9-9aff-e2e8f0e2296d
title: System. IsRead
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045dda6e840ff9d800b44573c4ba8537cdd2ebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677495"
---
# <a name="systemisread"></a><span data-ttu-id="6181c-103">System. IsRead</span><span class="sxs-lookup"><span data-stu-id="6181c-103">System.IsRead</span></span>

<span data-ttu-id="6181c-104">Identifica si el elemento se ha leído.</span><span class="sxs-lookup"><span data-stu-id="6181c-104">Identifies whether the item has been read.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="6181c-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="6181c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Read
            value = #TRUE#
            text = Read
            defineToken = ISREAD_READ
         enum
            name = NotRead
            value = #FALSE#
            text = Unread
            defineToken = ISREAD_NOTREAD
```

## <a name="windows-vista"></a><span data-ttu-id="6181c-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6181c-106">Windows Vista</span></span>

```
propertyDescription
   name = System.IsRead
   shellPKey = PKEY_IsRead
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Read
            mnemonics = read
         enum
            value = #FALSE#
            text = Unread
            mnemonics = unread
```

## <a name="remarks"></a><span data-ttu-id="6181c-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6181c-107">Remarks</span></span>

<span data-ttu-id="6181c-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6181c-108">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6181c-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6181c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6181c-110">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6181c-110">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6181c-111">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6181c-111">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6181c-112">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6181c-112">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6181c-113">Requerida</span><span class="sxs-lookup"><span data-stu-id="6181c-113">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6181c-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6181c-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6181c-115">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6181c-115">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6181c-116">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6181c-116">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6181c-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="6181c-117">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6181c-118">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6181c-118">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6181c-119">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6181c-119">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6181c-120">drawControl</span><span class="sxs-lookup"><span data-stu-id="6181c-120">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6181c-121">editControl</span><span class="sxs-lookup"><span data-stu-id="6181c-121">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6181c-122">filterControl</span><span class="sxs-lookup"><span data-stu-id="6181c-122">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6181c-123">Consulta</span><span class="sxs-lookup"><span data-stu-id="6181c-123">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
