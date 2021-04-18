---
description: Establezca la propiedad MSIUSEREALADMINDETECTION en 1 para solicitar que el instalador use información de usuario real al establecer la propiedad AdminUser.
ms.assetid: eb0ed6e3-377b-40f4-afee-346a83e310cf
title: Propiedad MSIUSEREALADMINDETECTION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0989174f41bc4b58f89e440dd9852dfde6249a5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680789"
---
# <a name="msiuserealadmindetection-property"></a><span data-ttu-id="2f1d7-103">Propiedad MSIUSEREALADMINDETECTION</span><span class="sxs-lookup"><span data-stu-id="2f1d7-103">MSIUSEREALADMINDETECTION property</span></span>

<span data-ttu-id="2f1d7-104">Establezca la propiedad **MSIUSEREALADMINDETECTION** en 1 para solicitar que el instalador use información de usuario real al establecer la propiedad [**AdminUser**](adminuser.md) .</span><span class="sxs-lookup"><span data-stu-id="2f1d7-104">Set the **MSIUSEREALADMINDETECTION** property to 1 to request that the installer use actual user information when setting the [**AdminUser**](adminuser.md) property.</span></span> <span data-ttu-id="2f1d7-105">Cuando se ejecuta en Windows Vista, [**privileged**](privileged.md) y **AdminUser** son los mismos.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-105">When running on Windows Vista, the [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="2f1d7-106">Los autores deben usar la propiedad **privileged** en los nuevos paquetes.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-106">Authors should used the **Privileged** property in new packages.</span></span> <span data-ttu-id="2f1d7-107">Los paquetes heredados que requieren distintas propiedades **privileged** y **AdminUser** pueden restaurar la diferencia estableciendo la propiedad **MSIUSEREALADMINDETECTION** .</span><span class="sxs-lookup"><span data-stu-id="2f1d7-107">Legacy packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the **MSIUSEREALADMINDETECTION** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1d7-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f1d7-108">Requirements</span></span>



| <span data-ttu-id="2f1d7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f1d7-109">Requirement</span></span> | <span data-ttu-id="2f1d7-110">Value</span><span class="sxs-lookup"><span data-stu-id="2f1d7-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1d7-111">Versión</span><span class="sxs-lookup"><span data-stu-id="2f1d7-111">Version</span></span><br/> | <span data-ttu-id="2f1d7-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2f1d7-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2f1d7-114">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2f1d7-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f1d7-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f1d7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f1d7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2f1d7-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="2f1d7-117">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="2f1d7-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




