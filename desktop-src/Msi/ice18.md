---
description: ICE18 valida que los directorios vacíos usados como una ruta de acceso de clave para un componente se muestran en la tabla CreateFolder.
ms.assetid: de31b893-831b-4a6d-809a-c4a3056b8a66
title: ICE18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60a3032a285604197e4c0bfda4225d519b0b744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666673"
---
# <a name="ice18"></a><span data-ttu-id="5612b-103">ICE18</span><span class="sxs-lookup"><span data-stu-id="5612b-103">ICE18</span></span>

<span data-ttu-id="5612b-104">ICE18 valida que los directorios vacíos usados como una ruta de acceso de clave para un componente se muestran en la [tabla CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-104">ICE18 validates that any empty directories used as a key path for a component are listed in the [CreateFolder table](createfolder-table.md).</span></span>

<span data-ttu-id="5612b-105">Si la columna de ruta de acceso de la [tabla de componentes](component-table.md) es null, significa que el directorio que aparece en la \_ columna directorio es la ruta de acceso de la clave de ese componente.</span><span class="sxs-lookup"><span data-stu-id="5612b-105">If the KeyPath column of the [Component table](component-table.md) is Null, this means that directory listed in the Directory\_ column is the key path for that component.</span></span> <span data-ttu-id="5612b-106">Dado que las carpetas creadas por el instalador se eliminan cuando se vacían, esta carpeta debe aparecer en la [tabla CreateFolder](createfolder-table.md) para evitar que el instalador intente instalarse cada vez.</span><span class="sxs-lookup"><span data-stu-id="5612b-106">Because folders created by the installer are deleted when they become empty, this folder must be listed in the [CreateFolder table](createfolder-table.md) to prevent the installer from attempting to install every time.</span></span>

<span data-ttu-id="5612b-107">No convierta el directorio Carpetadelsistema en la ruta de acceso de la clave de un componente.</span><span class="sxs-lookup"><span data-stu-id="5612b-107">Do not make the SystemFolder directory the key path of a component.</span></span> <span data-ttu-id="5612b-108">Dado que esta carpeta se encuentra en cada sistema operativo, el instalador detecta siempre la ruta de acceso de la clave tanto si el componente está presente como si no.</span><span class="sxs-lookup"><span data-stu-id="5612b-108">Because this folder is present on every operating system, the installer always detects the key path whether or not the component is present.</span></span> <span data-ttu-id="5612b-109">En este caso, la ruta de acceso de la clave debe ser un archivo, una entrada del registro o un origen de datos ODBC.</span><span class="sxs-lookup"><span data-stu-id="5612b-109">In this case, the key path should be a file, registry entry, or ODBC data source.</span></span>

<span data-ttu-id="5612b-110">Al realizar una validación, ICE18 comprueba en primer lugar si se cumplen todas las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="5612b-110">When performing a validation ICE18 first checks whether the following are all true:</span></span>

-   <span data-ttu-id="5612b-111">La columna de ruta de rutas de la [tabla de componentes](component-table.md) contiene un valor null.</span><span class="sxs-lookup"><span data-stu-id="5612b-111">The KeyPath column of the [Component table](component-table.md) contains a Null value.</span></span>
-   <span data-ttu-id="5612b-112">Que no hay ningún archivo en la lista para el componente en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-112">That there are no files listed for the component in the [File table](file-table.md).</span></span>
-   <span data-ttu-id="5612b-113">Que no hay archivos para el componente enumerado en la [tabla RemoveFile](removefile-table.md) y que el valor de DirProperty es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-113">That there are no files for the component listed in the [RemoveFile table](removefile-table.md) and that the value in the DirProperty is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="5612b-114">Que no hay archivos para el componente enumerado en la [tabla DuplicateFile](duplicatefile-table.md) y que el valor de DestFolder es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-114">That there are no files for the component listed in the [DuplicateFile table](duplicatefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="5612b-115">Que no hay archivos para el componente enumerado en la [tabla MoveFile](movefile-table.md) y que el valor de DestFolder es el mismo que el de la \_ columna de directorio de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-115">That there are no files for the component listed in the [MoveFile table](movefile-table.md) and that the value in the DestFolder is the same as the Directory\_ column of the [Component table](component-table.md).</span></span>

<span data-ttu-id="5612b-116">Si se cumplen todas las condiciones, ICE18 valida lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5612b-116">If these are all true then ICE18 validates the following:</span></span>

-   <span data-ttu-id="5612b-117">Que la \_ columna componente de la [tabla CreateFolder](createfolder-table.md) tenga el mismo valor que la columna componente de la [tabla componente](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-117">That the Component\_ column of the [CreateFolder table](createfolder-table.md) has the same value as the Component column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="5612b-118">Que la \_ columna directorio de la tabla CreateFolder tenga el mismo valor que la \_ columna directorio de la [tabla componente](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-118">That the Directory\_ column of the CreateFolder table has the same value as the Directory\_ column of the [Component table](component-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="5612b-119">Resultado</span><span class="sxs-lookup"><span data-stu-id="5612b-119">Result</span></span>

<span data-ttu-id="5612b-120">ICE18 envía un mensaje de error si el paquete de instalación especifica un directorio como la ruta de acceso de la clave del componente que no aparece en la [tabla CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="5612b-120">ICE18 posts an error message if the installation package specifies a directory as the key path for component that is not listed in the [CreateFolder table](createfolder-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5612b-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5612b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5612b-122">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="5612b-122">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



