---
description: Tipo canónico del elemento.
ms.assetid: 530ba98a-09fd-438b-8872-9eee47f0cf54
title: System. ItemType
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0159a12e1cc3c6d85e461461cad20334a641fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278882"
---
# <a name="systemitemtype"></a><span data-ttu-id="7c44d-103">System. ItemType</span><span class="sxs-lookup"><span data-stu-id="7c44d-103">System.ItemType</span></span>

<span data-ttu-id="7c44d-104">Tipo canónico del elemento.</span><span class="sxs-lookup"><span data-stu-id="7c44d-104">The canonical type of the item.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="7c44d-105">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c44d-105">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemType
   shellPKey = PKEY_ItemType
   formatID = 28636AA6-953D-11D2-B5D6-00C04FD918D0
   propID = 11
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="7c44d-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c44d-106">Remarks</span></span>

<span data-ttu-id="7c44d-107">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="7c44d-107">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="7c44d-108">El valor de System. ItemType está diseñado para analizarse mediante programación y puede ser:</span><span class="sxs-lookup"><span data-stu-id="7c44d-108">The value for System.ItemType is intended to be programmatically parsed, and can be either:</span></span>

-   <span data-ttu-id="7c44d-109">Extensión de archivo que señala a un valor ProgID ( \_ clase HKEY \_ raíz \\ <ProgID> ) que contiene el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="7c44d-109">A file extension that points to a ProgID value (HKEY\_CLASSES\_ROOT\\<ProgID>) holding the display name for the type.</span></span>
-   <span data-ttu-id="7c44d-110">Un valor ProgID ( \_ clases HKEY \_ RROOT \\ <ProgID> ), que contiene el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="7c44d-110">A ProgID value (HKEY\_CLASSES\_RROOT\\<ProgID>), containing the display name for the type.</span></span>

<span data-ttu-id="7c44d-111">El elemento FriendlyTypeName de un ProgID debe ser una versión localizada del nombre de la aplicación ( @winword.dll ,-42), mientras que el valor predeterminado de la clave ProgID es un nombre no traducido (Word.Document. 12).</span><span class="sxs-lookup"><span data-stu-id="7c44d-111">The FriendlyTypeName element of a ProgID should be a localized version of the application name (@winword.dll,-42), while the default value of the ProgID key is a non-localized name (Word.Document.12).</span></span>

<span data-ttu-id="7c44d-112">Si no hay ningún tipo canónico, el valor es VT \_ vacío.</span><span class="sxs-lookup"><span data-stu-id="7c44d-112">If there is no canonical type, the value is VT\_EMPTY.</span></span> <span data-ttu-id="7c44d-113">Si el elemento es un archivo ([System. FileName](./props-system-filename.md) no es VT \_ vacío), el valor es el mismo que [System. FileExtension](./props-system-fileextension.md).</span><span class="sxs-lookup"><span data-stu-id="7c44d-113">If the item is a file ([System.FileName](./props-system-filename.md) is not VT\_EMPTY), the value is the same as [System.FileExtension](./props-system-fileextension.md).</span></span> <span data-ttu-id="7c44d-114">Use [System. ItemTypeText](./props-system-itemtypetext.md) cuando desee mostrar el tipo a los usuarios finales en una vista.</span><span class="sxs-lookup"><span data-stu-id="7c44d-114">Use [System.ItemTypeText](./props-system-itemtypetext.md) when you want to display the type to end users in a view.</span></span>

> [!Note]  
> <span data-ttu-id="7c44d-115">Si el elemento es un archivo, pasar el valor [System. ItemType]() a [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) da como resultado el mismo valor que [System. ItemTypeText](./props-system-itemtypetext.md).</span><span class="sxs-lookup"><span data-stu-id="7c44d-115">If the item is a file, passing the [System.ItemType]() value to [**PSFormatForDisplay**](/windows/win32/api/propsys/nf-propsys-psformatfordisplay) results in the same value as [System.ItemTypeText](./props-system-itemtypetext.md).</span></span>

 

<span data-ttu-id="7c44d-116">Valores de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="7c44d-116">Example values:</span></span>



