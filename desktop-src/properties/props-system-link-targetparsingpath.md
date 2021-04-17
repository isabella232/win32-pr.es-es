---
description: Ruta de acceso del espacio de nombres del shell al destino del elemento de vínculo.
ms.assetid: 05bd6cae-68b2-49ce-ad4f-e395ec88407a
title: System. Link. TargetParsingPath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1414947b988422c0ff37afda4bd55c80ffc9832
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715969"
---
# <a name="systemlinktargetparsingpath"></a><span data-ttu-id="01c43-103">System. Link. TargetParsingPath</span><span class="sxs-lookup"><span data-stu-id="01c43-103">System.Link.TargetParsingPath</span></span>

<span data-ttu-id="01c43-104">Ruta de acceso del espacio de nombres del shell al destino del elemento de vínculo.</span><span class="sxs-lookup"><span data-stu-id="01c43-104">The Shell namespace path to the target of the link item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="01c43-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01c43-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.Link.TargetParsingPath
   shellPKey = PKEY_Link_TargetParsingPath
   formatID = B9B4B3FC-2B51-4A42-B5D8-324146AFCF25
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="01c43-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01c43-106">Remarks</span></span>

<span data-ttu-id="01c43-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="01c43-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="01c43-108">Esta ruta de acceso se puede pasar a [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) para analizar la ruta de acceso a la carpeta de Shell correcta.</span><span class="sxs-lookup"><span data-stu-id="01c43-108">This path can be passed to [**SHParseDisplayName**](/windows/win32/api/shlobj_core/nf-shlobj_core-shparsedisplayname) to parse the path to the correct Shell folder.</span></span> <span data-ttu-id="01c43-109">Si el elemento de destino es un archivo, el valor es idéntico a [System. ItemPathDisplay](./props-system-itempathdisplay.md). Si no se puede tener acceso al elemento de destino a través del espacio de nombres del shell, este valor es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="01c43-109">If the target item is a file, the value is identical to [System.ItemPathDisplay](./props-system-itempathdisplay.md).If the target item cannot be accessed through the Shell namespace, this value is VT\_EMPTY.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01c43-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01c43-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01c43-111">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="01c43-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="01c43-112">searchInfo</span><span class="sxs-lookup"><span data-stu-id="01c43-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="01c43-113">labelInfo</span><span class="sxs-lookup"><span data-stu-id="01c43-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="01c43-114">Requerida</span><span class="sxs-lookup"><span data-stu-id="01c43-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="01c43-115">displayInfo</span><span class="sxs-lookup"><span data-stu-id="01c43-115">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="01c43-116">stringFormat</span><span class="sxs-lookup"><span data-stu-id="01c43-116">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="01c43-117">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="01c43-117">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="01c43-118">Numérico</span><span class="sxs-lookup"><span data-stu-id="01c43-118">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="01c43-119">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="01c43-119">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="01c43-120">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="01c43-120">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="01c43-121">drawControl</span><span class="sxs-lookup"><span data-stu-id="01c43-121">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="01c43-122">editControl</span><span class="sxs-lookup"><span data-stu-id="01c43-122">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="01c43-123">filterControl</span><span class="sxs-lookup"><span data-stu-id="01c43-123">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="01c43-124">Consulta</span><span class="sxs-lookup"><span data-stu-id="01c43-124">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
