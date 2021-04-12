---
description: La ruta de acceso de visualización fácil de ver al elemento.
ms.assetid: 5dd44e13-bc5c-4e32-b5eb-2c7c40e10dfb
title: System. ItemPathDisplayNarrow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87ef7b9d03a78a23e955c20f52e32062a8bcabd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278326"
---
# <a name="systemitempathdisplaynarrow"></a><span data-ttu-id="2eb1e-103">System. ItemPathDisplayNarrow</span><span class="sxs-lookup"><span data-stu-id="2eb1e-103">System.ItemPathDisplayNarrow</span></span>

<span data-ttu-id="2eb1e-104">La ruta de acceso de visualización fácil de ver al elemento.</span><span class="sxs-lookup"><span data-stu-id="2eb1e-104">The user-friendly display path to the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="2eb1e-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eb1e-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemPathDisplayNarrow
   shellPKey = PKEY_ItemPathDisplayNarrow
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 8
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="2eb1e-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2eb1e-106">Remarks</span></span>

<span data-ttu-id="2eb1e-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="2eb1e-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="2eb1e-108">Para optimizar en una columna de visualización estrecha, el formato de la cadena debe estar adaptado para que el nombre aparezca primero.</span><span class="sxs-lookup"><span data-stu-id="2eb1e-108">To optimize for a narrow viewing column, the format of the string should be tailored so that the name comes first.</span></span>

<span data-ttu-id="2eb1e-109">Si el elemento es un archivo, el valor de la propiedad excluye la extensión de archivo, pero incluye nombres localizados si están presentes.</span><span class="sxs-lookup"><span data-stu-id="2eb1e-109">If the item is a file, the property value excludes the file extension, but includes localized names if they are present.</span></span> <span data-ttu-id="2eb1e-110">Si el elemento es un mensaje, el valor incluye [System. ItemNamePrefix](./props-system-itemnameprefix.md).</span><span class="sxs-lookup"><span data-stu-id="2eb1e-110">If the item is a message, the value includes the [System.ItemNamePrefix](./props-system-itemnameprefix.md).</span></span> <span data-ttu-id="2eb1e-111">Para analizar una ruta de acceso de elemento, use [System. ItemUrl](./props-system-itemurl.md) o [System. ParsingPath](./props-system-parsingpath.md).</span><span class="sxs-lookup"><span data-stu-id="2eb1e-111">To parse an item path, use [System.ItemUrl](./props-system-itemurl.md) or [System.ParsingPath](./props-system-parsingpath.md).</span></span>

<span data-ttu-id="2eb1e-112">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="2eb1e-112">Example values:</span></span>



| <span data-ttu-id="2eb1e-113">Ruta</span><span class="sxs-lookup"><span data-stu-id="2eb1e-113">Path</span></span>                                   | <span data-ttu-id="2eb1e-114">ItemPathDisplayName</span><span class="sxs-lookup"><span data-stu-id="2eb1e-114">ItemPathDisplayName</span></span>                 |
|----------------------------------------|-------------------------------------|
| <span data-ttu-id="2eb1e-115">c: \\hello.txt de la \\ barra myDir \\</span><span class="sxs-lookup"><span data-stu-id="2eb1e-115">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="2eb1e-116">Hola (c: \\ myDir \\ bar)</span><span class="sxs-lookup"><span data-stu-id="2eb1e-116">hello (c:\\mydir\\bar)</span></span>              |
| <span data-ttu-id="2eb1e-117">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="2eb1e-117">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="2eb1e-118">Goodnews ( \\ \\ \\ recurso compartido de servidor \\ myDir)</span><span class="sxs-lookup"><span data-stu-id="2eb1e-118">goodnews (\\\\server\\share\\mydir)</span></span> |
| <span data-ttu-id="2eb1e-119">\\\\\\carpeta de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="2eb1e-119">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="2eb1e-120">carpeta ( \\ \\ \\ recurso compartido de servidor)</span><span class="sxs-lookup"><span data-stu-id="2eb1e-120">folder (\\\\server\\share)</span></span>          |
| <span data-ttu-id="2eb1e-121">c: \\ MyDir \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="2eb1e-121">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="2eb1e-122">Carpeta (c: \\ myDir)</span><span class="sxs-lookup"><span data-stu-id="2eb1e-122">MyFolder (c:\\mydir)</span></span>                |
| <span data-ttu-id="2eb1e-123">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="2eb1e-123">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="2eb1e-124">Re: ¡ Hola!</span><span class="sxs-lookup"><span data-stu-id="2eb1e-124">Re: Hello!</span></span> <span data-ttu-id="2eb1e-125">(Cuenta o bandeja de entrada de/Mailbox)</span><span class="sxs-lookup"><span data-stu-id="2eb1e-125">(/Mailbox Account/Inbox)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="2eb1e-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2eb1e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eb1e-127">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="2eb1e-127">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-128">searchInfo</span><span class="sxs-lookup"><span data-stu-id="2eb1e-128">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-129">labelInfo</span><span class="sxs-lookup"><span data-stu-id="2eb1e-129">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-130">Requerida</span><span class="sxs-lookup"><span data-stu-id="2eb1e-130">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-131">displayInfo</span><span class="sxs-lookup"><span data-stu-id="2eb1e-131">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-132">stringFormat</span><span class="sxs-lookup"><span data-stu-id="2eb1e-132">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-133">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="2eb1e-133">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-134">Numérico</span><span class="sxs-lookup"><span data-stu-id="2eb1e-134">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-135">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2eb1e-135">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-136">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="2eb1e-136">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-137">drawControl</span><span class="sxs-lookup"><span data-stu-id="2eb1e-137">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-138">editControl</span><span class="sxs-lookup"><span data-stu-id="2eb1e-138">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-139">filterControl</span><span class="sxs-lookup"><span data-stu-id="2eb1e-139">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="2eb1e-140">Consulta</span><span class="sxs-lookup"><span data-stu-id="2eb1e-140">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
