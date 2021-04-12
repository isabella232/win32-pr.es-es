---
description: Esta tabla contiene los archivos de icono. Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se va a usar para los accesos directos anunciados y los servidores OLE. Vea limitaciones de OLE en secuencias.
ms.assetid: a59c552a-21c0-4dd4-9146-88a5f9a22962
title: Tabla de iconos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8e8e38575dc6f6e6bda10b2c1047f3940f7559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276507"
---
# <a name="icon-table"></a><span data-ttu-id="06c14-105">Tabla de iconos</span><span class="sxs-lookup"><span data-stu-id="06c14-105">Icon Table</span></span>

<span data-ttu-id="06c14-106">Esta tabla contiene los archivos de icono.</span><span class="sxs-lookup"><span data-stu-id="06c14-106">This table contains the icon files.</span></span> <span data-ttu-id="06c14-107">Cada icono de la tabla se copia en un archivo como parte del anuncio del producto que se va a usar para los accesos directos anunciados y los servidores OLE.</span><span class="sxs-lookup"><span data-stu-id="06c14-107">Each icon from the table is copied to a file as a part of product advertisement to be used for advertised shortcuts and OLE servers.</span></span> <span data-ttu-id="06c14-108">Vea [limitaciones de OLE en secuencias](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="06c14-108">See [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span>

<span data-ttu-id="06c14-109">La tabla de iconos tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="06c14-109">The Icon table has the following columns.</span></span>



| <span data-ttu-id="06c14-110">Columna</span><span class="sxs-lookup"><span data-stu-id="06c14-110">Column</span></span> | <span data-ttu-id="06c14-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="06c14-111">Type</span></span>                         | <span data-ttu-id="06c14-112">Clave</span><span class="sxs-lookup"><span data-stu-id="06c14-112">Key</span></span> | <span data-ttu-id="06c14-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="06c14-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="06c14-114">Nombre</span><span class="sxs-lookup"><span data-stu-id="06c14-114">Name</span></span>   | [<span data-ttu-id="06c14-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="06c14-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="06c14-116">Y</span><span class="sxs-lookup"><span data-stu-id="06c14-116">Y</span></span>   | <span data-ttu-id="06c14-117">N</span><span class="sxs-lookup"><span data-stu-id="06c14-117">N</span></span>        |
| <span data-ttu-id="06c14-118">Datos</span><span class="sxs-lookup"><span data-stu-id="06c14-118">Data</span></span>   | [<span data-ttu-id="06c14-119">Binario</span><span class="sxs-lookup"><span data-stu-id="06c14-119">Binary</span></span>](binary.md)         | <span data-ttu-id="06c14-120">N</span><span class="sxs-lookup"><span data-stu-id="06c14-120">N</span></span>   | <span data-ttu-id="06c14-121">N</span><span class="sxs-lookup"><span data-stu-id="06c14-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="06c14-122">Columnas</span><span class="sxs-lookup"><span data-stu-id="06c14-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="06c14-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="06c14-123"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="06c14-124">Nombre del archivo de icono.</span><span class="sxs-lookup"><span data-stu-id="06c14-124">Name of the icon file.</span></span>

</dd> <dt>

<span data-ttu-id="06c14-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span><span class="sxs-lookup"><span data-stu-id="06c14-125"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="06c14-126">Los datos del icono binario en formato PE (. dll o. exe) o de icono (. ico).</span><span class="sxs-lookup"><span data-stu-id="06c14-126">The binary icon data in PE (.dll or .exe) or icon (.ico) format.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06c14-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06c14-127">Remarks</span></span>

<span data-ttu-id="06c14-128">Se hace referencia a esta tabla cuando se ejecuta la [acción PublishProduct](publishproduct-action.md) .</span><span class="sxs-lookup"><span data-stu-id="06c14-128">This table is referred to when the [PublishProduct action](publishproduct-action.md) is executed.</span></span>

<span data-ttu-id="06c14-129">Los iconos para los accesos directos, las extensiones de nombre de archivo y los CLSID deben almacenarse en archivos que sean independientes del propio archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="06c14-129">The icons for shortcuts, file name extensions, and CLSIDs must be stored in files that are separate from the target file itself.</span></span> <span data-ttu-id="06c14-130">Esto es necesario porque el instalador solo debe copiar los archivos de iconos pequeños en el equipo del usuario al anunciar el recurso.</span><span class="sxs-lookup"><span data-stu-id="06c14-130">This is required because the installer should copy only the small icon files to the user's machine when advertising the resource.</span></span> <span data-ttu-id="06c14-131">Por lo tanto, un desarrollador de un paquete de instalación debe crear archivos independientes que contengan solo los iconos.</span><span class="sxs-lookup"><span data-stu-id="06c14-131">A developer of an installation package therefore needs to author separate files containing only the icons.</span></span> <span data-ttu-id="06c14-132">Estos archivos de icono se almacenan después como datos binarios en la tabla de iconos.</span><span class="sxs-lookup"><span data-stu-id="06c14-132">These icon files are then stored as binary data in the Icon table.</span></span>

<span data-ttu-id="06c14-133">Los archivos de icono que están asociados estrictamente con extensiones de nombre de archivo o CLSID pueden tener cualquier extensión, como. ico.</span><span class="sxs-lookup"><span data-stu-id="06c14-133">Icon files that are associated strictly with file name extensions or CLSIDs can have any extension, such as .ico.</span></span> <span data-ttu-id="06c14-134">Sin embargo, los archivos de icono que están asociados con accesos directos deben tener el formato binario EXE y deben tener un nombre que coincida con la extensión del destino.</span><span class="sxs-lookup"><span data-stu-id="06c14-134">However, Icon files that are associated with shortcuts must be in the EXE binary format and must be named such that their extension matches the extension of the target.</span></span> <span data-ttu-id="06c14-135">El acceso directo no funcionará si no se sigue esta regla.</span><span class="sxs-lookup"><span data-stu-id="06c14-135">The shortcut will not work if this rule is not followed.</span></span> <span data-ttu-id="06c14-136">Por ejemplo, si un acceso directo va a apuntar a un recurso que tiene el archivo de clave Red.bar, el archivo de icono también debe tener la extensión. bar.</span><span class="sxs-lookup"><span data-stu-id="06c14-136">For example, if a shortcut is to point to a resource having the key file Red.bar, then the icon file must also have the extension .bar.</span></span> <span data-ttu-id="06c14-137">Puede haber varios iconos en el mismo archivo de icono, siempre que todos los archivos de destino tengan la misma extensión.</span><span class="sxs-lookup"><span data-stu-id="06c14-137">Multiple icons can be stuffed into the same icon file as long as all of the target files have the same extension.</span></span>

## <a name="validation"></a><span data-ttu-id="06c14-138">Validación</span><span class="sxs-lookup"><span data-stu-id="06c14-138">Validation</span></span>

<dl>

[<span data-ttu-id="06c14-139">ICE03</span><span class="sxs-lookup"><span data-stu-id="06c14-139">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="06c14-140">ICE06</span><span class="sxs-lookup"><span data-stu-id="06c14-140">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="06c14-141">ICE29</span><span class="sxs-lookup"><span data-stu-id="06c14-141">ICE29</span></span>](ice29.md)  
[<span data-ttu-id="06c14-142">ICE32</span><span class="sxs-lookup"><span data-stu-id="06c14-142">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="06c14-143">ICE36</span><span class="sxs-lookup"><span data-stu-id="06c14-143">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="06c14-144">ICE50</span><span class="sxs-lookup"><span data-stu-id="06c14-144">ICE50</span></span>](ice50.md)  
</dl>

 

 



