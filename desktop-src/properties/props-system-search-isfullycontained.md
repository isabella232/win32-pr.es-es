---
description: Lo emiten todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con la extensión de nombre. zip) que emite System. Search. IsClosedDirectory como TRUE. Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.
ms.assetid: 6da60e89-6956-41f6-8624-063c4d46464d
title: System. Search. IsFullyContained
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1245f29a2940146a4e5d8f0a392210173be75e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546758"
---
# <a name="systemsearchisfullycontained"></a><span data-ttu-id="c62a2-104">System. Search. IsFullyContained</span><span class="sxs-lookup"><span data-stu-id="c62a2-104">System.Search.IsFullyContained</span></span>

<span data-ttu-id="c62a2-105">**Lo** emiten todos los elementos secundarios de un contenedor (por ejemplo, un correo electrónico o un archivo comprimido con la extensión de nombre. zip) que emite [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="c62a2-105">Emitted as **TRUE** by all child items of a container (such as an e-mail or a compressed file with a .zip name extension) that emits [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) as **TRUE**.</span></span> <span data-ttu-id="c62a2-106">Esto garantiza que los elementos secundarios se incluyen en el índice de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="c62a2-106">This ensures that the child items are included in the search index.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="c62a2-107">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c62a2-107">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsFullyContained
   shellPKey = PKEY_Search_IsFullyContained
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 24
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="c62a2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c62a2-108">Remarks</span></span>

<span data-ttu-id="c62a2-109">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="c62a2-109">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="c62a2-110">La propiedad [System. Search. IsClosedDirectory](./props-system-search-iscloseddirectory.md) ayuda a optimizar el rendimiento del indexador permitiendo al indizador omitir la enumeración de los elementos secundarios de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="c62a2-110">The [System.Search.IsClosedDirectory](./props-system-search-iscloseddirectory.md) property helps to optimize indexer performance by allowing the indexer to skip the enumeration of a container's child items.</span></span> <span data-ttu-id="c62a2-111">Sin embargo, los elementos secundarios están marcados por el indexador como no visitados y, como tal, se eliminarán del índice.</span><span class="sxs-lookup"><span data-stu-id="c62a2-111">However, those child items are marked by the indexer as not visited, and as such will be deleted from the index.</span></span> <span data-ttu-id="c62a2-112">Al emitir [System. Search. IsFullyContained]() como **true**, no se elimina un elemento del índice a pesar de que no se ha visitado.</span><span class="sxs-lookup"><span data-stu-id="c62a2-112">By emitting [System.Search.IsFullyContained]() as **TRUE**, an item is not deleted from the index despite having not been visited.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c62a2-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c62a2-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c62a2-114">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="c62a2-114">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="c62a2-115">searchInfo</span><span class="sxs-lookup"><span data-stu-id="c62a2-115">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="c62a2-116">labelInfo</span><span class="sxs-lookup"><span data-stu-id="c62a2-116">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="c62a2-117">Requerida</span><span class="sxs-lookup"><span data-stu-id="c62a2-117">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="c62a2-118">displayInfo</span><span class="sxs-lookup"><span data-stu-id="c62a2-118">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="c62a2-119">stringFormat</span><span class="sxs-lookup"><span data-stu-id="c62a2-119">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="c62a2-120">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="c62a2-120">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="c62a2-121">Numérico</span><span class="sxs-lookup"><span data-stu-id="c62a2-121">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="c62a2-122">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="c62a2-122">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="c62a2-123">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="c62a2-123">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="c62a2-124">drawControl</span><span class="sxs-lookup"><span data-stu-id="c62a2-124">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="c62a2-125">editControl</span><span class="sxs-lookup"><span data-stu-id="c62a2-125">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="c62a2-126">filterControl</span><span class="sxs-lookup"><span data-stu-id="c62a2-126">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="c62a2-127">Consulta</span><span class="sxs-lookup"><span data-stu-id="c62a2-127">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
