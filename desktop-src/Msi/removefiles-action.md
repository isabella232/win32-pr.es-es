---
description: La acción RemoveFiles quita los archivos instalados previamente por la acción InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Acción RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667939"
---
# <a name="removefiles-action"></a><span data-ttu-id="bc370-103">Acción RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="bc370-103">RemoveFiles Action</span></span>

<span data-ttu-id="bc370-104">La acción RemoveFiles quita los archivos instalados previamente por la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bc370-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="bc370-105">Cada uno de estos archivos se valida mediante un vínculo a una entrada en la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bc370-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="bc370-106">Solo se quitarán los archivos con componentes que se resuelvan en el estado *msiInstallStateAbsent* o *msiInstallStateLocal* si el componente está instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="bc370-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bc370-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="bc370-107">Sequence Restrictions</span></span>

<span data-ttu-id="bc370-108">Se debe llamar a la acción [InstallValidate](installvalidate-action.md) antes de llamar a RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="bc370-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="bc370-109">Si se usa una acción [InstallFiles](installfiles-action.md) , debe aparecer después de RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="bc370-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bc370-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="bc370-110">ActionData Messages</span></span>



| <span data-ttu-id="bc370-111">Campo</span><span class="sxs-lookup"><span data-stu-id="bc370-111">Field</span></span> | <span data-ttu-id="bc370-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="bc370-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="bc370-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bc370-113">\[1\]</span></span> | <span data-ttu-id="bc370-114">Identificador del archivo quitado.</span><span class="sxs-lookup"><span data-stu-id="bc370-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="bc370-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="bc370-115">\[9\]</span></span> | <span data-ttu-id="bc370-116">Identificador del directorio que contiene el archivo quitado.</span><span class="sxs-lookup"><span data-stu-id="bc370-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bc370-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc370-117">Remarks</span></span>

<span data-ttu-id="bc370-118">La tabla [RemoveFile](removefile-table.md) se puede omitir en la base de datos del instalador si no hay archivos varios que quitar.</span><span class="sxs-lookup"><span data-stu-id="bc370-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="bc370-119">La acción RemoveFiles también puede quitar archivos especificados por el autor que no se instalan mediante la acción InstallFiles.</span><span class="sxs-lookup"><span data-stu-id="bc370-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="bc370-120">Estos archivos se especifican en la tabla [RemoveFile](removefile-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bc370-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="bc370-121">Cada uno de estos archivos se valida mediante un vínculo a una entrada en la tabla de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bc370-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="bc370-122">Los archivos cuyos componentes se resuelven en cualquier estado de acción activo (es decir, no en estado desactivado o nulo) se quitan si el archivo existe en el directorio especificado.</span><span class="sxs-lookup"><span data-stu-id="bc370-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="bc370-123">La eliminación de los archivos especificados en la tabla RemoveFile se intenta cuando el componente vinculado se instala por primera vez, durante una reinstalación y de nuevo cuando se quita el componente vinculado.</span><span class="sxs-lookup"><span data-stu-id="bc370-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="bc370-124">La acción RemoveFiles también puede quitar carpetas.</span><span class="sxs-lookup"><span data-stu-id="bc370-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="bc370-125">Si el valor de la columna FileName de la tabla RemoveFile es null, se quita una carpeta vacía.</span><span class="sxs-lookup"><span data-stu-id="bc370-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="bc370-126">Al quitar los archivos instalados anteriormente, la acción RemoveFiles consulta los mismos campos de las mismas tablas que los consultados por la acción [InstallFiles](installfiles-action.md) con la excepción de que la acción RemoveFiles no utiliza la [tabla de medios](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bc370-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="bc370-127">El nombre de archivo de destino se puede especificar en texto localizado en la columna FileName de la tabla RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="bc370-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



