---
description: El nombre de archivo, incluida su extensión.
ms.assetid: 40940026-6c67-4196-aff6-5f846dc94f27
title: System. FileName
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f535eff4625178b3c32a04ea6d325505266a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687408"
---
# <a name="systemfilename"></a><span data-ttu-id="f3c07-103">System. FileName</span><span class="sxs-lookup"><span data-stu-id="f3c07-103">System.FileName</span></span>

<span data-ttu-id="f3c07-104">El nombre de archivo, incluida su extensión.</span><span class="sxs-lookup"><span data-stu-id="f3c07-104">The file name, including its extension.</span></span> <span data-ttu-id="f3c07-105">System. FileExtension se deriva de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3c07-105">System.FileExtension is derived from this property.</span></span>

<span data-ttu-id="f3c07-106">Es posible que el elemento no exista en un sistema de archivos (es decir, que no se pueda abrir con CreateFile).</span><span class="sxs-lookup"><span data-stu-id="f3c07-106">It is possible that the item might not exist on a filesystem (that is, it may not be opened using CreateFile).</span></span> <span data-ttu-id="f3c07-107">No obstante, si el elemento se representa como un archivo y su nombre sigue la sintaxis estándar de nombres de archivo de Win32, el origen de datos debe emitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3c07-107">Nonetheless, if the item is represented as a file and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="f3c07-108">Si el elemento no es un archivo, el origen de datos debe emitir esta propiedad como VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="f3c07-108">If the item is not a file, then the data source should emit this property as VT\_EMPTY.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a><span data-ttu-id="f3c07-109">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3c07-109">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="windows-vista"></a><span data-ttu-id="f3c07-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3c07-110">Windows Vista</span></span>

```
propertyDescription
   name = System.FileName
   shellPKey = PKEY_FileName
   formatID = 41CF5AE0-F75A-4806-BD87-59C7D9248EB9
   propID = 100
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enumRange
            minValue = 0
            setValue = 0
            text = 0-9
         enumRange
            minValue = A
            setValue = A
            text = A-H
         enumRange
            minValue = I
            setValue = I
            text = I-P
         enumRange
            minValue = Q
            setValue = Q
            text = Q-Z
```

## <a name="remarks"></a><span data-ttu-id="f3c07-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3c07-111">Remarks</span></span>

<span data-ttu-id="f3c07-112">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="f3c07-112">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="f3c07-113">Es posible que el elemento no exista en un sistema de archivos (es decir, que no se pueda abrir con CreateFile), pero si el elemento se representa como un archivo desde el sentido lógico y su nombre sigue la sintaxis estándar de nombres de archivo de Win32, el origen de datos debe emitir esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f3c07-113">The item might not exist on a filesystem (that is, it may not be opened using CreateFile), but if the item is represented as a file from the logical sense and its name follows standard Win32 file-naming syntax, then the data source should emit this property.</span></span> <span data-ttu-id="f3c07-114">Si un elemento no es un archivo, el valor de esta propiedad es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="f3c07-114">If an item is not a file, then the value for this property is VT\_EMPTY.</span></span> <span data-ttu-id="f3c07-115">Vea System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="f3c07-115">See System.ItemNameDisplay.</span></span> <span data-ttu-id="f3c07-116">Tiene el mismo valor que System. ParsingName para los elementos que proporciona la carpeta de archivos del shell.</span><span class="sxs-lookup"><span data-stu-id="f3c07-116">This has the same value as System.ParsingName for items that are provided by the Shell's file folder.</span></span>

<span data-ttu-id="f3c07-117">En la tabla siguiente se muestran ejemplos de valores de propiedad path y FILENAME:</span><span class="sxs-lookup"><span data-stu-id="f3c07-117">The following table lists examples of path and filename property values:</span></span>



| <span data-ttu-id="f3c07-118">Ruta</span><span class="sxs-lookup"><span data-stu-id="f3c07-118">Path</span></span>                               | <span data-ttu-id="f3c07-119">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f3c07-119">Property Value</span></span> |
|------------------------------------|----------------|
| <span data-ttu-id="f3c07-120">c: \\ archivos \\ personales \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="f3c07-120">c:\\files\\personal\\hello.txt</span></span>     | <span data-ttu-id="f3c07-121">hello.txt</span><span class="sxs-lookup"><span data-stu-id="f3c07-121">hello.txt</span></span>      |
| <span data-ttu-id="f3c07-122">\\\\\\news.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="f3c07-122">\\\\server\\share\\mydir\\news.doc</span></span> | <span data-ttu-id="f3c07-123">news.doc</span><span class="sxs-lookup"><span data-stu-id="f3c07-123">news.doc</span></span>       |
| <span data-ttu-id="f3c07-124">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="f3c07-124">\\\\server\\share\\numbers.xls</span></span>     | <span data-ttu-id="f3c07-125">numbers.xls</span><span class="sxs-lookup"><span data-stu-id="f3c07-125">numbers.xls</span></span>    |
| <span data-ttu-id="f3c07-126">c: \\ mis \\ carpetas</span><span class="sxs-lookup"><span data-stu-id="f3c07-126">c:\\Stuff\\MyFolder</span></span>                | <span data-ttu-id="f3c07-127">MyFolder</span><span class="sxs-lookup"><span data-stu-id="f3c07-127">MyFolder</span></span>       |
| <span data-ttu-id="f3c07-128">\[mensaje de correo electrónico\]</span><span class="sxs-lookup"><span data-stu-id="f3c07-128">\[email message\]</span></span>                  | <span data-ttu-id="f3c07-129">VT \_ vacío</span><span class="sxs-lookup"><span data-stu-id="f3c07-129">VT\_EMPTY</span></span>      |
| <span data-ttu-id="f3c07-130">\[Song. WMA en dispositivo portátil\]</span><span class="sxs-lookup"><span data-stu-id="f3c07-130">\[song.wma on portable device\]</span></span>    | <span data-ttu-id="f3c07-131">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="f3c07-131">song.wma</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="f3c07-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3c07-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3c07-133">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="f3c07-133">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="f3c07-134">searchInfo</span><span class="sxs-lookup"><span data-stu-id="f3c07-134">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="f3c07-135">labelInfo</span><span class="sxs-lookup"><span data-stu-id="f3c07-135">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="f3c07-136">Requerida</span><span class="sxs-lookup"><span data-stu-id="f3c07-136">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="f3c07-137">displayInfo</span><span class="sxs-lookup"><span data-stu-id="f3c07-137">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="f3c07-138">stringFormat</span><span class="sxs-lookup"><span data-stu-id="f3c07-138">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="f3c07-139">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="f3c07-139">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="f3c07-140">Numérico</span><span class="sxs-lookup"><span data-stu-id="f3c07-140">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="f3c07-141">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="f3c07-141">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="f3c07-142">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="f3c07-142">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="f3c07-143">drawControl</span><span class="sxs-lookup"><span data-stu-id="f3c07-143">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="f3c07-144">editControl</span><span class="sxs-lookup"><span data-stu-id="f3c07-144">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="f3c07-145">filterControl</span><span class="sxs-lookup"><span data-stu-id="f3c07-145">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="f3c07-146">Consulta</span><span class="sxs-lookup"><span data-stu-id="f3c07-146">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
