---
description: La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la extensión o la información del servidor COM necesaria para el anuncio del contenido MIME (Extensiones multipropósito de correo Internet).
ms.assetid: 5d452b24-ae04-4c45-8b3b-48e81f13a21e
title: Tabla MIME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca11c8596e8f3735872c88668211953fc2b18b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278152"
---
# <a name="mime-table"></a><span data-ttu-id="44480-103">Tabla MIME</span><span class="sxs-lookup"><span data-stu-id="44480-103">MIME Table</span></span>

<span data-ttu-id="44480-104">La tabla MIME asocia un tipo de contenido MIME con una extensión de nombre de archivo o un CLSID para generar la extensión o la información del servidor COM necesaria para el anuncio del contenido MIME (Extensiones multipropósito de correo Internet).</span><span class="sxs-lookup"><span data-stu-id="44480-104">The MIME table associates a MIME content type with a file name extension or a CLSID to generate the extension or COM server information required for advertisement of the MIME (Multipurpose Internet Mail Extensions) content.</span></span>

<span data-ttu-id="44480-105">La tabla MIME tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="44480-105">The MIME table has the following columns.</span></span>



| <span data-ttu-id="44480-106">Columna</span><span class="sxs-lookup"><span data-stu-id="44480-106">Column</span></span>      | <span data-ttu-id="44480-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="44480-107">Type</span></span>             | <span data-ttu-id="44480-108">Clave</span><span class="sxs-lookup"><span data-stu-id="44480-108">Key</span></span> | <span data-ttu-id="44480-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="44480-109">Nullable</span></span> |
|-------------|------------------|-----|----------|
| <span data-ttu-id="44480-110">ContentType</span><span class="sxs-lookup"><span data-stu-id="44480-110">ContentType</span></span> | [<span data-ttu-id="44480-111">Texto</span><span class="sxs-lookup"><span data-stu-id="44480-111">Text</span></span>](text.md) | <span data-ttu-id="44480-112">Y</span><span class="sxs-lookup"><span data-stu-id="44480-112">Y</span></span>   | <span data-ttu-id="44480-113">N</span><span class="sxs-lookup"><span data-stu-id="44480-113">N</span></span>        |
| <span data-ttu-id="44480-114">Extensión\_</span><span class="sxs-lookup"><span data-stu-id="44480-114">Extension\_</span></span> | [<span data-ttu-id="44480-115">Texto</span><span class="sxs-lookup"><span data-stu-id="44480-115">Text</span></span>](text.md) | <span data-ttu-id="44480-116">N</span><span class="sxs-lookup"><span data-stu-id="44480-116">N</span></span>   | <span data-ttu-id="44480-117">N</span><span class="sxs-lookup"><span data-stu-id="44480-117">N</span></span>        |
| <span data-ttu-id="44480-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="44480-118">CLSID</span></span>       | [<span data-ttu-id="44480-119">GUID</span><span class="sxs-lookup"><span data-stu-id="44480-119">GUID</span></span>](guid.md) | <span data-ttu-id="44480-120">N</span><span class="sxs-lookup"><span data-stu-id="44480-120">N</span></span>   | <span data-ttu-id="44480-121">Y</span><span class="sxs-lookup"><span data-stu-id="44480-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="44480-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="44480-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="44480-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span><span class="sxs-lookup"><span data-stu-id="44480-123"><span id="ContentType"></span><span id="contenttype"></span><span id="CONTENTTYPE"></span>ContentType</span></span>
</dt> <dd>

<span data-ttu-id="44480-124">Esta columna es un identificador del contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="44480-124">This column is an identifier for the MIME content.</span></span> <span data-ttu-id="44480-125">Normalmente se escribe en forma de tipo/formato.</span><span class="sxs-lookup"><span data-stu-id="44480-125">It is commonly written in the form of type/format.</span></span>

</dd> <dt>

<span data-ttu-id="44480-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span><span class="sxs-lookup"><span data-stu-id="44480-126"><span id="Extension_"></span><span id="extension_"></span><span id="EXTENSION_"></span>Extension\_</span></span>
</dt> <dd>

