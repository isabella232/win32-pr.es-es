---
description: Obtenga información sobre la propiedad System.ItemPathDisplay, que representa la ruta de acceso de presentación fácil de usar al elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System.ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddad0edbc1a77a3de1fab7956d8ce6e6f906f06
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403908"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="600e9-103">System.ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="600e9-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="600e9-104">Ruta de acceso de presentación fácil de usar al elemento.</span><span class="sxs-lookup"><span data-stu-id="600e9-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="600e9-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="600e9-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplay
   shellPKey = PKEY_ItemPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 7
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="600e9-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="600e9-106">Remarks</span></span>

<span data-ttu-id="600e9-107">Los valores PKEY se definen en Propkey.h.</span><span class="sxs-lookup"><span data-stu-id="600e9-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="600e9-108">Si el elemento es un archivo o una carpeta, esta propiedad incluye la extensión en todos los casos y se localiza si hay un nombre localizado disponible.</span><span class="sxs-lookup"><span data-stu-id="600e9-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="600e9-109">Para otros elementos, este es el equivalente fácil de usar, suponiendo que el elemento existe en el almacenamiento jerárquico.</span><span class="sxs-lookup"><span data-stu-id="600e9-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="600e9-110">A [diferencia de System.ItemUrl](./props-system-itemurl.md), este valor de propiedad no incluye el esquema de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="600e9-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="600e9-111">Para analizar una ruta de acceso de elemento, use System.ItemUrl o [System.ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="600e9-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="600e9-112">Para hacer referencia a elementos de espacio de nombres de Shell mediante las API de Shell, use System.ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="600e9-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="600e9-113">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="600e9-113">Example values:</span></span>



| <span data-ttu-id="600e9-114">Ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="600e9-114">Path</span></span>                                   | <span data-ttu-id="600e9-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="600e9-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="600e9-116">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="600e9-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="600e9-117">c: \\ barra de mydir \\ \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="600e9-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="600e9-118">\\\\servidor \\ compartido \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="600e9-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="600e9-119">\\\\servidor \\ compartido \\ mydir \\goodnews.doc</span><span class="sxs-lookup"><span data-stu-id="600e9-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="600e9-120">\\\\servidor \\ compartidonumbers.xls \\</span><span class="sxs-lookup"><span data-stu-id="600e9-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="600e9-121">\\\\servidor \\ compartidonumbers.xls \\</span><span class="sxs-lookup"><span data-stu-id="600e9-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="600e9-122">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="600e9-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="600e9-123">c: \\ mydir \\ MyFolder</span><span class="sxs-lookup"><span data-stu-id="600e9-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="600e9-124">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="600e9-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="600e9-125">/Mailbox Account/Inbox/'Re: Hello!'</span><span class="sxs-lookup"><span data-stu-id="600e9-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="600e9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="600e9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600e9-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="600e9-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="600e9-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="600e9-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="600e9-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="600e9-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="600e9-130">typeInfo</span><span class="sxs-lookup"><span data-stu-id="600e9-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="600e9-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="600e9-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="600e9-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="600e9-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="600e9-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="600e9-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="600e9-134">numberFormat</span><span class="sxs-lookup"><span data-stu-id="600e9-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="600e9-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="600e9-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="600e9-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="600e9-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="600e9-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="600e9-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="600e9-138">editControl</span><span class="sxs-lookup"><span data-stu-id="600e9-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="600e9-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="600e9-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="600e9-140">queryControl</span><span class="sxs-lookup"><span data-stu-id="600e9-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
