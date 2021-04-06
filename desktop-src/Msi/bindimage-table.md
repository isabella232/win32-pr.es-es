---
description: La tabla BindImage contiene información sobre cada archivo ejecutable o DLL que debe estar enlazado a los archivos dll importados por él.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: Tabla BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001716"
---
# <a name="bindimage-table"></a><span data-ttu-id="2f22b-103">Tabla BindImage</span><span class="sxs-lookup"><span data-stu-id="2f22b-103">BindImage Table</span></span>

<span data-ttu-id="2f22b-104">La tabla BindImage contiene información sobre cada archivo ejecutable o DLL que debe estar enlazado a los archivos dll importados por él.</span><span class="sxs-lookup"><span data-stu-id="2f22b-104">The BindImage table contains information about each executable or DLL that needs to be bound to the DLLs imported by it.</span></span>

<span data-ttu-id="2f22b-105">La tabla BindImage tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="2f22b-105">The BindImage table has the following columns.</span></span>



| <span data-ttu-id="2f22b-106">Columna</span><span class="sxs-lookup"><span data-stu-id="2f22b-106">Column</span></span> | <span data-ttu-id="2f22b-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="2f22b-107">Type</span></span>                         | <span data-ttu-id="2f22b-108">Clave</span><span class="sxs-lookup"><span data-stu-id="2f22b-108">Key</span></span> | <span data-ttu-id="2f22b-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="2f22b-109">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="2f22b-110">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="2f22b-110">File\_</span></span> | [<span data-ttu-id="2f22b-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="2f22b-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="2f22b-112">Y</span><span class="sxs-lookup"><span data-stu-id="2f22b-112">Y</span></span>   | <span data-ttu-id="2f22b-113">N</span><span class="sxs-lookup"><span data-stu-id="2f22b-113">N</span></span>        |
| <span data-ttu-id="2f22b-114">Ruta</span><span class="sxs-lookup"><span data-stu-id="2f22b-114">Path</span></span>   | [<span data-ttu-id="2f22b-115">Paths</span><span class="sxs-lookup"><span data-stu-id="2f22b-115">Paths</span></span>](paths.md)           | <span data-ttu-id="2f22b-116">N</span><span class="sxs-lookup"><span data-stu-id="2f22b-116">N</span></span>   | <span data-ttu-id="2f22b-117">Y</span><span class="sxs-lookup"><span data-stu-id="2f22b-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="2f22b-118">Columnas</span><span class="sxs-lookup"><span data-stu-id="2f22b-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="2f22b-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Filesystem\_</span><span class="sxs-lookup"><span data-stu-id="2f22b-119"><span id="File_"></span><span id="file_"></span><span id="FILE_"></span>File\_</span></span>
</dt> <dd>

<span data-ttu-id="2f22b-120">Una clave externa para la columna uno de la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="2f22b-120">An external key to column one of the [File table](file-table.md).</span></span> <span data-ttu-id="2f22b-121">Debe ser un archivo ejecutable o un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2f22b-121">This must be an executable file or a DLL file.</span></span>

</dd> <dt>

<span data-ttu-id="2f22b-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Camino</span><span class="sxs-lookup"><span data-stu-id="2f22b-122"><span id="Path"></span><span id="path"></span><span id="PATH"></span>Path</span></span>
</dt> <dd>

<span data-ttu-id="2f22b-123">Una lista de rutas de acceso, separadas por punto y coma, que representan las rutas de acceso en las que se van a buscar los archivos dll importados.</span><span class="sxs-lookup"><span data-stu-id="2f22b-123">A list of paths, separated by semicolons, that represent the paths to be searched to find the imported DLLs.</span></span> <span data-ttu-id="2f22b-124">La lista suele ser una lista de propiedades, con cada propiedad entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="2f22b-124">The list is usually a list of properties, with each property enclosed inside square brackets (\[ \]) .</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f22b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f22b-125">Remarks</span></span>

<span data-ttu-id="2f22b-126">El instalador calcula la dirección virtual de cada una de las funciones que se importan desde todos los archivos dll, y la dirección virtual calculada se guarda en la tabla de direcciones de importación (IAT) de la imagen de importación.</span><span class="sxs-lookup"><span data-stu-id="2f22b-126">The installer computes the virtual address of each function that is imported from all DLLs, and the computed virtual address is then saved in the importing image's Import Address Table (IAT).</span></span>

<span data-ttu-id="2f22b-127">Se hace referencia a esta tabla cuando se ejecuta la [acción BindImage](bindimage-action.md) .</span><span class="sxs-lookup"><span data-stu-id="2f22b-127">This table is referred to when the [BindImage action](bindimage-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="2f22b-128">Validación</span><span class="sxs-lookup"><span data-stu-id="2f22b-128">Validation</span></span>

<dl>

[<span data-ttu-id="2f22b-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="2f22b-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="2f22b-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="2f22b-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="2f22b-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="2f22b-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="2f22b-132">ICE46</span><span class="sxs-lookup"><span data-stu-id="2f22b-132">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="2f22b-133">ICE76</span><span class="sxs-lookup"><span data-stu-id="2f22b-133">ICE76</span></span>](ice76.md)  
</dl>

 

 



