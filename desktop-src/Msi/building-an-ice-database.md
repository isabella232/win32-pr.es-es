---
description: Después de seleccionar el ICEs apropiado para la validación, el desarrollador debe recopilar las acciones personalizadas en una base de datos de ICE.
ms.assetid: 69151d5a-be6e-4947-862d-cea65306c536
title: Creación de una base de datos ICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f51043aa9b3c1591fa3262492c117aba35f23d92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909045"
---
# <a name="building-an-ice-database"></a><span data-ttu-id="b0779-103">Creación de una base de datos ICE</span><span class="sxs-lookup"><span data-stu-id="b0779-103">Building an ICE Database</span></span>

<span data-ttu-id="b0779-104">Después de seleccionar el [ICEs](internal-consistency-evaluators-ices.md) apropiado para la validación, el desarrollador debe recopilar las acciones personalizadas en una base de datos de ICE.</span><span class="sxs-lookup"><span data-stu-id="b0779-104">After selecting the appropriate [ICEs](internal-consistency-evaluators-ices.md) for validation, a developer must collect the custom actions together into an ICE database.</span></span> <span data-ttu-id="b0779-105">Un archivo. Cub es una base de datos. msi estándar que solo contiene CIEM y las tablas necesarias.</span><span class="sxs-lookup"><span data-stu-id="b0779-105">A .cub file is a standard .msi database that contains only ICEs and their required tables.</span></span> <span data-ttu-id="b0779-106">No se puede instalar un archivo. Cub y solo se usa para almacenar y proporcionar acceso a las acciones personalizadas de ICE.</span><span class="sxs-lookup"><span data-stu-id="b0779-106">A .cub file cannot be installed and is used only to store and provide access to ICE custom actions.</span></span>

<span data-ttu-id="b0779-107">Un archivo. Cub contiene las siguientes tablas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b0779-107">A .cub file contains the following database tables.</span></span>



| <span data-ttu-id="b0779-108">Tabla</span><span class="sxs-lookup"><span data-stu-id="b0779-108">Table</span></span>                                  | <span data-ttu-id="b0779-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0779-109">Description</span></span>                                                                                                                                                                                                                                                                |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0779-110">Binario</span><span class="sxs-lookup"><span data-stu-id="b0779-110">Binary</span></span>](binary-table.md)             | <span data-ttu-id="b0779-111">Archivos de script, dll y exe de las acciones de la aduana de hielo a las que se hace referencia en la tabla CustomAction.</span><span class="sxs-lookup"><span data-stu-id="b0779-111">The script files, DLLs, and EXEs of the ICE customs actions that are referenced in the CustomAction table.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="b0779-112">CustomAction</span><span class="sxs-lookup"><span data-stu-id="b0779-112">CustomAction</span></span>](customaction-table.md) | <span data-ttu-id="b0779-113">Cada registro de esta tabla corresponde a una acción personalizada ICE incluida en el archivo. Cub.</span><span class="sxs-lookup"><span data-stu-id="b0779-113">Each record in this table corresponds to an ICE custom action included in the .cub file.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="b0779-114">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="b0779-114">\_ICESequence</span></span>                          | <span data-ttu-id="b0779-115">En esta tabla se enumeran las acciones de hielo que se incluyen en el archivo. Cub en su secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b0779-115">This table lists the ICE customs actions included in the .cub file in their execution sequence.</span></span> <span data-ttu-id="b0779-116">Las acciones personalizadas de ICE enumeradas en esta tabla se ejecutan llamando a [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), o bien se ejecutan de forma individual con [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span><span class="sxs-lookup"><span data-stu-id="b0779-116">The ICE custom actions listed in this table are executed by calling [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea), or individually executed using [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona).</span></span> |
| [<span data-ttu-id="b0779-117">\_Validación</span><span class="sxs-lookup"><span data-stu-id="b0779-117">\_Validation</span></span>](-validation-table.md)  | <span data-ttu-id="b0779-118">Esta tabla contiene las entradas de archivo. Cub que se van a combinar en la \_ tabla de validación.</span><span class="sxs-lookup"><span data-stu-id="b0779-118">This table contains the .cub file entries that are to be merged into the \_Validation table.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="b0779-119">\_Especial</span><span class="sxs-lookup"><span data-stu-id="b0779-119">\_Special</span></span>                              | <span data-ttu-id="b0779-120">Todas las tablas de procesamiento especiales requeridas por acciones personalizadas específicas de ICE deben incluirse en el archivo. Cub.</span><span class="sxs-lookup"><span data-stu-id="b0779-120">Any special processing tables required by particular ICE custom actions must be included in the .cub file.</span></span> <span data-ttu-id="b0779-121">El nombre de estas tablas debe tener un carácter de subrayado inicial.</span><span class="sxs-lookup"><span data-stu-id="b0779-121">The name of these tables must have a leading underscore.</span></span>                                                                                                        |



 

<span data-ttu-id="b0779-122">Vea el [archivo Sample. Cub](sample--cub-file.md).</span><span class="sxs-lookup"><span data-stu-id="b0779-122">See [Sample .cub File](sample--cub-file.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0779-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b0779-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0779-124">Creación de un ICE</span><span class="sxs-lookup"><span data-stu-id="b0779-124">Building An ICE</span></span>](building-an-ice.md)
</dt> </dl>

 

 



