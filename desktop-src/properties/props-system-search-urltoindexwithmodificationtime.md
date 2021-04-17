---
description: Esta propiedad es igual que System. Search. UrlToIndex, salvo que incluye la hora en que se modificó por última vez la dirección URL.
ms.assetid: 53ca765b-0795-49ab-9946-c3ef101ababd
title: System. Search. UrlToIndexWithModificationTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fcc83b9796ae2375f10235a08ba0db313fb1958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716730"
---
# <a name="systemsearchurltoindexwithmodificationtime"></a><span data-ttu-id="32926-103">System. Search. UrlToIndexWithModificationTime</span><span class="sxs-lookup"><span data-stu-id="32926-103">System.Search.UrlToIndexWithModificationTime</span></span>

<span data-ttu-id="32926-104">Esta propiedad es igual que [**System. Search. UrlToIndex**](props-system-search-urltoindex.md) , salvo que incluye la hora en que se modificó por última vez la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="32926-104">This property is the same as [**System.Search.UrlToIndex**](props-system-search-urltoindex.md) except that it includes the time that the URL was last modified.</span></span> <span data-ttu-id="32926-105">Se trata de una optimización para el indizador, de modo que no tenga que volver a llamar al controlador de protocolo para solicitar esta información para determinar si es necesario indizar el contenido de nuevo.</span><span class="sxs-lookup"><span data-stu-id="32926-105">This is an optimization for the indexer so that it does not have to call back into the protocol handler to ask for this information to determine whether the content needs to be indexed again.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="32926-106">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32926-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Search.UrlToIndexWithModificationTime
   shellPKey = PKEY_Search_UrlToIndexWithModificationTime
   formatID = 0B63E343-9CCC-11D0-BCDB-00805FCCCE04
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = Multivalue Any
```

## <a name="remarks"></a><span data-ttu-id="32926-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="32926-107">Remarks</span></span>

<span data-ttu-id="32926-108">Esta propiedad [System. Search. UrlToIndexWithModificationTime]() es la misma que la propiedad [System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) , salvo que también se pasa la hora de la última modificación del documento.</span><span class="sxs-lookup"><span data-stu-id="32926-108">This [System.Search.UrlToIndexWithModificationTime]() property is the same as the [System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)) property, except that you also pass in the last modified time of the document.</span></span> <span data-ttu-id="32926-109">Si la hora de la última modificación coincide, el indexador supone que el documento ya está indexado y que sale de la notificación.</span><span class="sxs-lookup"><span data-stu-id="32926-109">If the last modified time matches, the indexer assumes that the document is already indexed and throws away the notification.</span></span> <span data-ttu-id="32926-110">Esta propiedad es un vector con dos elementos, un valor de **VT \_ LPWStr** que contiene la dirección URL y un valor **\_ FILETIME de VT** que contiene la hora de la última modificación.</span><span class="sxs-lookup"><span data-stu-id="32926-110">This property is a vector with two elements, a **VT\_LPWSTR** value that contains the URL and a **VT\_FILETIME** value that contains the last modified time.</span></span>

<span data-ttu-id="32926-111">[System. Search. UrlToIndexWithModificationTime]() se llamaba PID \_ GTHR \_ DIRLINK \_ con \_ hora en versiones anteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="32926-111">[System.Search.UrlToIndexWithModificationTime]() was called PID\_GTHR\_DIRLINK\_WITH\_TIME in earlier versions of the Windows operating system.</span></span>

<span data-ttu-id="32926-112">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="32926-112">PKEY values are defined in Propkey.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32926-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="32926-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="32926-114">[System. Search. UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="32926-114">[System.Search.UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="32926-115">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="32926-115">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="32926-116">searchInfo</span><span class="sxs-lookup"><span data-stu-id="32926-116">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="32926-117">labelInfo</span><span class="sxs-lookup"><span data-stu-id="32926-117">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="32926-118">Requerida</span><span class="sxs-lookup"><span data-stu-id="32926-118">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="32926-119">displayInfo</span><span class="sxs-lookup"><span data-stu-id="32926-119">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="32926-120">stringFormat</span><span class="sxs-lookup"><span data-stu-id="32926-120">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="32926-121">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="32926-121">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="32926-122">Numérico</span><span class="sxs-lookup"><span data-stu-id="32926-122">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="32926-123">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="32926-123">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="32926-124">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="32926-124">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="32926-125">drawControl</span><span class="sxs-lookup"><span data-stu-id="32926-125">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="32926-126">editControl</span><span class="sxs-lookup"><span data-stu-id="32926-126">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="32926-127">filterControl</span><span class="sxs-lookup"><span data-stu-id="32926-127">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="32926-128">Consulta</span><span class="sxs-lookup"><span data-stu-id="32926-128">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
