---
description: Nombre de tipo descriptivo del elemento.
ms.assetid: 5d4c86da-6317-4a34-88d6-caf794aaa165
title: System. ItemTypeText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699a953392054cb2344c5f3b3d652e64a9a2c1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276585"
---
# <a name="systemitemtypetext"></a><span data-ttu-id="1a3c8-103">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="1a3c8-103">System.ItemTypeText</span></span>

<span data-ttu-id="1a3c8-104">Nombre de tipo descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-104">The user-friendly type name of the item.</span></span> <span data-ttu-id="1a3c8-105">Este valor no se ha diseñado para analizarse mediante programación.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-105">This value is not intended to be programmatically parsed.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="1a3c8-106">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a3c8-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemTypeText
   shellPKey = PKEY_ItemTypeText
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 4
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="1a3c8-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a3c8-107">Remarks</span></span>

<span data-ttu-id="1a3c8-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="1a3c8-109">Si [System. ItemType](./props-system-itemtype.md) es VT \_ vacío, el valor de esta propiedad también es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-109">If [System.ItemType](./props-system-itemtype.md) is VT\_EMPTY, the value of this property is also VT\_EMPTY.</span></span> <span data-ttu-id="1a3c8-110">Si el elemento es un archivo, el valor de esta propiedad es el mismo que si se pasa el valor System. ItemType del archivo a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span><span class="sxs-lookup"><span data-stu-id="1a3c8-110">If the item is a file, the value of this property is the same as if you passed the file's System.ItemType value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay).</span></span>

<span data-ttu-id="1a3c8-111">Esta propiedad no se debe confundir con [System. Kind](./props-system-kind.md), que es un nombre de clase de alto nivel fácil de usar.</span><span class="sxs-lookup"><span data-stu-id="1a3c8-111">This property should not be confused with [System.Kind](./props-system-kind.md), which is a high-level, user-friendly kind name.</span></span> <span data-ttu-id="1a3c8-112">Por ejemplo, para un archivo de documento. doc, las distintas propiedades se muestran a continuación:</span><span class="sxs-lookup"><span data-stu-id="1a3c8-112">For example, for a .doc document file, the various properties are as shown here:</span></span>



| <span data-ttu-id="1a3c8-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a3c8-113">Property</span></span>                                               | <span data-ttu-id="1a3c8-114">Value</span><span class="sxs-lookup"><span data-stu-id="1a3c8-114">Value</span></span>                   |
|--------------------------------------------------------|-------------------------|
| [<span data-ttu-id="1a3c8-115">System. Kind</span><span class="sxs-lookup"><span data-stu-id="1a3c8-115">System.Kind</span></span>](./props-system-kind.md)                 | <span data-ttu-id="1a3c8-116">Documento</span><span class="sxs-lookup"><span data-stu-id="1a3c8-116">Document</span></span>                |
| [<span data-ttu-id="1a3c8-117">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="1a3c8-117">System.ItemType</span></span>](./props-system-itemtype.md)         | <span data-ttu-id="1a3c8-118">.doc</span><span class="sxs-lookup"><span data-stu-id="1a3c8-118">.doc</span></span>                    |
| [<span data-ttu-id="1a3c8-119">System. ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="1a3c8-119">System.ItemTypeText</span></span>]() | <span data-ttu-id="1a3c8-120">Documento de Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="1a3c8-120">Microsoft Word Document</span></span> |



 

<span data-ttu-id="1a3c8-121">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="1a3c8-121">Example values:</span></span>



| <span data-ttu-id="1a3c8-122">Ruta</span><span class="sxs-lookup"><span data-stu-id="1a3c8-122">Path</span></span>                                   | <span data-ttu-id="1a3c8-123">ItemTypeText</span><span class="sxs-lookup"><span data-stu-id="1a3c8-123">ItemTypeText</span></span>            |
|----------------------------------------|-------------------------|
| <span data-ttu-id="1a3c8-124">c: \\hello.txt de la \\ barra myDir \\</span><span class="sxs-lookup"><span data-stu-id="1a3c8-124">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="1a3c8-125">Archivo de texto</span><span class="sxs-lookup"><span data-stu-id="1a3c8-125">Text File</span></span>               |
| <span data-ttu-id="1a3c8-126">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="1a3c8-126">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="1a3c8-127">Documento de Microsoft Word</span><span class="sxs-lookup"><span data-stu-id="1a3c8-127">Microsoft Word Document</span></span> |
| <span data-ttu-id="1a3c8-128">\\\\\\carpeta de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="1a3c8-128">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="1a3c8-129">Carpeta de archivos</span><span class="sxs-lookup"><span data-stu-id="1a3c8-129">File Folder</span></span>             |
| <span data-ttu-id="1a3c8-130">c: \\ MyDir \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="1a3c8-130">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="1a3c8-131">Carpeta de archivos</span><span class="sxs-lookup"><span data-stu-id="1a3c8-131">File Folder</span></span>             |
| <span data-ttu-id="1a3c8-132">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="1a3c8-132">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="1a3c8-133">Mensaje de correo electrónico de Outlook</span><span class="sxs-lookup"><span data-stu-id="1a3c8-133">Outlook E-Mail Message</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="1a3c8-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a3c8-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a3c8-135">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="1a3c8-135">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-136">searchInfo</span><span class="sxs-lookup"><span data-stu-id="1a3c8-136">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-137">labelInfo</span><span class="sxs-lookup"><span data-stu-id="1a3c8-137">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-138">Requerida</span><span class="sxs-lookup"><span data-stu-id="1a3c8-138">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-139">displayInfo</span><span class="sxs-lookup"><span data-stu-id="1a3c8-139">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-140">stringFormat</span><span class="sxs-lookup"><span data-stu-id="1a3c8-140">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-141">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="1a3c8-141">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-142">Numérico</span><span class="sxs-lookup"><span data-stu-id="1a3c8-142">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-143">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="1a3c8-143">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-144">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="1a3c8-144">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-145">drawControl</span><span class="sxs-lookup"><span data-stu-id="1a3c8-145">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-146">editControl</span><span class="sxs-lookup"><span data-stu-id="1a3c8-146">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-147">filterControl</span><span class="sxs-lookup"><span data-stu-id="1a3c8-147">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="1a3c8-148">Consulta</span><span class="sxs-lookup"><span data-stu-id="1a3c8-148">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
