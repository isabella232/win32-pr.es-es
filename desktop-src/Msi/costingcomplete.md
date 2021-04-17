---
description: La propiedad CostingComplete indica si el instalador ha completado el costo de espacio en disco.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propiedad CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653506"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="ce201-103">Propiedad CostingComplete</span><span class="sxs-lookup"><span data-stu-id="ce201-103">CostingComplete property</span></span>

<span data-ttu-id="ce201-104">La propiedad **CostingComplete** indica si el instalador ha completado el costo de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ce201-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="ce201-105">Esta propiedad se puede usar para crear un cuadro de diálogo desencadenado si no se ha completado el costo.</span><span class="sxs-lookup"><span data-stu-id="ce201-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="ce201-106">La propiedad se establece dinámicamente durante el costo del espacio en disco y se establece en 1 en cuanto se completa el costo.</span><span class="sxs-lookup"><span data-stu-id="ce201-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="ce201-107">La [acción CostFinalize](costfinalize-action.md)inicializa esta propiedad en 0.</span><span class="sxs-lookup"><span data-stu-id="ce201-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ce201-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ce201-108">Remarks</span></span>

<span data-ttu-id="ce201-109">Para obtener un ejemplo de cómo crear un "espere.</span><span class="sxs-lookup"><span data-stu-id="ce201-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="ce201-110">.</span><span class="sxs-lookup"><span data-stu-id="ce201-110">.</span></span> <span data-ttu-id="ce201-111">.</span><span class="sxs-lookup"><span data-stu-id="ce201-111">.</span></span> <span data-ttu-id="ce201-112">"cuadro de diálogo que aparece durante el costo de espacio en disco, consulte la sección [creación de una instrucción condicional" espere.... " Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md).</span><span class="sxs-lookup"><span data-stu-id="ce201-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ce201-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce201-113">Requirements</span></span>



| <span data-ttu-id="ce201-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce201-114">Requirement</span></span> | <span data-ttu-id="ce201-115">Value</span><span class="sxs-lookup"><span data-stu-id="ce201-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce201-116">Versión</span><span class="sxs-lookup"><span data-stu-id="ce201-116">Version</span></span><br/> | <span data-ttu-id="ce201-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ce201-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ce201-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ce201-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ce201-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ce201-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ce201-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ce201-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ce201-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ce201-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce201-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce201-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




