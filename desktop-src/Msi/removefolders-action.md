---
description: La acción RemoveFolders quita todas las carpetas vinculadas a los componentes que se van a quitar o ejecutar desde el origen. Estas carpetas se quitan solo si están vacías. Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Acción RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277741"
---
# <a name="removefolders-action"></a><span data-ttu-id="5f019-105">Acción RemoveFolders</span><span class="sxs-lookup"><span data-stu-id="5f019-105">RemoveFolders Action</span></span>

<span data-ttu-id="5f019-106">La acción RemoveFolders quita todas las carpetas vinculadas a los componentes que se van a quitar o ejecutar desde el origen.</span><span class="sxs-lookup"><span data-stu-id="5f019-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="5f019-107">Estas carpetas se quitan solo si están vacías.</span><span class="sxs-lookup"><span data-stu-id="5f019-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="5f019-108">Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.</span><span class="sxs-lookup"><span data-stu-id="5f019-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="5f019-109">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="5f019-109">Sequence Restrictions</span></span>

<span data-ttu-id="5f019-110">La acción RemoveFolders debe aparecer después de la acción [RemoveFiles](removefiles-action.md) o cualquier acción que pueda quitar archivos de las carpetas.</span><span class="sxs-lookup"><span data-stu-id="5f019-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="5f019-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="5f019-111">ActionData Messages</span></span>



| <span data-ttu-id="5f019-112">Campo</span><span class="sxs-lookup"><span data-stu-id="5f019-112">Field</span></span> | <span data-ttu-id="5f019-113">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="5f019-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="5f019-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="5f019-114">\[1\]</span></span> | <span data-ttu-id="5f019-115">Identificador de la carpeta quitada.</span><span class="sxs-lookup"><span data-stu-id="5f019-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5f019-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f019-116">Remarks</span></span>

<span data-ttu-id="5f019-117">El instalador no quita automáticamente las carpetas creadas por la [acción CreateFolders](createfolders-action.md) durante la desinstalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f019-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="5f019-118">Se debe indicar al instalador que quite estas carpetas mediante la creación de la acción RemoveFolders en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="5f019-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="5f019-119">Para especificar el nombre y la ubicación de la carpeta, utilice la \_ columna directorio de la [tabla CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f019-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="5f019-120">Se supone que cada nombre de carpeta de la tabla CreateFolder es una propiedad que define la ubicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5f019-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="5f019-121">Para especificar el componente propietario de la carpeta, utilice la columna ComponentId de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5f019-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