| <span data-ttu-id="7c44d-117">Ruta</span><span class="sxs-lookup"><span data-stu-id="7c44d-117">Path</span></span>                                   | <span data-ttu-id="7c44d-118">ItemType</span><span class="sxs-lookup"><span data-stu-id="7c44d-118">ItemType</span></span>         |
|----------------------------------------|------------------|
| <span data-ttu-id="7c44d-119">c: \\hello.txt de la \\ barra myDir \\</span><span class="sxs-lookup"><span data-stu-id="7c44d-119">c:\\mydir\\bar\\hello.txt</span></span>              | <span data-ttu-id="7c44d-120">.txt</span><span class="sxs-lookup"><span data-stu-id="7c44d-120">.txt</span></span>             |
| <span data-ttu-id="7c44d-121">\\\\\\goodnews.doc del recurso compartido del servidor \\ myDir \\</span><span class="sxs-lookup"><span data-stu-id="7c44d-121">\\\\server\\share\\mydir\\goodnews.doc</span></span> | <span data-ttu-id="7c44d-122">.doc</span><span class="sxs-lookup"><span data-stu-id="7c44d-122">.doc</span></span>             |
| <span data-ttu-id="7c44d-123">\\\\\\carpeta de recurso compartido de servidor \\</span><span class="sxs-lookup"><span data-stu-id="7c44d-123">\\\\server\\share\\folder</span></span>              | <span data-ttu-id="7c44d-124">Directorio</span><span class="sxs-lookup"><span data-stu-id="7c44d-124">Directory</span></span>        |
| <span data-ttu-id="7c44d-125">c: \\ MyDir \\ carpeta</span><span class="sxs-lookup"><span data-stu-id="7c44d-125">c:\\MyDir\\MyFolder</span></span>                    | <span data-ttu-id="7c44d-126">Directorio</span><span class="sxs-lookup"><span data-stu-id="7c44d-126">Directory</span></span>        |
| <span data-ttu-id="7c44d-127">\[desktop\]</span><span class="sxs-lookup"><span data-stu-id="7c44d-127">\[desktop\]</span></span>                            | <span data-ttu-id="7c44d-128">Carpeta</span><span class="sxs-lookup"><span data-stu-id="7c44d-128">Folder</span></span>           |
| <span data-ttu-id="7c44d-129">Cuenta o bandeja de entrada de/Mailbox/' re: Hello! '</span><span class="sxs-lookup"><span data-stu-id="7c44d-129">/Mailbox Account/Inbox/'Re: Hello!'</span></span>    | <span data-ttu-id="7c44d-130">MAPI/IPM. Mensaje</span><span class="sxs-lookup"><span data-stu-id="7c44d-130">MAPI/IPM.Message</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7c44d-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7c44d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c44d-132">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="7c44d-132">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="7c44d-133">searchInfo</span><span class="sxs-lookup"><span data-stu-id="7c44d-133">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="7c44d-134">labelInfo</span><span class="sxs-lookup"><span data-stu-id="7c44d-134">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="7c44d-135">Requerida</span><span class="sxs-lookup"><span data-stu-id="7c44d-135">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="7c44d-136">displayInfo</span><span class="sxs-lookup"><span data-stu-id="7c44d-136">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="7c44d-137">stringFormat</span><span class="sxs-lookup"><span data-stu-id="7c44d-137">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="7c44d-138">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="7c44d-138">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="7c44d-139">Numérico</span><span class="sxs-lookup"><span data-stu-id="7c44d-139">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="7c44d-140">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="7c44d-140">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="7c44d-141">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="7c44d-141">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="7c44d-142">drawControl</span><span class="sxs-lookup"><span data-stu-id="7c44d-142">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c44d-143">editControl</span><span class="sxs-lookup"><span data-stu-id="7c44d-143">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="7c44d-144">filterControl</span><span class="sxs-lookup"><span data-stu-id="7c44d-144">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="7c44d-145">Consulta</span><span class="sxs-lookup"><span data-stu-id="7c44d-145">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="7c44d-146">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="7c44d-146">Programmatic Identifiers</span></span>](../shell/fa-progids.md)
</dt> </dl>

 

 
