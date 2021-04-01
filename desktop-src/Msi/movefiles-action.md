---
description: La acción MoveFiles busca los archivos existentes en el equipo del usuario y mueve o copia esos archivos en una nueva ubicación.
ms.assetid: f08f751d-877b-4b17-8015-7108d5fd8195
title: Acción MoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06db0cef12753652bf94bf05875b2c2f9d4067c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913482"
---
# <a name="movefiles-action"></a><span data-ttu-id="75dfc-103">Acción MoveFiles</span><span class="sxs-lookup"><span data-stu-id="75dfc-103">MoveFiles Action</span></span>

<span data-ttu-id="75dfc-104">La acción MoveFiles busca los archivos existentes en el equipo del usuario y mueve o copia esos archivos en una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="75dfc-104">The MoveFiles action locates existing files on the user's computer and moves or copies those files to a new location.</span></span> <span data-ttu-id="75dfc-105">La acción MoveFiles consulta la [tabla MoveFile](movefile-table.md) y mueve los archivos especificados allí si el componente vinculado a las entradas se especifica para que se instale localmente o se ejecute desde el origen.</span><span class="sxs-lookup"><span data-stu-id="75dfc-105">The MoveFiles action queries the [MoveFile table](movefile-table.md) and moves files specified there if the component linked to the entries is specified to be install locally or is being run from source.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="75dfc-106">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="75dfc-106">Sequence Restrictions</span></span>

<span data-ttu-id="75dfc-107">La acción MoveFiles debe aparecer después de la acción [InstallValidate](installvalidate-action.md) y antes de la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="75dfc-107">The MoveFiles action must come after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="75dfc-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="75dfc-108">ActionData Messages</span></span>



| <span data-ttu-id="75dfc-109">Campo</span><span class="sxs-lookup"><span data-stu-id="75dfc-109">Field</span></span> | <span data-ttu-id="75dfc-110">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="75dfc-110">Description of action data</span></span>                  |
|-------|---------------------------------------------|
| <span data-ttu-id="75dfc-111">\[1\]</span><span class="sxs-lookup"><span data-stu-id="75dfc-111">\[1\]</span></span> | <span data-ttu-id="75dfc-112">Identificador del archivo que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="75dfc-112">Identifier of moved file.</span></span>                   |
| <span data-ttu-id="75dfc-113">\[6\]</span><span class="sxs-lookup"><span data-stu-id="75dfc-113">\[6\]</span></span> | <span data-ttu-id="75dfc-114">Tamaño del archivo instalado en bytes.</span><span class="sxs-lookup"><span data-stu-id="75dfc-114">Size of installed file in bytes.</span></span>            |
| <span data-ttu-id="75dfc-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="75dfc-115">\[9\]</span></span> | <span data-ttu-id="75dfc-116">Identificador del directorio que contiene el archivo que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="75dfc-116">Identifier of directory holding moved file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="75dfc-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75dfc-117">Remarks</span></span>

<span data-ttu-id="75dfc-118">La tabla MoveFiles contiene una columna denominada "Options" que especifica los archivos de origen que se van a copiar o copiar.</span><span class="sxs-lookup"><span data-stu-id="75dfc-118">The MoveFiles table contain a column named "options" which specifies the source files to be moved or copied.</span></span> <span data-ttu-id="75dfc-119">Un archivo de origen que se ha despasado se elimina una vez copiado en una nueva ubicación.</span><span class="sxs-lookup"><span data-stu-id="75dfc-119">A moved source file is deleted after it has been copied to a new location.</span></span> <span data-ttu-id="75dfc-120">Para ver la sintaxis exacta, vea la [tabla MoveFile](movefile-table.md).</span><span class="sxs-lookup"><span data-stu-id="75dfc-120">For the exact syntax, see the [MoveFile table](movefile-table.md).</span></span>

