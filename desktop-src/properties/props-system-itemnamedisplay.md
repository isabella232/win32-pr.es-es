---
description: El nombre para mostrar en &\# 0034; el formulario más completo&\# 0034;.
ms.assetid: fdb6b0fa-0741-4edc-8902-763a461313b9
title: System.ItemNameDisplay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf735935ee7971acad7d11ee91636e18a6542252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810982"
---
# <a name="systemitemnamedisplay"></a><span data-ttu-id="29fab-103">System.ItemNameDisplay</span><span class="sxs-lookup"><span data-stu-id="29fab-103">System.ItemNameDisplay</span></span>

<span data-ttu-id="29fab-104">El nombre para mostrar en el formulario "más completo".</span><span class="sxs-lookup"><span data-stu-id="29fab-104">The display name in "most complete" form.</span></span> <span data-ttu-id="29fab-105">Es la representación única del nombre del elemento más adecuada para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="29fab-105">It is the unique representation of the item name most appropriate for end users.</span></span>

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7-windows-vista"></a><span data-ttu-id="29fab-106">Windows 10, versión 1703, Windows 10, versión 1607, Windows 10, versión 1511, Windows 10, versión 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29fab-106">Windows 10, version 1703, Windows 10, version 1607, Windows 10, version 1511, Windows 10, version 1507, Windows 8.1, Windows 8, Windows 7, Windows Vista</span></span>

```
propertyDescription
   name = System.ItemNameDisplay
   shellPKey = PKEY_ItemNameDisplay
   formatID = B725F130-47EF-101A-A5F1-02608C9EEBAC
   propID = 10
   SearchInfo
      InInvertedIndex = true
      IsColumn = true
   typeInfo
      type = String
      IsInnate = true
```

## <a name="remarks"></a><span data-ttu-id="29fab-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29fab-107">Remarks</span></span>

<span data-ttu-id="29fab-108">Los valores PKEY se definen en Propkey. h.</span><span class="sxs-lookup"><span data-stu-id="29fab-108">PKEY values are defined in Propkey.h.</span></span>

