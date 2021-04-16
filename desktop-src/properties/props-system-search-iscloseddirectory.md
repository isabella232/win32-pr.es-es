---
description: Un elemento contenedor emite como TRUE para indicar que no es necesario que un indexador Enumere sus elementos secundarios si el elemento contenedor no ha cambiado desde el último rastreo de comprobación de Índice incremental.
ms.assetid: 8bb487b9-4a51-4a6b-939e-946a8aad85de
title: System. Search. IsClosedDirectory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea97aeb8d0192eea7d71ca65fd0ec109780702f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720684"
---
# <a name="systemsearchiscloseddirectory"></a><span data-ttu-id="7c98c-103">System. Search. IsClosedDirectory</span><span class="sxs-lookup"><span data-stu-id="7c98c-103">System.Search.IsClosedDirectory</span></span>

<span data-ttu-id="7c98c-104">Un elemento contenedor emite como **true** para indicar que no es necesario que un indexador Enumere sus elementos secundarios si el elemento contenedor no ha cambiado desde el último rastreo de comprobación de Índice incremental.</span><span class="sxs-lookup"><span data-stu-id="7c98c-104">Emitted as **TRUE** by a container item to indicate that its child items do not need to be enumerated by an indexer if the container item has not changed since the last incremental index verification crawl.</span></span> <span data-ttu-id="7c98c-105">Esto contribuye a la optimización del rendimiento del indexador.</span><span class="sxs-lookup"><span data-stu-id="7c98c-105">This contributes to the optimization of indexer performance.</span></span> <span data-ttu-id="7c98c-106">En estos casos de contenedor (los ejemplos son un correo electrónico con datos adjuntos o un archivo comprimido con la extensión. zip), los elementos secundarios son inseparables de su elemento primario.</span><span class="sxs-lookup"><span data-stu-id="7c98c-106">In these container cases (examples are an e-mail with attachments or a compressed file with a .zip name extension), child items are inseparable from their parent item.</span></span> <span data-ttu-id="7c98c-107">Por ejemplo, si la propiedad [System. DateModified](./props-system-datemodified.md) de un elemento contenido cambia, el valor System. DateModified del contenedor cambia para coincidir.</span><span class="sxs-lookup"><span data-stu-id="7c98c-107">For instance, if the [System.DateModified](./props-system-datemodified.md) property of a contained item changes, then the System.DateModified value of the container changes to match.</span></span> <span data-ttu-id="7c98c-108">Además, si se elimina un elemento primario, se eliminan también todos los elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="7c98c-108">Also, if a parent item is deleted, all of the child items are deleted as well.</span></span> <span data-ttu-id="7c98c-109">Por lo tanto, si el contenedor no ha cambiado, el indizador sabe que no ha cambiado nada y no necesita abrir el contenedor para examinar el contenido de forma individual.</span><span class="sxs-lookup"><span data-stu-id="7c98c-109">Therefore, if the container has not changed, the indexer knows that nothing within it has changed and does not need to open the container to examine the contents individually.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="7c98c-110">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c98c-110">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.IsClosedDirectory
   shellPKey = PKEY_Search_IsClosedDirectory
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 23
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Boolean
```

## <a name="remarks"></a><span data-ttu-id="7c98c-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c98c-111">Remarks</span></span>

<span data-ttu-id="7c98c-112">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="7c98c-112">PKEY values are defined in Propkey.h.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7c98c-113">Si un elemento emite **true** para esta propiedad, cada uno de sus elementos secundarios debe emitir la propiedad [System. Search. IsFullyContained](./props-system-search-isfullycontained.md) como **true** para evitar que estos elementos se eliminen del índice.</span><span class="sxs-lookup"><span data-stu-id="7c98c-113">If an item emits **TRUE** for this property, each of its child items must emit the [System.Search.IsFullyContained](./props-system-search-isfullycontained.md) property as **TRUE** to prevent those items from being deleted from the index.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="7c98c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c98c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c98c-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7c98c-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7c98c-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7c98c-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7c98c-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7c98c-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7c98c-118">Requerida</span><span class="sxs-lookup"><span data-stu-id="7c98c-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7c98c-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7c98c-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7c98c-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7c98c-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7c98c-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7c98c-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7c98c-122">Numérico</span><span class="sxs-lookup"><span data-stu-id="7c98c-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7c98c-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7c98c-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7c98c-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7c98c-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7c98c-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="7c98c-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c98c-126">editControl</span><span class="sxs-lookup"><span data-stu-id="7c98c-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c98c-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="7c98c-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7c98c-128">Consulta</span><span class="sxs-lookup"><span data-stu-id="7c98c-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
