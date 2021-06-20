---
description: Obtenga información sobre la propiedad System.ItemFolderPathDisplayNarrow, que representa la ruta de acceso de presentación fácil de usar de la carpeta primaria de un elemento.
ms.assetid: f60b7465-bca4-4c7b-9caf-9cda1bf6eeeb
title: System.ItemFolderPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbee8a45eb6ea557e99c854464c7dc09ec5613d2
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403918"
---
# <a name="systemitemfolderpathdisplaynarrow"></a><span data-ttu-id="0e46e-103">System.ItemFolderPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="0e46e-103">System.ItemFolderPathDisplayNarrow</span></span>

<span data-ttu-id="0e46e-104">Ruta de acceso para mostrar fácil de usar de la carpeta primaria de un elemento.</span><span class="sxs-lookup"><span data-stu-id="0e46e-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="0e46e-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e46e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplayNarrow
   shellPKey = PKEY_ItemFolderPathDisplayNarrow
   formatID = DABD30ED-0043-4789-A7F8-D013A4736622
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="0e46e-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e46e-106">Remarks</span></span>

<span data-ttu-id="0e46e-107">Los valores PKEY se definen en Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="0e46e-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="0e46e-108">El formato de la cadena debe adaptarse para que el nombre de la carpeta sea el primero en optimizarse para una columna de visualización estrecha.</span><span class="sxs-lookup"><span data-stu-id="0e46e-108">The format of the string should be tailored so that the folder name comes first, to optimize for a narrow viewing column.</span></span> <span data-ttu-id="0e46e-109">Si la carpeta es una carpeta de archivos, el valor incluye los nombres localizados.</span><span class="sxs-lookup"><span data-stu-id="0e46e-109">If the folder is a file folder, the value includes any localized names.</span></span> <span data-ttu-id="0e46e-110">Si [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) es VT \_ EMPTY, esta propiedad también debe estar vacía.</span><span class="sxs-lookup"><span data-stu-id="0e46e-110">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="0e46e-111">De lo contrario, el origen de datos debe derivarlo correctamente de System.ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="0e46e-111">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0e46e-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0e46e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e46e-113">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="0e46e-113">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="0e46e-114">searchInfo</span><span class="sxs-lookup"><span data-stu-id="0e46e-114">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="0e46e-115">labelInfo</span><span class="sxs-lookup"><span data-stu-id="0e46e-115">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="0e46e-116">typeInfo</span><span class="sxs-lookup"><span data-stu-id="0e46e-116">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="0e46e-117">displayInfo</span><span class="sxs-lookup"><span data-stu-id="0e46e-117">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="0e46e-118">stringFormat</span><span class="sxs-lookup"><span data-stu-id="0e46e-118">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="0e46e-119">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="0e46e-119">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="0e46e-120">numberFormat</span><span class="sxs-lookup"><span data-stu-id="0e46e-120">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="0e46e-121">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="0e46e-121">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="0e46e-122">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="0e46e-122">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="0e46e-123">drawControl</span><span class="sxs-lookup"><span data-stu-id="0e46e-123">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e46e-124">editControl</span><span class="sxs-lookup"><span data-stu-id="0e46e-124">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="0e46e-125">filterControl</span><span class="sxs-lookup"><span data-stu-id="0e46e-125">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="0e46e-126">queryControl</span><span class="sxs-lookup"><span data-stu-id="0e46e-126">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
