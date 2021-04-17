---
description: La propiedad UpgradeCode es un GUID que representa un conjunto de productos relacionado. El UpgradeCode se usa en la tabla de actualización para buscar las versiones relacionadas del producto que ya están instaladas. La acción RegisterProduct usa esta propiedad.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: Propiedad UpgradeCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653631"
---
# <a name="upgradecode-property"></a><span data-ttu-id="f2b2f-104">Propiedad UpgradeCode</span><span class="sxs-lookup"><span data-stu-id="f2b2f-104">UpgradeCode property</span></span>

<span data-ttu-id="f2b2f-105">La propiedad **UpgradeCode** es un GUID que representa un conjunto de productos relacionado.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="f2b2f-106">El **UpgradeCode** se usa en la [tabla de actualización](upgrade-table.md) para buscar las versiones relacionadas del producto que ya están instaladas.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="f2b2f-107">La [acción RegisterProduct](registerproduct-action.md)usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f2b2f-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2b2f-108">Remarks</span></span>

<span data-ttu-id="f2b2f-109">Se recomienda encarecidamente que los autores de los paquetes de instalación especifiquen **UpgradeCode** para su aplicación.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2b2f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2b2f-110">Requirements</span></span>



| <span data-ttu-id="f2b2f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2b2f-111">Requirement</span></span> | <span data-ttu-id="f2b2f-112">Value</span><span class="sxs-lookup"><span data-stu-id="f2b2f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b2f-113">Versión</span><span class="sxs-lookup"><span data-stu-id="f2b2f-113">Version</span></span><br/> | <span data-ttu-id="f2b2f-114">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f2b2f-115">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f2b2f-116">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f2b2f-117">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f2b2f-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f2b2f-118">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f2b2f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2b2f-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f2b2f-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="f2b2f-120">Revisiones y actualizaciones</span><span class="sxs-lookup"><span data-stu-id="f2b2f-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="f2b2f-121">Preparación de una aplicación para futuras actualizaciones principales</span><span class="sxs-lookup"><span data-stu-id="f2b2f-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