<span data-ttu-id="44480-127">Esta columna contiene la extensión de servidor que se va a asociar al contenido MIME, sin el punto.</span><span class="sxs-lookup"><span data-stu-id="44480-127">This column contains the server extension that is to be associated with the MIME content, without the dot.</span></span> <span data-ttu-id="44480-128">Esta columna es una clave externa de la [tabla de extensión](extension-table.md).</span><span class="sxs-lookup"><span data-stu-id="44480-128">This column is a foreign key into the [Extension table](extension-table.md).</span></span> <span data-ttu-id="44480-129">La tabla de extensión contiene información del servidor de extensión de nombre de archivo que se usa como parte del anuncio.</span><span class="sxs-lookup"><span data-stu-id="44480-129">The Extension table contains file name extension server information which is used as a part of advertisement.</span></span>

</dd> <dt>

<span data-ttu-id="44480-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span><span class="sxs-lookup"><span data-stu-id="44480-130"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="44480-131">Esta columna contiene el CLSID del servidor COM que se va a asociar al contenido MIME.</span><span class="sxs-lookup"><span data-stu-id="44480-131">This column contains the COM server CLSID that is to be associated with the MIME content.</span></span> <span data-ttu-id="44480-132">El CLSID de esta columna puede ser una clave externa en la [tabla de clases](class-table.md) o puede ser un CLSID que ya existe en el equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="44480-132">The CLSID in this column can be a foreign key into the [Class table](class-table.md) or it can be a CLSID that already exists on the user's machine.</span></span> <span data-ttu-id="44480-133">La tabla de clases contiene información relacionada con el servidor COM que se utiliza como parte del anuncio.</span><span class="sxs-lookup"><span data-stu-id="44480-133">The Class table contains COM server-related information which is used as a part of advertisement.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44480-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44480-134">Remarks</span></span>

<span data-ttu-id="44480-135">Se hace referencia a esta tabla cuando se ejecuta la acción [RegisterMIMEInfo](registermimeinfo-action.md) o la [acción UnregisterMIMEInfo](unregistermimeinfo-action.md) .</span><span class="sxs-lookup"><span data-stu-id="44480-135">This table is referred to when the [RegisterMIMEInfo action](registermimeinfo-action.md) or the [UnregisterMIMEInfo action](unregistermimeinfo-action.md) is executed.</span></span> <span data-ttu-id="44480-136">En el modo de anuncio, la acción RegisterMIMEInfo registra toda la información MIME de los servidores de la tabla MIME para la que está habilitada la característica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="44480-136">In advertise mode, the RegisterMIMEInfo action registers all MIME information for servers from the MIME table for which the corresponding feature is enabled.</span></span> <span data-ttu-id="44480-137">De lo contrario, la acción registra la información MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente.</span><span class="sxs-lookup"><span data-stu-id="44480-137">Otherwise the action registers MIME information for servers from the MIME table for which the corresponding feature is currently selected to be installed.</span></span> <span data-ttu-id="44480-138">La [acción UnregisterMIMEInfo](unregistermimeinfo-action.md) anula el registro de la información del registro relacionada con MIME del sistema.</span><span class="sxs-lookup"><span data-stu-id="44480-138">The [UnregisterMIMEInfo action](unregistermimeinfo-action.md) unregisters MIME-related registry information from the system.</span></span> <span data-ttu-id="44480-139">La acción anula el registro de la información de MIME para los servidores de la tabla MIME para la que está seleccionada actualmente la característica correspondiente para desinstalarla.</span><span class="sxs-lookup"><span data-stu-id="44480-139">The action unregisters MIME information for servers from the MIME table for which the corresponding feature is currently selected to be uninstalled.</span></span>

## <a name="validation"></a><span data-ttu-id="44480-140">Validación</span><span class="sxs-lookup"><span data-stu-id="44480-140">Validation</span></span>

<dl>

[<span data-ttu-id="44480-141">ICE03</span><span class="sxs-lookup"><span data-stu-id="44480-141">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="44480-142">ICE06</span><span class="sxs-lookup"><span data-stu-id="44480-142">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="44480-143">ICE15</span><span class="sxs-lookup"><span data-stu-id="44480-143">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="44480-144">ICE32</span><span class="sxs-lookup"><span data-stu-id="44480-144">ICE32</span></span>](ice32.md)  
</dl>

 

 



