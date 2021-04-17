---
description: Identifica la extensión de archivo del elemento basado en archivo, incluido el punto inicial.
ms.assetid: b72c695e-bdbd-471d-b902-9e30a62facd4
title: System. FileExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf8792a3965c394a1944985515df527e41e3a159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659881"
---
# <a name="systemfileextension"></a><span data-ttu-id="577c2-103">System. FileExtension</span><span class="sxs-lookup"><span data-stu-id="577c2-103">System.FileExtension</span></span>

<span data-ttu-id="577c2-104">Identifica la extensión de archivo del elemento basado en archivo, incluido el punto inicial.</span><span class="sxs-lookup"><span data-stu-id="577c2-104">Identifies the file extension of the file-based item, including the leading period.</span></span> <span data-ttu-id="577c2-105">Esta propiedad se deriva de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="577c2-105">This property is derived from System.FileName.</span></span> <span data-ttu-id="577c2-106">Si System. FileName no tiene una extensión de archivo o es VT \_ vacío, el valor de esta propiedad debe ser VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="577c2-106">If System.FileName either does not have a file extension or is VT\_EMPTY, the value for this property should be VT\_EMPTY.</span></span>

<span data-ttu-id="577c2-107">Para obtener el tipo de cualquier elemento (incluido un elemento que no es un archivo), use System. ItemType.</span><span class="sxs-lookup"><span data-stu-id="577c2-107">To obtain the type of any item (including an item that is not a file), use System.ItemType.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="577c2-108">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="577c2-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.FileExtension
   shellPKey = PKEY_FileExtension
   formatID = E4F10A3C-49E6-405D-8288-A23BD4EEAA6C
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="577c2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="577c2-109">Remarks</span></span>

<span data-ttu-id="577c2-110">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="577c2-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="577c2-111">Si [System. FileName](./props-system-filename.md) es VT \_ vacío, esta propiedad también debe estar vacía.</span><span class="sxs-lookup"><span data-stu-id="577c2-111">If [System.FileName](./props-system-filename.md) is VT\_EMPTY, this property should also be empty.</span></span> <span data-ttu-id="577c2-112">De lo contrario, esta propiedad debe derivarse apropiadamente por el origen de datos de System. FileName.</span><span class="sxs-lookup"><span data-stu-id="577c2-112">Otherwise, this property should be derived appropriately by the data source from System.FileName.</span></span> <span data-ttu-id="577c2-113">Si System. FileName no incluye una extensión de archivo, [System. FileExtension]() debe ser VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="577c2-113">If System.FileName does not include a file extension, [System.FileExtension]() should be VT\_EMPTY.</span></span> <span data-ttu-id="577c2-114">Para obtener el tipo de cualquier elemento (incluido un elemento que no es un archivo), use [System. ItemType](./props-system-itemtype.md).</span><span class="sxs-lookup"><span data-stu-id="577c2-114">To obtain the type of any item (including an item that is not a file), use [System.ItemType](./props-system-itemtype.md).</span></span>

<span data-ttu-id="577c2-115">Ejemplos de propiedades de extensión de archivo y ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="577c2-115">Path and file extension property examples.</span></span> 

| <span data-ttu-id="577c2-116">Ruta</span><span class="sxs-lookup"><span data-stu-id="577c2-116">Path</span></span>                               | <span data-ttu-id="577c2-117">Extensión de archivo</span><span class="sxs-lookup"><span data-stu-id="577c2-117">File Extension</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="577c2-118">c: \\ archivos \\ personales \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="577c2-118">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="577c2-119">.txt</span><span class="sxs-lookup"><span data-stu-id="577c2-119">.txt</span></span>           |
| <span data-ttu-id="577c2-120">\\\\\\news.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="577c2-120">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="577c2-121">.doc</span><span class="sxs-lookup"><span data-stu-id="577c2-121">.doc</span></span>           |
| <span data-ttu-id="577c2-122">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="577c2-122">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="577c2-123">.xls</span><span class="sxs-lookup"><span data-stu-id="577c2-123">.xls</span></span>           |
| <span data-ttu-id="577c2-124">\\\\\\carpeta de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="577c2-124">\\\\server\\share\\folder</span></span>          | <span data-ttu-id="577c2-125">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="577c2-125">VT\_EMPTY</span></span>      |
| <span data-ttu-id="577c2-126">c: \\ mis \\ carpetas</span><span class="sxs-lookup"><span data-stu-id="577c2-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="577c2-127">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="577c2-127">VT\_EMPTY</span></span>      |
| <span data-ttu-id="577c2-128">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="577c2-128">\[desktop\]</span></span>                        | <span data-ttu-id="577c2-129">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="577c2-129">VT\_EMPTY</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="577c2-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="577c2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="577c2-131">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="577c2-131">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="577c2-132">searchInfo</span><span class="sxs-lookup"><span data-stu-id="577c2-132">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="577c2-133">labelInfo</span><span class="sxs-lookup"><span data-stu-id="577c2-133">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="577c2-134">Requerida</span><span class="sxs-lookup"><span data-stu-id="577c2-134">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="577c2-135">displayInfo</span><span class="sxs-lookup"><span data-stu-id="577c2-135">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="577c2-136">stringFormat</span><span class="sxs-lookup"><span data-stu-id="577c2-136">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="577c2-137">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="577c2-137">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="577c2-138">Numérico</span><span class="sxs-lookup"><span data-stu-id="577c2-138">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="577c2-139">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="577c2-139">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="577c2-140">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="577c2-140">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="577c2-141">drawControl</span><span class="sxs-lookup"><span data-stu-id="577c2-141">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="577c2-142">editControl</span><span class="sxs-lookup"><span data-stu-id="577c2-142">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="577c2-143">filterControl</span><span class="sxs-lookup"><span data-stu-id="577c2-143">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="577c2-144">Consulta</span><span class="sxs-lookup"><span data-stu-id="577c2-144">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
