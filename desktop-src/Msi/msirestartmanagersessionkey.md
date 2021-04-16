---
description: El instalador establece el valor de la propiedad MsiRestartManagerSessionKey en la clave de sesión para la sesión del administrador de reinicio.
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: Propiedad MsiRestartManagerSessionKey
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671373"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="8a44b-103">Propiedad MsiRestartManagerSessionKey</span><span class="sxs-lookup"><span data-stu-id="8a44b-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="8a44b-104">El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** en la clave de sesión para la sesión del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8a44b-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="8a44b-105">Las acciones personalizadas pueden usar la clave de sesión para unirse a la sesión del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8a44b-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a44b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8a44b-106">Remarks</span></span>

<span data-ttu-id="8a44b-107">El instalador establece el valor de la propiedad **MsiRestartManagerSessionKey** en la inicialización y, a continuación, borra el valor durante la acción [InstallValidate](installvalidate-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8a44b-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="8a44b-108">Las acciones personalizadas que necesitan el valor de la propiedad **MsiRestartManagerSessionKey** deben ir antes de la acción InstallValidate en la secuencia de acción.</span><span class="sxs-lookup"><span data-stu-id="8a44b-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a44b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a44b-109">Requirements</span></span>



| <span data-ttu-id="8a44b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a44b-110">Requirement</span></span> | <span data-ttu-id="8a44b-111">Value</span><span class="sxs-lookup"><span data-stu-id="8a44b-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a44b-112">Versión</span><span class="sxs-lookup"><span data-stu-id="8a44b-112">Version</span></span><br/> | <span data-ttu-id="8a44b-113">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8a44b-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8a44b-114">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8a44b-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8a44b-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima requerida por una versión de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8a44b-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a44b-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8a44b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a44b-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a44b-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8a44b-118">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="8a44b-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
