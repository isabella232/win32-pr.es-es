---
description: Representa una dirección URL con formato correcto que señala al elemento.
ms.assetid: d592f12b-f8c2-406f-a031-eeb8212e64f7
title: System. ItemUrl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d02beb9629661a052d2ec1fae7c7a34e999e777e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707165"
---
# <a name="systemitemurl"></a><span data-ttu-id="73e7c-103">System. ItemUrl</span><span class="sxs-lookup"><span data-stu-id="73e7c-103">System.ItemUrl</span></span>

<span data-ttu-id="73e7c-104">Representa una dirección URL con formato correcto que señala al elemento.</span><span class="sxs-lookup"><span data-stu-id="73e7c-104">Represents a well-formed URL that points to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="73e7c-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73e7c-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemUrl
   shellPKey = PKEY_ItemUrl
   formatID = 49691C90-7E17-101A-A91C-08002B2ECDA9
   propID = 9
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="73e7c-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="73e7c-106">Remarks</span></span>

<span data-ttu-id="73e7c-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="73e7c-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="73e7c-108">Para hacer referencia a los elementos del espacio de nombres del shell a través de las API de Shell, use [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="73e7c-108">To reference Shell namespace items through Shell APIs, use [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="73e7c-109">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="73e7c-109">Example values:</span></span>



| <span data-ttu-id="73e7c-110">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="73e7c-110">Item type</span></span> | <span data-ttu-id="73e7c-111">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73e7c-111">Example</span></span>                        |
|-----------|--------------------------------|
| <span data-ttu-id="73e7c-112">Archivo</span><span class="sxs-lookup"><span data-stu-id="73e7c-112">File</span></span>      | <span data-ttu-id="73e7c-113">hello.txt file:///c:/mydir/bar/</span><span class="sxs-lookup"><span data-stu-id="73e7c-113">file:///c:/mydir/bar/hello.txt</span></span> |
| <span data-ttu-id="73e7c-114">Archivo</span><span class="sxs-lookup"><span data-stu-id="73e7c-114">File</span></span>      | <span data-ttu-id="73e7c-115">CSC://{GUID}/...</span><span class="sxs-lookup"><span data-stu-id="73e7c-115">csc://{GUID}/...</span></span>               |
| <span data-ttu-id="73e7c-116">Message</span><span class="sxs-lookup"><span data-stu-id="73e7c-116">Message</span></span>   | <span data-ttu-id="73e7c-117">mapi://...</span><span class="sxs-lookup"><span data-stu-id="73e7c-117">mapi://...</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="73e7c-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73e7c-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e7c-119">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="73e7c-119">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="73e7c-120">searchInfo</span><span class="sxs-lookup"><span data-stu-id="73e7c-120">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="73e7c-121">labelInfo</span><span class="sxs-lookup"><span data-stu-id="73e7c-121">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="73e7c-122">Requerida</span><span class="sxs-lookup"><span data-stu-id="73e7c-122">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="73e7c-123">displayInfo</span><span class="sxs-lookup"><span data-stu-id="73e7c-123">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="73e7c-124">stringFormat</span><span class="sxs-lookup"><span data-stu-id="73e7c-124">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="73e7c-125">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="73e7c-125">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="73e7c-126">Numérico</span><span class="sxs-lookup"><span data-stu-id="73e7c-126">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="73e7c-127">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="73e7c-127">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="73e7c-128">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="73e7c-128">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="73e7c-129">drawControl</span><span class="sxs-lookup"><span data-stu-id="73e7c-129">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="73e7c-130">editControl</span><span class="sxs-lookup"><span data-stu-id="73e7c-130">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="73e7c-131">filterControl</span><span class="sxs-lookup"><span data-stu-id="73e7c-131">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="73e7c-132">Consulta</span><span class="sxs-lookup"><span data-stu-id="73e7c-132">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
