---
description: Identifica si el elemento está cifrado.
ms.assetid: fd93f915-6af3-4bde-982e-6774a1ca83af
title: System. IsEncrypted
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05f6f1d31838f885820938e9be38ef161c168ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648339"
---
# <a name="systemisencrypted"></a><span data-ttu-id="7e17d-103">System. IsEncrypted</span><span class="sxs-lookup"><span data-stu-id="7e17d-103">System.IsEncrypted</span></span>

<span data-ttu-id="7e17d-104">Identifica si el elemento está cifrado.</span><span class="sxs-lookup"><span data-stu-id="7e17d-104">Identifies whether the item is encrypted.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="7e17d-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="7e17d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Encrypted
            value = #TRUE#
            text = Encrypted
            defineToken = ISENCRYPTED_ENCRYPTED
         enum
            name = NotEncrypted
            value = #FALSE#
            text = Unencrypted
            defineToken = ISENCRYPTED_NOTENCRYPTED
```

## <a name="windows-vista"></a><span data-ttu-id="7e17d-106">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e17d-106">Windows Vista</span></span>

```
propertyDescription
   name = System.IsEncrypted
   shellPKey = PKEY_IsEncrypted
   formatID = 90E5E14E-648B-4826-B2AA-ACAF790E3513
   propID = 10
   SearchInfo
      IsColumn = true
   typeInfo
      type = Boolean
      EnumeratedList
         UseValueForDefault = True
         enum
            value = #TRUE#
            text = Encrypted
            mnemonics = encrypted
         enum
            value = #FALSE#
            text = Unencrypted
            mnemonics = unencrypted
```

## <a name="remarks"></a><span data-ttu-id="7e17d-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e17d-107">Remarks</span></span>

<span data-ttu-id="7e17d-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="7e17d-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="7e17d-109">Esta propiedad se presentó con la versión de Windows Search 4,0.</span><span class="sxs-lookup"><span data-stu-id="7e17d-109">This property was introduced with the release of Windows Search 4.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e17d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e17d-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e17d-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7e17d-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7e17d-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7e17d-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7e17d-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7e17d-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7e17d-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="7e17d-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7e17d-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7e17d-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7e17d-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7e17d-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7e17d-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7e17d-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7e17d-118">Numérico</span><span class="sxs-lookup"><span data-stu-id="7e17d-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7e17d-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7e17d-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7e17d-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7e17d-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7e17d-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="7e17d-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7e17d-122">editControl</span><span class="sxs-lookup"><span data-stu-id="7e17d-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7e17d-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="7e17d-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7e17d-124">Consulta</span><span class="sxs-lookup"><span data-stu-id="7e17d-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
