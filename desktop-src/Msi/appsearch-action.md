---
description: La acción AppSearch usa firmas de archivo para buscar versiones existentes de los productos.
ms.assetid: 56665876-2c74-476b-aa1a-158c6e86418d
title: Acción AppSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04187fb146af80839e135c99986dea1902ccb6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276524"
---
# <a name="appsearch-action"></a><span data-ttu-id="cdd24-103">Acción AppSearch</span><span class="sxs-lookup"><span data-stu-id="cdd24-103">AppSearch Action</span></span>

<span data-ttu-id="cdd24-104">La acción AppSearch usa firmas de archivo para buscar versiones existentes de los productos.</span><span class="sxs-lookup"><span data-stu-id="cdd24-104">The AppSearch action uses file signatures to search for existing versions of products.</span></span> <span data-ttu-id="cdd24-105">La acción AppSearch puede usar esta información para determinar dónde se instalarán las actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="cdd24-105">The AppSearch action may use this information to determine where upgrades are to be installed.</span></span> <span data-ttu-id="cdd24-106">La acción AppSearch también se puede usar para establecer una propiedad en el valor existente de una entrada del archivo Registry o. ini.</span><span class="sxs-lookup"><span data-stu-id="cdd24-106">The AppSearch action can also be used to set a property to the existing value of an registry or .ini file entry.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="cdd24-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="cdd24-107">Sequence Restrictions</span></span>

<span data-ttu-id="cdd24-108">AppSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="cdd24-108">AppSearch should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="cdd24-109">El instalador impide que la acción AppSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="cdd24-109">The installer prevents the AppSearch action from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="cdd24-110">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="cdd24-110">ActionData Messages</span></span>



| <span data-ttu-id="cdd24-111">Campo</span><span class="sxs-lookup"><span data-stu-id="cdd24-111">Field</span></span> | <span data-ttu-id="cdd24-112">Descripción de los datos de acción</span><span class="sxs-lookup"><span data-stu-id="cdd24-112">Description of action data</span></span>      |
|-------|---------------------------------|
| <span data-ttu-id="cdd24-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="cdd24-113">\[1\]</span></span> | <span data-ttu-id="cdd24-114">Propiedad que contiene la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="cdd24-114">Property holding file location.</span></span> |
| <span data-ttu-id="cdd24-115">\[2\]</span><span class="sxs-lookup"><span data-stu-id="cdd24-115">\[2\]</span></span> | <span data-ttu-id="cdd24-116">Firma de archivo.</span><span class="sxs-lookup"><span data-stu-id="cdd24-116">File signature.</span></span>                 |



 

## <a name="remarks"></a><span data-ttu-id="cdd24-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdd24-117">Remarks</span></span>

<span data-ttu-id="cdd24-118">La acción AppSearch requiere que la tabla de [firma](signature-table.md) esté presente en el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="cdd24-118">The AppSearch action requires that the [Signature](signature-table.md) table be present in the installation package.</span></span> <span data-ttu-id="cdd24-119">Las firmas de archivo se muestran en la tabla de firmas.</span><span class="sxs-lookup"><span data-stu-id="cdd24-119">File signatures are listed in the Signature table.</span></span> <span data-ttu-id="cdd24-120">Una firma que no está en la tabla de signatura denota un directorio y la acción establece la propiedad en la ruta de acceso del directorio para esa firma.</span><span class="sxs-lookup"><span data-stu-id="cdd24-120">A signature that is not in the Signature table denotes a directory and the action sets the property to the directory path for that signature.</span></span>

<span data-ttu-id="cdd24-121">La acción AppSearch busca firmas de archivo mediante la tabla [CompLocator](complocator-table.md) en primer lugar, la tabla [RegLocator](reglocator-table.md) siguiente, la tabla [IniLocator](inilocator-table.md) y, por último, la tabla [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cdd24-121">The AppSearch action searches for file signatures using the [CompLocator](complocator-table.md) table first, the [RegLocator](reglocator-table.md) table next, then the [IniLocator](inilocator-table.md) table, and finally the [DrLocator](drlocator-table.md) table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdd24-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdd24-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdd24-123">AppSearch</span><span class="sxs-lookup"><span data-stu-id="cdd24-123">AppSearch</span></span>](appsearch-table.md)
</dt> <dt>

[<span data-ttu-id="cdd24-124">CompLocator</span><span class="sxs-lookup"><span data-stu-id="cdd24-124">CompLocator</span></span>](complocator-table.md)
</dt> <dt>

[<span data-ttu-id="cdd24-125">IniLocator</span><span class="sxs-lookup"><span data-stu-id="cdd24-125">IniLocator</span></span>](inilocator-table.md)
</dt> <dt>

[<span data-ttu-id="cdd24-126">RegLocator</span><span class="sxs-lookup"><span data-stu-id="cdd24-126">RegLocator</span></span>](reglocator-table.md)
</dt> <dt>

[<span data-ttu-id="cdd24-127">DrLocator</span><span class="sxs-lookup"><span data-stu-id="cdd24-127">DrLocator</span></span>](drlocator-table.md)
</dt> </dl>

 

 



