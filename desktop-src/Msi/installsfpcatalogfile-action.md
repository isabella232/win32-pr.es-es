---
description: La acción InstallSFPCatalogFile instala los catálogos que usa Windows me para la protección de archivos de Windows.
ms.assetid: 1c8253f1-ac7d-4346-a16e-887d16f521d9
title: Acción InstallSFPCatalogFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc4192f8ee0062c51833292a98c28ea27c12531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686573"
---
# <a name="installsfpcatalogfile-action"></a><span data-ttu-id="8f31e-103">Acción InstallSFPCatalogFile</span><span class="sxs-lookup"><span data-stu-id="8f31e-103">InstallSFPCatalogFile Action</span></span>

<span data-ttu-id="8f31e-104">La acción InstallSFPCatalogFile instala los catálogos que usa Windows me para la protección de archivos de Windows.</span><span class="sxs-lookup"><span data-stu-id="8f31e-104">The InstallSFPCatalogFile action installs the catalogs used by Windows Me for Windows File Protection.</span></span> <span data-ttu-id="8f31e-105">InstallSFPCatalogFile consulta la tabla de [componentes](component-table.md), la [tabla de archivos](file-table.md), la tabla [FileSFPCatalog](filesfpcatalog-table.md) y la tabla [SFPCatalog](sfpcatalog-table.md).</span><span class="sxs-lookup"><span data-stu-id="8f31e-105">InstallSFPCatalogFile queries the [Component table](component-table.md), [File table](file-table.md), [FileSFPCatalog table](filesfpcatalog-table.md) and [SFPCatalog table](sfpcatalog-table.md).</span></span> <span data-ttu-id="8f31e-106">Los catálogos se instalan si están asociados a un archivo en un componente que se establece para la instalación local o si están asociados a un archivo que se va a reparar en un componente instalado localmente.</span><span class="sxs-lookup"><span data-stu-id="8f31e-106">Catalogs are installed if they are associated with a file in a component that is set for local installation or if they are associated with a file being repaired in a locally installed component.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="8f31e-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="8f31e-107">Sequence Restrictions</span></span>

<span data-ttu-id="8f31e-108">La acción InstallSFPCatalogFile se debe secuenciar antes de [InstallFiles](installfiles-action.md) y después de [CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="8f31e-108">The InstallSFPCatalogFile action must be sequenced before [InstallFiles](installfiles-action.md) and after [CostFinalize](costfinalize-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="8f31e-109">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="8f31e-109">ActionData Messages</span></span>



| <span data-ttu-id="8f31e-110">Campo</span><span class="sxs-lookup"><span data-stu-id="8f31e-110">Field</span></span> | <span data-ttu-id="8f31e-111">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="8f31e-111">Description of action data</span></span>                                    |
|-------|---------------------------------------------------------------|
| <span data-ttu-id="8f31e-112">\[1\]</span><span class="sxs-lookup"><span data-stu-id="8f31e-112">\[1\]</span></span> | <span data-ttu-id="8f31e-113">Nombre del catálogo que se va a instalar.</span><span class="sxs-lookup"><span data-stu-id="8f31e-113">Name of the catalog being installed.</span></span>                          |
| <span data-ttu-id="8f31e-114">\[2\]</span><span class="sxs-lookup"><span data-stu-id="8f31e-114">\[2\]</span></span> | <span data-ttu-id="8f31e-115">Nombre del catálogo del que depende esta instalación de este catálogo.</span><span class="sxs-lookup"><span data-stu-id="8f31e-115">Name of the catalog this catalog's installation depends upon.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8f31e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f31e-116">Remarks</span></span>

<span data-ttu-id="8f31e-117">Catálogo que depende de otro Catálogo instalado después del catálogo primario.</span><span class="sxs-lookup"><span data-stu-id="8f31e-117">A catalog that is dependent on another catalog installed after the parent catalog.</span></span>

 

 