<span data-ttu-id="75dfc-121">Las columnas Carpetadeorigen y DestFolder de la tabla MoveFile son nombres de propiedad cuyos valores se espera que se resuelvan en rutas de acceso completas.</span><span class="sxs-lookup"><span data-stu-id="75dfc-121">The SourceFolder and DestFolder columns of the MoveFile table are property names whose values are expected to resolve to fully qualified paths.</span></span> <span data-ttu-id="75dfc-122">Estas propiedades pueden ser cualquiera de las entradas de directorio de la tabla de [directorio](directory-table.md) , cualquier propiedad de carpeta predefinida ([**FavoritesFolder**](favoritesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la tabla [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="75dfc-122">These properties can be any of the directory entries in the [Directory](directory-table.md) table, any predefined folder property ([**FavoritesFolder**](favoritesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="75dfc-123">Estas propiedades pueden contener una ruta de acceso completa que contenga el nombre de archivo a un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="75dfc-123">These properties may contain a full path containing the file name to a specific file.</span></span> <span data-ttu-id="75dfc-124">Por ejemplo, se puede crear la tabla AppSearch para buscar un archivo determinado y establecer una propiedad en la ruta de acceso completa a ese archivo.</span><span class="sxs-lookup"><span data-stu-id="75dfc-124">For example, the AppSearch table can be authored to search for a particular file and set a property to the full path to that file.</span></span> <span data-ttu-id="75dfc-125">En este ejemplo, la columna SourceName de la tabla MoveFile puede dejarse en blanco para indicar que el valor de la propiedad Carpetadeorigen contiene una ruta de acceso completa al archivo.</span><span class="sxs-lookup"><span data-stu-id="75dfc-125">In this example, the SourceName column in the MoveFile table can be left blank to indicate that the value in the SourceFolder property contains a full file path.</span></span> <span data-ttu-id="75dfc-126">El punto y coma es el delimitador de lista para las transformaciones, los orígenes y las revisiones, y no debe usarse en los nombres de archivo o rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="75dfc-126">The semicolon is the list delimiter for transforms, sources, and patches and should not be used in file names or paths.</span></span>

<span data-ttu-id="75dfc-127">La acción MoveFiles no actúa sobre las entradas de la tabla MoveFile en las que la propiedad Carpetadeorigen o DestFolder no se evalúa como una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="75dfc-127">The MoveFiles action does not act on entries in the MoveFile table in which either the SourceFolder or DestFolder property does not evaluate to a full path.</span></span>

<span data-ttu-id="75dfc-128">La acción MoveFiles intenta trasladar o copiar todos los archivos del directorio de origen que coinciden con el nombre dado en la columna SourceName de la tabla MoveFiles.</span><span class="sxs-lookup"><span data-stu-id="75dfc-128">The MoveFiles action attempts to move or copy all files in the source directory that match the name given in the SourceName column of the MoveFiles table.</span></span> <span data-ttu-id="75dfc-129">El nombre de la columna SourceName puede incluir \* o?</span><span class="sxs-lookup"><span data-stu-id="75dfc-129">The name in the SourceName column can include either the \* or ?</span></span> <span data-ttu-id="75dfc-130">caracteres comodín que permiten que un grupo de archivos se muevan o se copien.</span><span class="sxs-lookup"><span data-stu-id="75dfc-130">wildcards which allow a group of files to be moved or copied.</span></span> <span data-ttu-id="75dfc-131">Por ejemplo, la columna SourceName puede contener una entrada de " \* . xls" y la acción MoveFiles mueve o copia cada libro de Microsoft Excel del directorio de origen al de destino.</span><span class="sxs-lookup"><span data-stu-id="75dfc-131">For example, the SourceName column may contain an entry of "\*.xls" and the MoveFiles action moves or copies every Microsoft Excel workbook from the source directory to the destination.</span></span>

<span data-ttu-id="75dfc-132">El nombre que se va a asignar al archivo de destino se puede especificar en la columna DestName de la tabla MoveFile.</span><span class="sxs-lookup"><span data-stu-id="75dfc-132">The name to be given to the destination file can be specified in the DestName column of the MoveFile table.</span></span> <span data-ttu-id="75dfc-133">El nombre de archivo de destino conserva el nombre del archivo de código fuente si esta columna se deja en blanco.</span><span class="sxs-lookup"><span data-stu-id="75dfc-133">The destination file name retains the source file name if this column is left blank.</span></span>

<span data-ttu-id="75dfc-134">Si \* se escribe un carácter comodín "" en la columna SourceName de la [tabla MoveFile](movefile-table.md) y se especifica un nombre de archivo de destino en la columna DestName, todos los archivos que se han copiado o copiado conservan los nombres en los orígenes.</span><span class="sxs-lookup"><span data-stu-id="75dfc-134">If a "\*" wildcard is entered in the SourceName column of the [MoveFile table](movefile-table.md) and a destination file name is specified in the DestName column, all moved or copied files retain the names in the sources.</span></span>

<span data-ttu-id="75dfc-135">Los archivos que se mueven o copian mediante la acción MoveFiles no se eliminan cuando se desinstala el producto.</span><span class="sxs-lookup"><span data-stu-id="75dfc-135">Files that are moved or copied by the MoveFiles action are not deleted when the product is uninstalled.</span></span>

 

 



