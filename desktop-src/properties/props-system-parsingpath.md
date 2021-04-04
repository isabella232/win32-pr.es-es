---
description: Ruta de acceso del espacio de nombres del shell al elemento.
ms.assetid: e0fb2092-0427-40c9-9e09-aefc5ef017e6
title: System. ParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae62243ff37464617f87654f8ca1f04c3ea606da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909234"
---
# <a name="systemparsingpath"></a><span data-ttu-id="73535-103">System. ParsingPath</span><span class="sxs-lookup"><span data-stu-id="73535-103">System.ParsingPath</span></span>

<span data-ttu-id="73535-104">Ruta de acceso del espacio de nombres del shell al elemento.</span><span class="sxs-lookup"><span data-stu-id="73535-104">The Shell namespace path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="73535-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73535-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ParsingPath
   shellPKey = PKEY_ParsingPath
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 30
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="73535-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73535-106">Remarks</span></span>

<span data-ttu-id="73535-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="73535-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="73535-108">Este valor se puede pasar a [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) para analizar la ruta de acceso a la carpeta de Shell correcta.</span><span class="sxs-lookup"><span data-stu-id="73535-108">This value can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="73535-109">Si el elemento es un archivo, el valor es idéntico a [System. ItemPathDisplay](./props-system-itempathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="73535-109">If the item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).</span></span> <span data-ttu-id="73535-110">Si no se puede tener acceso al elemento a través del espacio de nombres del shell, este valor es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="73535-110">If the item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="73535-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73535-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73535-112">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="73535-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="73535-113">searchInfo</span><span class="sxs-lookup"><span data-stu-id="73535-113">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="73535-114">labelInfo</span><span class="sxs-lookup"><span data-stu-id="73535-114">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="73535-115">Requerida</span><span class="sxs-lookup"><span data-stu-id="73535-115">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="73535-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="73535-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="73535-117">stringFormat</span><span class="sxs-lookup"><span data-stu-id="73535-117">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="73535-118">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="73535-118">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="73535-119">Numérico</span><span class="sxs-lookup"><span data-stu-id="73535-119">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="73535-120">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="73535-120">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="73535-121">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="73535-121">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="73535-122">drawControl</span><span class="sxs-lookup"><span data-stu-id="73535-122">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="73535-123">editControl</span><span class="sxs-lookup"><span data-stu-id="73535-123">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="73535-124">filterControl</span><span class="sxs-lookup"><span data-stu-id="73535-124">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="73535-125">Consulta</span><span class="sxs-lookup"><span data-stu-id="73535-125">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
