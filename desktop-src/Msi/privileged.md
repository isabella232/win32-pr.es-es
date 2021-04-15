---
description: La propiedad privileged indica si la instalación se realiza en el contexto de privilegios elevados.
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: Propiedad privileged
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653933"
---
# <a name="privileged-property"></a><span data-ttu-id="a545e-103">Propiedad privileged</span><span class="sxs-lookup"><span data-stu-id="a545e-103">Privileged property</span></span>

<span data-ttu-id="a545e-104">La propiedad **privileged** indica si la instalación se realiza en el contexto de privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="a545e-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="a545e-105">El instalador establece esta propiedad si el usuario tiene privilegios de administrador, si el administrador del sistema ha asignado la aplicación, o si las directivas de usuario y de equipo AlwaysInstallElevated están establecidas en true.</span><span class="sxs-lookup"><span data-stu-id="a545e-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="a545e-106">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="a545e-106">Default Value</span></span>

<span data-ttu-id="a545e-107">El instalador no establece esta propiedad si el usuario no tiene permiso para instalar con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="a545e-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="a545e-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a545e-108">Remarks</span></span>

<span data-ttu-id="a545e-109">Los desarrolladores de paquetes del instalador pueden utilizar la propiedad **privileged** para hacer que la instalación sea condicional en la Directiva del sistema, el usuario es un administrador o la asignación por parte de un administrador.</span><span class="sxs-lookup"><span data-stu-id="a545e-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="a545e-110">Cuando se ejecuta en Windows Vista, **privileged** y [**AdminUser**](adminuser.md) son los mismos.</span><span class="sxs-lookup"><span data-stu-id="a545e-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="a545e-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a545e-111">Requirements</span></span>



| <span data-ttu-id="a545e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a545e-112">Requirement</span></span> | <span data-ttu-id="a545e-113">Value</span><span class="sxs-lookup"><span data-stu-id="a545e-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a545e-114">Versión</span><span class="sxs-lookup"><span data-stu-id="a545e-114">Version</span></span><br/> | <span data-ttu-id="a545e-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a545e-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a545e-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a545e-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a545e-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a545e-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a545e-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a545e-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a545e-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a545e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a545e-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a545e-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




