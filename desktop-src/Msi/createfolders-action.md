---
description: La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Acción CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669927"
---
# <a name="createfolders-action"></a><span data-ttu-id="4df3a-103">Acción CreateFolders</span><span class="sxs-lookup"><span data-stu-id="4df3a-103">CreateFolders Action</span></span>

<span data-ttu-id="4df3a-104">La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse.</span><span class="sxs-lookup"><span data-stu-id="4df3a-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="4df3a-105">El instalador crea carpetas para los componentes que se ejecutan localmente y se ejecutan desde el origen.</span><span class="sxs-lookup"><span data-stu-id="4df3a-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="4df3a-106">Las carpetas recién creadas se registran con el identificador de componente adecuado.</span><span class="sxs-lookup"><span data-stu-id="4df3a-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="4df3a-107">La acción CreateFolders consulta la [tabla CreateFolder](createfolder-table.md) y la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="4df3a-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4df3a-108">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="4df3a-108">Sequence Restrictions</span></span>

<span data-ttu-id="4df3a-109">La acción CreateFolders se debe ejecutar antes de la acción [InstallFiles](installfiles-action.md) o antes de cualquier acción que agregue archivos a carpetas.</span><span class="sxs-lookup"><span data-stu-id="4df3a-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4df3a-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="4df3a-110">ActionData Messages</span></span>



| <span data-ttu-id="4df3a-111">Campo</span><span class="sxs-lookup"><span data-stu-id="4df3a-111">Field</span></span> | <span data-ttu-id="4df3a-112">Descripción de la descripción de los datos de la acción</span><span class="sxs-lookup"><span data-stu-id="4df3a-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="4df3a-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4df3a-113">\[1\]</span></span> | <span data-ttu-id="4df3a-114">Identificador de directorio de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="4df3a-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="4df3a-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4df3a-115">Remarks</span></span>

<span data-ttu-id="4df3a-116">El instalador no quita automáticamente las carpetas creadas por la acción CreateFolders durante la desinstalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="4df3a-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="4df3a-117">El instalador solo quita las carpetas si la [acción RemoveFolders](removefolders-action.md) se incluye en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="4df3a-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



