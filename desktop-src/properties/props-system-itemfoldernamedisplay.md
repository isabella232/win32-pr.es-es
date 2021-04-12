---
description: Nombre para mostrar descriptivo de la carpeta primaria de un elemento.
ms.assetid: 4049b6cb-41a1-4df6-89d1-a2022d3a285d
title: System. ItemFolderNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d637412b02345b52fee2e1c13e8f499314af4c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277802"
---
# <a name="systemitemfoldernamedisplay"></a><span data-ttu-id="90ad7-103">System. ItemFolderNameDisplay</span><span class="sxs-lookup"><span data-stu-id="90ad7-103">System.ItemFolderNameDisplay</span></span>

<span data-ttu-id="90ad7-104">Nombre para mostrar descriptivo de la carpeta primaria de un elemento.</span><span class="sxs-lookup"><span data-stu-id="90ad7-104">The user-friendly display name of an item's parent folder.</span></span>

<span data-ttu-id="90ad7-105">Se deriva de [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span><span class="sxs-lookup"><span data-stu-id="90ad7-105">This is derived from [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md).</span></span> <span data-ttu-id="90ad7-106">Si esa propiedad está vacía en VT \_ , esta propiedad también debe ser.</span><span class="sxs-lookup"><span data-stu-id="90ad7-106">If that property is VT\_EMPTY, then this property should be too.</span></span>

<span data-ttu-id="90ad7-107">Si la carpeta es una carpeta de archivos, el valor se traducirá si está disponible un nombre traducido.</span><span class="sxs-lookup"><span data-stu-id="90ad7-107">If the folder is a file folder, the value will be localized if a localized name is available.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="90ad7-108">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="90ad7-108">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderNameDisplay
   shellPKey = PKEY_ItemFolderNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 2
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="90ad7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90ad7-109">Remarks</span></span>

<span data-ttu-id="90ad7-110">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="90ad7-110">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="90ad7-111">Si [System. ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) es VT \_ vacío, esta propiedad también debe estar vacía.</span><span class="sxs-lookup"><span data-stu-id="90ad7-111">If [System.ItemFolderPathDisplay](./props-system-itemfolderpathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="90ad7-112">De lo contrario, el origen de datos debe derivar de la forma adecuada de System. ItemFolderPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="90ad7-112">Otherwise, it should be derived appropriately by the data source from System.ItemFolderPathDisplay.</span></span>

<span data-ttu-id="90ad7-113">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="90ad7-113">Examples:</span></span>



| <span data-ttu-id="90ad7-114">Ruta de acceso dada</span><span class="sxs-lookup"><span data-stu-id="90ad7-114">Given path</span></span>                             | <span data-ttu-id="90ad7-115">Nombre para mostrar de la carpeta</span><span class="sxs-lookup"><span data-stu-id="90ad7-115">Folder Display Name</span></span> |
|----------------------------------------|---------------------|
| <span data-ttu-id="90ad7-116">c: \\ archivo de \\ texto \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="90ad7-116">c:\\MyFiles\\Text\\hello.txt</span></span>           | <span data-ttu-id="90ad7-117">Texto</span><span class="sxs-lookup"><span data-stu-id="90ad7-117">Text</span></span>                |
| <span data-ttu-id="90ad7-118">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="90ad7-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="90ad7-119">myDir</span><span class="sxs-lookup"><span data-stu-id="90ad7-119">mydir</span></span>               |
| <span data-ttu-id="90ad7-120">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="90ad7-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="90ad7-121">Compartir</span><span class="sxs-lookup"><span data-stu-id="90ad7-121">share</span></span>               |
| <span data-ttu-id="90ad7-122">c: \\ carpetas \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="90ad7-122">c:\\Folders\\MyFolder</span></span>                  | <span data-ttu-id="90ad7-123">Carpetas</span><span class="sxs-lookup"><span data-stu-id="90ad7-123">Folders</span></span>             |
| <span data-ttu-id="90ad7-124">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="90ad7-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="90ad7-125">Bandeja de entrada</span><span class="sxs-lookup"><span data-stu-id="90ad7-125">Inbox</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="90ad7-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="90ad7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90ad7-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="90ad7-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="90ad7-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="90ad7-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="90ad7-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="90ad7-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="90ad7-130">Requerida</span><span class="sxs-lookup"><span data-stu-id="90ad7-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="90ad7-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="90ad7-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="90ad7-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="90ad7-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="90ad7-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="90ad7-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="90ad7-134">Numérico</span><span class="sxs-lookup"><span data-stu-id="90ad7-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="90ad7-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="90ad7-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="90ad7-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="90ad7-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="90ad7-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="90ad7-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="90ad7-138">editControl</span><span class="sxs-lookup"><span data-stu-id="90ad7-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="90ad7-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="90ad7-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="90ad7-140">Consulta</span><span class="sxs-lookup"><span data-stu-id="90ad7-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
