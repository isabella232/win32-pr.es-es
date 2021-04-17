---
description: La propiedad UPGRADINGPRODUCTCODE se establece mediante Windows Installer cuando una actualización quita una aplicación.
ms.assetid: 903e4c22-e7ae-47bd-989b-d8c922de8d1a
title: Propiedad UPGRADINGPRODUCTCODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a256ade7f03275752ad4d176e64cd9d0fa12ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653629"
---
# <a name="upgradingproductcode-property"></a><span data-ttu-id="36853-103">Propiedad UPGRADINGPRODUCTCODE</span><span class="sxs-lookup"><span data-stu-id="36853-103">UPGRADINGPRODUCTCODE property</span></span>

<span data-ttu-id="36853-104">La propiedad **UPGRADINGPRODUCTCODE** se establece mediante Windows Installer cuando una actualización quita una aplicación.</span><span class="sxs-lookup"><span data-stu-id="36853-104">The **UPGRADINGPRODUCTCODE** property is set by Windows Installer when an upgrade removes an application.</span></span> <span data-ttu-id="36853-105">El instalador establece esta propiedad cuando ejecuta la [acción RemoveExistingProducts](removeexistingproducts-action.md).</span><span class="sxs-lookup"><span data-stu-id="36853-105">The installer sets this property when it runs the [RemoveExistingProducts action](removeexistingproducts-action.md).</span></span> <span data-ttu-id="36853-106">Esta propiedad no se establece quitando una aplicación mediante agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="36853-106">This property is not set by removing an application using the Add or Remove Programs in Control Panel.</span></span> <span data-ttu-id="36853-107">Una aplicación determina si se va a quitar mediante una actualización o agregar o quitar programas comprobando **UPGRADINGPRODUCTCODE**.</span><span class="sxs-lookup"><span data-stu-id="36853-107">An application determines whether it is being removed by an upgrade or the Add or Remove Programs by checking **UPGRADINGPRODUCTCODE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36853-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36853-108">Requirements</span></span>



| <span data-ttu-id="36853-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="36853-109">Requirement</span></span> | <span data-ttu-id="36853-110">Value</span><span class="sxs-lookup"><span data-stu-id="36853-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36853-111">Versión</span><span class="sxs-lookup"><span data-stu-id="36853-111">Version</span></span><br/> | <span data-ttu-id="36853-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="36853-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="36853-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36853-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="36853-114">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="36853-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="36853-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="36853-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36853-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="36853-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36853-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36853-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




