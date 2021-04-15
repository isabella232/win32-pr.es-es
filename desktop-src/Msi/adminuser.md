---
description: El instalador establece esta propiedad si el usuario tiene privilegios de administrador.
ms.assetid: 2e7fd269-bd5f-40b7-b123-36b9c783a917
title: Propiedad AdminUser
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11651f0d7103edabbcf7b40087db91f999b1a5b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654006"
---
# <a name="adminuser-property"></a><span data-ttu-id="789f2-103">Propiedad AdminUser</span><span class="sxs-lookup"><span data-stu-id="789f2-103">AdminUser property</span></span>

<span data-ttu-id="789f2-104">El instalador establece esta propiedad si el usuario tiene privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="789f2-104">The installer sets this property if the user has administrator privileges.</span></span>

<span data-ttu-id="789f2-105">**Windows Server 2008 y Windows Vista:** La propiedad **AdminUser** es la misma que la propiedad [**privileged**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="789f2-105">**Windows Server 2008 and Windows Vista:** The **AdminUser** property is the same as the [**Privileged**](privileged.md) property.</span></span> <span data-ttu-id="789f2-106">Los autores deben usar la propiedad **privileged** .</span><span class="sxs-lookup"><span data-stu-id="789f2-106">Authors should used the **Privileged** property.</span></span> <span data-ttu-id="789f2-107">El instalador establece estas propiedades si el usuario tiene privilegios de administrador, si la aplicación ha sido asignada por un administrador del sistema, o si las directivas de usuario y de equipo AlwaysInstallElevated están establecidas en true.</span><span class="sxs-lookup"><span data-stu-id="789f2-107">The installer sets these properties if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="remarks"></a><span data-ttu-id="789f2-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="789f2-108">Remarks</span></span>

<span data-ttu-id="789f2-109">Las diferencias entre estas propiedades se pueden haber usado en algunos paquetes heredados.</span><span class="sxs-lookup"><span data-stu-id="789f2-109">The differences between these properties may have been used in some legacy packages.</span></span> <span data-ttu-id="789f2-110">Por ejemplo, se puede haber utilizado **AdminUser** en lugar de [**privileged**](privileged.md) en instrucciones condicionales, porque el instalador solo establece la propiedad **AdminUser** si el usuario es un administrador.</span><span class="sxs-lookup"><span data-stu-id="789f2-110">For example, **AdminUser** may have been used instead of [**Privileged**](privileged.md) in conditional statements, because the installer only sets the **AdminUser** property if the user is an administrator.</span></span> <span data-ttu-id="789f2-111">El instalador establece la propiedad **privileged** si el usuario es un administrador o si la Directiva permite al usuario instalar con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="789f2-111">The installer sets the **Privileged** property if the user is an administrator, or if policy enables the user to install with elevated privileges.</span></span>

<span data-ttu-id="789f2-112">**Windows Server 2008 y Windows Vista:** No compatible.</span><span class="sxs-lookup"><span data-stu-id="789f2-112">**Windows Server 2008 and Windows Vista:** Not supported.</span></span> <span data-ttu-id="789f2-113">[**Privileged**](privileged.md) y **AdminUser** son los mismos.</span><span class="sxs-lookup"><span data-stu-id="789f2-113">The [**Privileged**](privileged.md) and **AdminUser** are the same.</span></span> <span data-ttu-id="789f2-114">Los paquetes que requieren distintas propiedades **privileged** y **AdminUser** pueden restaurar la diferencia estableciendo la propiedad [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) .</span><span class="sxs-lookup"><span data-stu-id="789f2-114">Packages that require distinct **Privileged** and **AdminUser** properties can restore the difference by setting the [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md) property.</span></span>

<span data-ttu-id="789f2-115">Para obtener más información, vea [instalar un paquete con privilegios elevados para una propiedad sin privilegios de administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)y con [**privilegios**](privileged.md) .</span><span class="sxs-lookup"><span data-stu-id="789f2-115">For more information, see [Installing a Package with Elevated Privileges for a Non-Admin](installing-a-package-with-elevated-privileges-for-a-non-admin.md), and [**Privileged**](privileged.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="789f2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="789f2-116">Requirements</span></span>



| <span data-ttu-id="789f2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="789f2-117">Requirement</span></span> | <span data-ttu-id="789f2-118">Value</span><span class="sxs-lookup"><span data-stu-id="789f2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="789f2-119">Versión</span><span class="sxs-lookup"><span data-stu-id="789f2-119">Version</span></span><br/> | <span data-ttu-id="789f2-120">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="789f2-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="789f2-121">Windows Installer 4,0 o Windows Installer 4,5 en Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="789f2-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="789f2-122">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="789f2-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="789f2-123">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="789f2-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="789f2-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="789f2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="789f2-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="789f2-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




