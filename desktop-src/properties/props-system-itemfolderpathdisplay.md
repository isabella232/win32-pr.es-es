---
description: La ruta de acceso de visualización fácil de ver de la carpeta primaria de un elemento.
ms.assetid: 16f67edc-ca8a-4c2e-9d9b-be8600446e51
title: System. ItemFolderPathDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c4ae4c9178356d36c644f1bc886d63331155e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715971"
---
# <a name="systemitemfolderpathdisplay"></a><span data-ttu-id="fd307-103">System. ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="fd307-103">System.ItemFolderPathDisplay</span></span>

<span data-ttu-id="fd307-104">La ruta de acceso de visualización fácil de ver de la carpeta primaria de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd307-104">The user-friendly display path of an item's parent folder.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="fd307-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fd307-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemFolderPathDisplay
   shellPKey = PKEY_ItemFolderPathDisplay
   formatID = E3E0584C-B788-4A5A-BB20-7F5A44C9ACDD
   propID = 6
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="fd307-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd307-106">Remarks</span></span>

<span data-ttu-id="fd307-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="fd307-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="fd307-108">Si [System. ItemPathDisplay](./props-system-itempathdisplay.md) es VT \_ vacío, esta propiedad también debe estar vacía.</span><span class="sxs-lookup"><span data-stu-id="fd307-108">If [System.ItemPathDisplay](./props-system-itempathdisplay.md) is VT\_EMPTY, then this property should also be empty.</span></span> <span data-ttu-id="fd307-109">De lo contrario, el origen de datos debe derivar de la forma adecuada de System. ItemPathDisplay.</span><span class="sxs-lookup"><span data-stu-id="fd307-109">Otherwise, it should be derived appropriately by the data source from System.ItemPathDisplay.</span></span>

<span data-ttu-id="fd307-110">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="fd307-110">Example values:</span></span>



| <span data-ttu-id="fd307-111">Ruta</span><span class="sxs-lookup"><span data-stu-id="fd307-111">Path</span></span>                                   | <span data-ttu-id="fd307-112">ItemFolderPathDisplay</span><span class="sxs-lookup"><span data-stu-id="fd307-112">ItemFolderPathDisplay</span></span>    |
|----------------------------------------|--------------------------|
| <span data-ttu-id="fd307-113">c: \\ archivos \\ personales \\hello.txt</span><span class="sxs-lookup"><span data-stu-id="fd307-113">c:\\files\\personal\\hello.txt</span></span>         | <span data-ttu-id="fd307-114">c: \\ archivos \\ personales</span><span class="sxs-lookup"><span data-stu-id="fd307-114">c:\\files\\personal</span></span>      |
| <span data-ttu-id="fd307-115">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="fd307-115">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="fd307-116">\\\\\\myDir de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="fd307-116">\\\\server\\share\\mydir</span></span> |
| <span data-ttu-id="fd307-117">\\\\\\numbers.xls de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="fd307-117">\\\\server\\share\\numbers.xls</span></span>         | <span data-ttu-id="fd307-118">\\\\\\recurso compartido de servidor</span><span class="sxs-lookup"><span data-stu-id="fd307-118">\\\\server\\share</span></span>        |
| <span data-ttu-id="fd307-119">c: \\ mi \\ carpeta comida</span><span class="sxs-lookup"><span data-stu-id="fd307-119">c:\\food\\MyFolder</span></span>                     | <span data-ttu-id="fd307-120">c: \\ alimentación</span><span class="sxs-lookup"><span data-stu-id="fd307-120">c:\\food</span></span>                 |
| <span data-ttu-id="fd307-121">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="fd307-121">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="fd307-122">Cuenta o bandeja de entrada de/Mailbox</span><span class="sxs-lookup"><span data-stu-id="fd307-122">/Mailbox Account/Inbox</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="fd307-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd307-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd307-124">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="fd307-124">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="fd307-125">searchInfo</span><span class="sxs-lookup"><span data-stu-id="fd307-125">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="fd307-126">labelInfo</span><span class="sxs-lookup"><span data-stu-id="fd307-126">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="fd307-127">Requerida</span><span class="sxs-lookup"><span data-stu-id="fd307-127">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="fd307-128">displayInfo</span><span class="sxs-lookup"><span data-stu-id="fd307-128">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="fd307-129">stringFormat</span><span class="sxs-lookup"><span data-stu-id="fd307-129">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="fd307-130">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="fd307-130">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="fd307-131">Numérico</span><span class="sxs-lookup"><span data-stu-id="fd307-131">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="fd307-132">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="fd307-132">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="fd307-133">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="fd307-133">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="fd307-134">drawControl</span><span class="sxs-lookup"><span data-stu-id="fd307-134">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd307-135">editControl</span><span class="sxs-lookup"><span data-stu-id="fd307-135">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="fd307-136">filterControl</span><span class="sxs-lookup"><span data-stu-id="fd307-136">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="fd307-137">Consulta</span><span class="sxs-lookup"><span data-stu-id="fd307-137">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
