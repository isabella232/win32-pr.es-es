---
description: La ruta de acceso de visualización fácil de ver al elemento.
ms.assetid: 27e4490b-7914-4b38-9799-e9d5dc407f13
title: System. ItemPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb76a4218e7e7580ec70cb57dd16c635ca024ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156420"
---
# <a name="systemitempathdisplay"></a><span data-ttu-id="b7adc-103">System. ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="b7adc-103">System.ItemPathDisplay</span></span>

<span data-ttu-id="b7adc-104">La ruta de acceso de visualización fácil de ver al elemento.</span><span class="sxs-lookup"><span data-stu-id="b7adc-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="b7adc-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7adc-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

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

## <a name="remarks"></a><span data-ttu-id="b7adc-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7adc-106">Remarks</span></span>

<span data-ttu-id="b7adc-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="b7adc-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="b7adc-108">Si el elemento es un archivo o una carpeta, esta propiedad incluye la extensión en todos los casos y se localiza si hay disponible un nombre traducido.</span><span class="sxs-lookup"><span data-stu-id="b7adc-108">If the item is a file or folder, this property includes the extension in all cases, and is localized if a localized name is available.</span></span> <span data-ttu-id="b7adc-109">En el caso de otros elementos, este es el equivalente descriptivo, siempre que el elemento exista en el almacenamiento jerárquico.</span><span class="sxs-lookup"><span data-stu-id="b7adc-109">For other items, this is the user-friendly equivalent, assuming that the item exists in hierarchical storage.</span></span>

<span data-ttu-id="b7adc-110">A diferencia de [System. ItemUrl](./props-system-itemurl.md), este valor de propiedad no incluye el esquema de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="b7adc-110">Unlike [System.ItemUrl](./props-system-itemurl.md), this property value does not include the URL scheme.</span></span> <span data-ttu-id="b7adc-111">Para analizar una ruta de acceso de elemento, use System. ItemUrl o [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="b7adc-111">To parse an item path, use System.ItemUrl or [System.ParsingPath](./props-system-parsingpath.md).</span></span> <span data-ttu-id="b7adc-112">Para hacer referencia a elementos de espacio de nombres del shell mediante las API de Shell, use System. ParsingPath.</span><span class="sxs-lookup"><span data-stu-id="b7adc-112">To reference Shell namespace items using Shell APIs, use System.ParsingPath.</span></span>

<span data-ttu-id="b7adc-113">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="b7adc-113">Example values:</span></span>



| <span data-ttu-id="b7adc-114">Ruta</span><span class="sxs-lookup"><span data-stu-id="b7adc-114">Path</span></span>                                   | <span data-ttu-id="b7adc-115">ItemPathDisplay</span><span class="sxs-lookup"><span data-stu-id="b7adc-115">ItemPathDisplay</span></span>                        |
|----------------------------------------|----------------------------------------|
| <span data-ttu-id="b7adc-116">c: \\hello.txt de la \\ barra myDir \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-116">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="b7adc-117">c: \\hello.txt de la \\ barra myDir \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-117">c:\\mydir\\bar\\hello.txt</span></span>              |
| <span data-ttu-id="b7adc-118">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-118">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="b7adc-119">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-119">\\\\server\\share\\mydir\\goodnews.doc</span></span> |
| <span data-ttu-id="b7adc-120">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-120">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="b7adc-121">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="b7adc-121">\\\\server\\share\\numbers.xls</span></span>         |
| <span data-ttu-id="b7adc-122">c: \\ myDir \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="b7adc-122">c:\\mydir\\MyFolder</span></span>                    | <span data-ttu-id="b7adc-123">c: \\ myDir \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="b7adc-123">c:\\mydir\\MyFolder</span></span>                    |
| <span data-ttu-id="b7adc-124">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="b7adc-124">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="b7adc-125">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="b7adc-125">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="b7adc-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b7adc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7adc-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="b7adc-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="b7adc-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="b7adc-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="b7adc-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="b7adc-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="b7adc-130">Requerida</span><span class="sxs-lookup"><span data-stu-id="b7adc-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="b7adc-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b7adc-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="b7adc-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="b7adc-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="b7adc-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="b7adc-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="b7adc-134">Numérico</span><span class="sxs-lookup"><span data-stu-id="b7adc-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="b7adc-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="b7adc-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="b7adc-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="b7adc-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="b7adc-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="b7adc-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7adc-138">editControl</span><span class="sxs-lookup"><span data-stu-id="b7adc-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="b7adc-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="b7adc-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="b7adc-140">Consulta</span><span class="sxs-lookup"><span data-stu-id="b7adc-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
