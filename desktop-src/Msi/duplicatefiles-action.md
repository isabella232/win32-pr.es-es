---
description: La acción DuplicateFiles duplica los archivos instalados por la acción InstallFiles. Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.
ms.assetid: 51cc0b3f-aa01-4f4d-9a4d-add832698061
title: Acción DuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 711f6bbd4716beb227dea348826bc302e2f4ba2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652754"
---
# <a name="duplicatefiles-action"></a><span data-ttu-id="25c74-104">Acción DuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="25c74-104">DuplicateFiles Action</span></span>

<span data-ttu-id="25c74-105">La acción DuplicateFiles duplica los archivos instalados por la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="25c74-105">The DuplicateFiles action duplicates files installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="25c74-106">Los archivos duplicados se pueden copiar en el mismo directorio con un nombre diferente o en otro directorio con el nombre original.</span><span class="sxs-lookup"><span data-stu-id="25c74-106">The duplicate files can be copied to the same directory with a different name or to a different directory with the original name.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="25c74-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="25c74-107">Sequence Restrictions</span></span>

<span data-ttu-id="25c74-108">La acción DuplicateFiles debe aparecer después de la [acción InstallFiles](installfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="25c74-108">The DuplicateFiles action must come after the [InstallFiles action](installfiles-action.md).</span></span> <span data-ttu-id="25c74-109">La acción DuplicateFiles también debe aparecer después de la [acción PatchFiles](patchfiles-action.md) para evitar la duplicación de la versión no revisada del archivo.</span><span class="sxs-lookup"><span data-stu-id="25c74-109">The DuplicateFiles Action must also come after the [PatchFiles action](patchfiles-action.md) to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="25c74-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="25c74-110">ActionData Messages</span></span>



| <span data-ttu-id="25c74-111">Campo</span><span class="sxs-lookup"><span data-stu-id="25c74-111">Field</span></span> | <span data-ttu-id="25c74-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="25c74-112">Description of action data</span></span>                       |
|-------|--------------------------------------------------|
| <span data-ttu-id="25c74-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="25c74-113">\[1\]</span></span> | <span data-ttu-id="25c74-114">Identificador del archivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="25c74-114">Identifier of duplicated file.</span></span>                   |
| <span data-ttu-id="25c74-115">\[6\]</span><span class="sxs-lookup"><span data-stu-id="25c74-115">\[6\]</span></span> | <span data-ttu-id="25c74-116">Tamaño del archivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="25c74-116">Size of duplicated file.</span></span>                         |
| <span data-ttu-id="25c74-117">\[9\]</span><span class="sxs-lookup"><span data-stu-id="25c74-117">\[9\]</span></span> | <span data-ttu-id="25c74-118">Identificador del directorio que contiene el archivo duplicado.</span><span class="sxs-lookup"><span data-stu-id="25c74-118">Identifier of directory holding duplicated file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="25c74-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="25c74-119">Remarks</span></span>

<span data-ttu-id="25c74-120">La acción DuplicateFiles procesa una entrada de la [tabla DuplicateFile](duplicatefile-table.md) solo si el componente vinculado a esa entrada se está instalando localmente.</span><span class="sxs-lookup"><span data-stu-id="25c74-120">The DuplicateFiles action processes a [DuplicateFile table](duplicatefile-table.md) entry only if the component linked to that entry is being installed locally.</span></span> <span data-ttu-id="25c74-121">Para obtener más información, vea [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="25c74-121">For more information, see [Component table](component-table.md).</span></span>

<span data-ttu-id="25c74-122">La cadena en el campo DestFolder es un nombre de propiedad cuyo valor se espera que se resuelva como una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="25c74-122">The string in the DestFolder field is a property name whose value is expected to resolve to a fully qualified path.</span></span> <span data-ttu-id="25c74-123">Esta propiedad puede ser cualquiera de las entradas de directorio de la tabla de [directorio](directory-table.md) , cualquier propiedad de carpeta predefinida ([**CommonFilesFolder**](commonfilesfolder.md), por ejemplo) o una propiedad establecida por cualquier entrada de la tabla [AppSearch](appsearch-table.md) .</span><span class="sxs-lookup"><span data-stu-id="25c74-123">This property can either be any of the directory entries in the [Directory](directory-table.md) table, any pre-defined folder property ([**CommonFilesFolder**](commonfilesfolder.md), for example), or a property set by any entry in the [AppSearch](appsearch-table.md) table.</span></span> <span data-ttu-id="25c74-124">Si la propiedad **DestFolder** no se evalúa como una ruta de acceso válida, la acción DuplicateFiles no hace nada para esa entrada.</span><span class="sxs-lookup"><span data-stu-id="25c74-124">If the **DestFolder** property does not evaluate to a valid path the DuplicateFiles action does nothing for that entry.</span></span>

<span data-ttu-id="25c74-125">Si el nombre del archivo de destino en la columna DestName de la tabla DuplicateFile se deja en blanco, el nombre de archivo de destino será el mismo que el nombre de archivo original.</span><span class="sxs-lookup"><span data-stu-id="25c74-125">If the name of the destination file in the DestName column of the DuplicateFile table is left blank, the destination file name will be the same as the original file name.</span></span>

<span data-ttu-id="25c74-126">La acción [RemoveDuplicateFiles](removeduplicatefiles-action.md) quita los archivos instalados por la acción DuplicateFiles cuando corresponda.</span><span class="sxs-lookup"><span data-stu-id="25c74-126">Files installed by the DuplicateFiles action are removed by the [RemoveDuplicateFiles](removeduplicatefiles-action.md) action when appropriate.</span></span>

 

 



