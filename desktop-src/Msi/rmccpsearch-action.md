---
description: La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.
ms.assetid: d37b2434-86eb-4c6e-b817-77c75dcebbf5
title: Acción RMCCPSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c273ccb03bb77e0346edf73177d938d6002878a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677590"
---
# <a name="rmccpsearch-action"></a><span data-ttu-id="20c27-103">Acción RMCCPSearch</span><span class="sxs-lookup"><span data-stu-id="20c27-103">RMCCPSearch Action</span></span>

<span data-ttu-id="20c27-104">La acción RMCCPSearch usa firmas de archivo para validar que los productos aptos se instalan en un sistema antes de realizar una instalación de actualización.</span><span class="sxs-lookup"><span data-stu-id="20c27-104">The RMCCPSearch action uses file signatures to validate that qualifying products are installed on a system before an upgrade installation is performed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="20c27-105">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="20c27-105">Sequence Restrictions</span></span>

<span data-ttu-id="20c27-106">La acción RMCCPSearch debe crearse en la [tabla InstallUISequence](installuisequence-table.md) y en la [tabla InstallExecuteSequence](installexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="20c27-106">RMCCPSearch action should be authored into the [InstallUISequence table](installuisequence-table.md) and [InstallExecuteSequence table](installexecutesequence-table.md).</span></span> <span data-ttu-id="20c27-107">El instalador impide que RMCCPSearch se ejecute en la secuencia InstallExecuteSequence si la acción ya se ejecutó en la secuencia InstallUISequence.</span><span class="sxs-lookup"><span data-stu-id="20c27-107">The installer prevents RMCCPSearch from running in the InstallExecuteSequence sequence if the action has already run in InstallUISequence sequence.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="20c27-108">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="20c27-108">ActionData Messages</span></span>

<span data-ttu-id="20c27-109">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="20c27-109">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="20c27-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20c27-110">Remarks</span></span>

<span data-ttu-id="20c27-111">La acción RMCCPSearch requiere que la propiedad de la [**\_ unidad de CCP**](ccp-drive.md) se establezca en la ruta de acceso raíz en el [*volumen*](v-gly.md) extraíble que tiene la instalación de cualquiera de los productos calificados.</span><span class="sxs-lookup"><span data-stu-id="20c27-111">The RMCCPSearch action requires the [**CCP\_DRIVE**](ccp-drive.md) property to be set to the root path on the removable [*volume*](v-gly.md) that has the installation for any of the qualifying products.</span></span>

<span data-ttu-id="20c27-112">Cada firma de archivo de la tabla CCPSearch se busca en la ruta de acceso a la que se hace referencia en la propiedad de la [**\_ unidad de CCP**](ccp-drive.md) mediante la tabla [DrLocator](drlocator-table.md) .</span><span class="sxs-lookup"><span data-stu-id="20c27-112">Each file signature in the CCPSearch table is searched for under the path referred to by the [**CCP\_DRIVE**](ccp-drive.md) property using the [DrLocator](drlocator-table.md) table.</span></span> <span data-ttu-id="20c27-113">La ausencia de la firma de la tabla [Signature](signature-table.md) denota un directorio.</span><span class="sxs-lookup"><span data-stu-id="20c27-113">The absence of the signature from the [Signature](signature-table.md) table denotes a directory.</span></span> <span data-ttu-id="20c27-114">Si se determina que existe alguna firma, la acción RMCCPSearch finaliza.</span><span class="sxs-lookup"><span data-stu-id="20c27-114">If any signature is determined to exist, the RMCCPSearch action terminates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20c27-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20c27-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c27-116">Tabla CCPSearch</span><span class="sxs-lookup"><span data-stu-id="20c27-116">CCPSearch table</span></span>](ccpsearch-table.md)
</dt> </dl>

 

 