<span data-ttu-id="29fab-109">Este valor es concatentation de [System. ItemNamePrefix](./props-system-itemnameprefix.md) y [System. itemname](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="29fab-109">This value is the concatentation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span>

<span data-ttu-id="29fab-110">Si el elemento es un archivo, esta propiedad incluye el nombre para mostrar tal como se muestra en el explorador de archivos.</span><span class="sxs-lookup"><span data-stu-id="29fab-110">If the item is a file, this property includes the display name as shown in File Explorer.</span></span> <span data-ttu-id="29fab-111">Hay casos aceptables cuando se proporciona [System. FileName](./props-system-filename.md) pero el valor de esta propiedad es completamente diferente.</span><span class="sxs-lookup"><span data-stu-id="29fab-111">There are acceptable cases when [System.FileName](./props-system-filename.md) is given but the value of this property is completely different.</span></span> <span data-ttu-id="29fab-112">Los mensajes de correo electrónico son un buen ejemplo.</span><span class="sxs-lookup"><span data-stu-id="29fab-112">E-mail messages are a good example.</span></span> <span data-ttu-id="29fab-113">Si el elemento es un mensaje de correo electrónico, el nombre del elemento es normalmente el asunto.</span><span class="sxs-lookup"><span data-stu-id="29fab-113">If the item is an e-mail message, the item name is normally the subject.</span></span> <span data-ttu-id="29fab-114">En ese caso, el valor debe ser la concatenación de [System. ItemNamePrefix](./props-system-itemnameprefix.md) y [System. itemname](./props-system-itemname.md).</span><span class="sxs-lookup"><span data-stu-id="29fab-114">In that case, the value must be the concatenation of [System.ItemNamePrefix](./props-system-itemnameprefix.md) and [System.ItemName](./props-system-itemname.md).</span></span> <span data-ttu-id="29fab-115">Dado que el valor de System. ItemNamePrefix excluye los espacios finales, la concatenación debe incluir un espacio al generar [System. ItemNameDisplay]().</span><span class="sxs-lookup"><span data-stu-id="29fab-115">Since the value of System.ItemNamePrefix excludes any trailing spaces, the concatenation must include a space when generating [System.ItemNameDisplay]().</span></span> <span data-ttu-id="29fab-116">Tenga en cuenta que no se garantiza que esta propiedad sea única, sino que está diseñada para promocionar el candidato más probable que puede ser único y que también tenga sentido para los usuarios finales.</span><span class="sxs-lookup"><span data-stu-id="29fab-116">Note that this property is not guaranteed to be unique, but is designed to promote the most likely candidate that can be unique and also makes sense to end users.</span></span>

<span data-ttu-id="29fab-117">Por ejemplo, para los documentos, el [nombre System. title](./props-system-title.md) podría usarse como [System. ItemNameDisplay](), pero en la práctica el título de los documentos puede no ser útil o lo suficientemente exclusivo como para funcionar como System. ItemNameDisplay.</span><span class="sxs-lookup"><span data-stu-id="29fab-117">For example, for documents, the [System.Title](./props-system-title.md) could be used as the [System.ItemNameDisplay](), but in practice the title of the documents may not be useful or unique enough to function as the sole System.ItemNameDisplay.</span></span> <span data-ttu-id="29fab-118">En su lugar, proporcionar [System. FileName](./props-system-filename.md) como el valor de System. ItemNameDisplay es una opción mejor.</span><span class="sxs-lookup"><span data-stu-id="29fab-118">Instead, providing [System.FileName](./props-system-filename.md) as the value of System.ItemNameDisplay is a better choice.</span></span> <span data-ttu-id="29fab-119">En Windows Mail, el correo electrónico se almacena en el sistema de archivos como archivos. eml.</span><span class="sxs-lookup"><span data-stu-id="29fab-119">In Windows Mail, e-mail is stored in the file system as .eml files.</span></span> <span data-ttu-id="29fab-120">Los valores System. FileName para esos archivos no son descriptivos, ya que son GUID.</span><span class="sxs-lookup"><span data-stu-id="29fab-120">The System.FileName values for those files are not human-friendly as they are GUIDs.</span></span> <span data-ttu-id="29fab-121">En este ejemplo, la promoción de [System. Subject](./props-system-subject.md) como System. ItemNameDisplay tiene más sentido.</span><span class="sxs-lookup"><span data-stu-id="29fab-121">In this example, promoting [System.Subject](./props-system-subject.md) as System.ItemNameDisplay makes more sense.</span></span>

<span data-ttu-id="29fab-122">**Notas de compatibilidad:**</span><span class="sxs-lookup"><span data-stu-id="29fab-122">**Compatibility notes:**</span></span>

-   <span data-ttu-id="29fab-123">Implementaciones de carpetas de Shell en Windows Vista: Use PKEY \_ ItemNameDisplay para la columna nombre cuando desee que el explorador de Windows llame a [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN \_ normal) para obtener el valor del nombre.</span><span class="sxs-lookup"><span data-stu-id="29fab-123">Shell folder implementations on Windows Vista: use PKEY\_ItemNameDisplay for the name column when you want Windows Explorer to call [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)(SHGDN\_NORMAL) to get the value of the name.</span></span> <span data-ttu-id="29fab-124">Use otro PKEY, como PKEY \_ itemname, cuando desee que el explorador de Windows llame al almacén de propiedades de la carpeta o [**IShellFolder2:: GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) para obtener el valor del nombre.</span><span class="sxs-lookup"><span data-stu-id="29fab-124">Use another PKEY, such as PKEY\_ItemName, when you want Windows Explorer to call either the folder's property store or [**IShellFolder2::GetDetailsEx**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex) to get the value of the name.</span></span>
-   <span data-ttu-id="29fab-125">Implementaciones de carpetas de Shell en Windows XP: la primera columna debe ser la columna Name y el explorador de Windows llama a [**IShellFolder:: GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) para obtener el valor del nombre.</span><span class="sxs-lookup"><span data-stu-id="29fab-125">Shell folder implementations on Windows XP: the first column must be the name column, and Windows Explorer calls [**IShellFolder::GetDisplayNameOf**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to get the value of the name.</span></span> <span data-ttu-id="29fab-126">PKEY/SCID no importa.</span><span class="sxs-lookup"><span data-stu-id="29fab-126">The PKEY/SCID does not matter.</span></span>



| <span data-ttu-id="29fab-127">Tipo de elemento</span><span class="sxs-lookup"><span data-stu-id="29fab-127">Item type</span></span>     | <span data-ttu-id="29fab-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29fab-128">Example</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="29fab-129">Archivo</span><span class="sxs-lookup"><span data-stu-id="29fab-129">File</span></span>          | <span data-ttu-id="29fab-130">hello.txt</span><span class="sxs-lookup"><span data-stu-id="29fab-130">hello.txt</span></span>                 |
| <span data-ttu-id="29fab-131">Message</span><span class="sxs-lookup"><span data-stu-id="29fab-131">Message</span></span>       | <span data-ttu-id="29fab-132">Re: ¿Dónde está la reunión?</span><span class="sxs-lookup"><span data-stu-id="29fab-132">Re: Where is the meeting?</span></span> |
| <span data-ttu-id="29fab-133">Carpeta de dispositivo</span><span class="sxs-lookup"><span data-stu-id="29fab-133">Device folder</span></span> | <span data-ttu-id="29fab-134">Song. WMA</span><span class="sxs-lookup"><span data-stu-id="29fab-134">song.wma</span></span>                  |
| <span data-ttu-id="29fab-135">Carpeta</span><span class="sxs-lookup"><span data-stu-id="29fab-135">Folder</span></span>        | <span data-ttu-id="29fab-136">Documentos</span><span class="sxs-lookup"><span data-stu-id="29fab-136">Documents</span></span>                 |



 

## <a name="related-topics"></a><span data-ttu-id="29fab-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29fab-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29fab-138">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="29fab-138">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="29fab-139">searchInfo</span><span class="sxs-lookup"><span data-stu-id="29fab-139">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="29fab-140">labelInfo</span><span class="sxs-lookup"><span data-stu-id="29fab-140">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="29fab-141">Requerida</span><span class="sxs-lookup"><span data-stu-id="29fab-141">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="29fab-142">displayInfo</span><span class="sxs-lookup"><span data-stu-id="29fab-142">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="29fab-143">stringFormat</span><span class="sxs-lookup"><span data-stu-id="29fab-143">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="29fab-144">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="29fab-144">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="29fab-145">Numérico</span><span class="sxs-lookup"><span data-stu-id="29fab-145">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="29fab-146">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="29fab-146">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="29fab-147">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="29fab-147">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="29fab-148">drawControl</span><span class="sxs-lookup"><span data-stu-id="29fab-148">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="29fab-149">editControl</span><span class="sxs-lookup"><span data-stu-id="29fab-149">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="29fab-150">filterControl</span><span class="sxs-lookup"><span data-stu-id="29fab-150">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="29fab-151">Consulta</span><span class="sxs-lookup"><span data-stu-id="29fab-151">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
