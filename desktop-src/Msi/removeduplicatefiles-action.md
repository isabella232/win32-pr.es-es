---
description: La acción RemoveDuplicateFiles elimina los archivos instalados por la acción DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Acción RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809493"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="cc2c7-103">Acción RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="cc2c7-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="cc2c7-104">La acción RemoveDuplicateFiles elimina los archivos instalados por la acción [DuplicateFiles](duplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c7-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cc2c7-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="cc2c7-105">Sequence Restrictions</span></span>

<span data-ttu-id="cc2c7-106">La acción RemoveDuplicateFiles debe producirse después de la acción [InstallValidate](installvalidate-action.md) y antes de la acción [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="cc2c7-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cc2c7-107">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="cc2c7-107">ActionData Messages</span></span>



| <span data-ttu-id="cc2c7-108">Campo</span><span class="sxs-lookup"><span data-stu-id="cc2c7-108">Field</span></span> | <span data-ttu-id="cc2c7-109">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="cc2c7-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="cc2c7-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cc2c7-110">\[1\]</span></span> | <span data-ttu-id="cc2c7-111">Identificador del archivo quitado.</span><span class="sxs-lookup"><span data-stu-id="cc2c7-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="cc2c7-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="cc2c7-112">\[9\]</span></span> | <span data-ttu-id="cc2c7-113">Identificador del directorio que contiene el archivo quitado.</span><span class="sxs-lookup"><span data-stu-id="cc2c7-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cc2c7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc2c7-114">Remarks</span></span>

<span data-ttu-id="cc2c7-115">Para eliminar un archivo duplicado con la [acción DuplicateFiles](duplicatefiles-action.md) mediante la acción RemoveDuplicateFiles, se debe seleccionar el componente asociado a la entrada del archivo en la tabla DuplicateFile para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="cc2c7-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="cc2c7-116">Use la columna DestFolder de la [tabla DuplicateFile](duplicatefile-table.md) para especificar el nombre de la propiedad cuyo valor identifica la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="cc2c7-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



