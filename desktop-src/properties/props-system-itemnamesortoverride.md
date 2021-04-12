---
description: Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System. ItemNameDisplay en configuraciones regionales CJK (pinyin de CHS, Japonés JPN, hangul KOR, etc.).
ms.assetid: eb491644-bf59-4439-9e9b-bcafde619d66
title: System. ItemNameSortOverride
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79f9bb07eb15eb5d25fbfa1e95d4c0f80b35611
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278018"
---
# <a name="systemitemnamesortoverride"></a><span data-ttu-id="6e1c4-103">System. ItemNameSortOverride</span><span class="sxs-lookup"><span data-stu-id="6e1c4-103">System.ItemNameSortOverride</span></span>

<span data-ttu-id="6e1c4-104">Esta cadena debe establecerse en la versión fonética del nombre para mostrar tal como se define en System. ItemNameDisplay en configuraciones regionales CJK (pinyin de CHS, Japonés JPN, hangul KOR, etc.).</span><span class="sxs-lookup"><span data-stu-id="6e1c4-104">This string should be set to the phonetic version of the display name as defined in System.ItemNameDisplay in CJK locales(CHS Pinyin, JPN Hiragana, KOR Hangul, etc.).</span></span> <span data-ttu-id="6e1c4-105">El primer carácter de este campo también se utiliza para agrupar los nombres por firstLetter.</span><span class="sxs-lookup"><span data-stu-id="6e1c4-105">The first character of this field is also used for grouping names by firstletter.</span></span> <span data-ttu-id="6e1c4-106">Para la mayoría de los lenguajes que no sean CJK, no es necesario establecer este campo (en cuyo caso se usará System. ItemNameDisplay). Sin embargo, si es deseable invalidar la letra de agrupación (por ejemplo, para quitar los artículos iniciales como "a" y "el"), se puede proporcionar una cadena alternativa aquí.</span><span class="sxs-lookup"><span data-stu-id="6e1c4-106">For most non-CJK languages, this field does not need to be set (in which case System.ItemNameDisplay will be used).However, if it is desirable to override the grouping letter (for example, to remove leading articles such as "a" and "the"),an alternate string can be provided here.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a><span data-ttu-id="6e1c4-107">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8</span><span class="sxs-lookup"><span data-stu-id="6e1c4-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8</span></span>

```
propertyDescription
   name = System.ItemNameSortOverride
   shellPKey = PKEY_ItemNameSortOverride
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="6e1c4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6e1c4-108">Remarks</span></span>

<span data-ttu-id="6e1c4-109">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="6e1c4-109">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e1c4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6e1c4-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e1c4-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="6e1c4-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="6e1c4-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="6e1c4-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="6e1c4-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="6e1c4-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="6e1c4-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="6e1c4-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-118">Numérico</span><span class="sxs-lookup"><span data-stu-id="6e1c4-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="6e1c4-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="6e1c4-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="6e1c4-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-122">editControl</span><span class="sxs-lookup"><span data-stu-id="6e1c4-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="6e1c4-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="6e1c4-124">Consulta</span><span class="sxs-lookup"><span data-stu-id="6e1c4-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
