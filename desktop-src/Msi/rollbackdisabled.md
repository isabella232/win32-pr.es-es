---
description: El instalador establece la propiedad RollbackDisabled cuando se ha deshabilitado la reversión.
ms.assetid: 72215b0f-2fc4-49aa-abf8-3206bdfc765f
title: Propiedad RollbackDisabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f50c8e344ed4291210afb1714ce97d90b590999
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653469"
---
# <a name="rollbackdisabled-property"></a><span data-ttu-id="56bf8-103">Propiedad RollbackDisabled</span><span class="sxs-lookup"><span data-stu-id="56bf8-103">RollbackDisabled property</span></span>

<span data-ttu-id="56bf8-104">El instalador establece la propiedad **RollbackDisabled** cuando se ha deshabilitado la reversión.</span><span class="sxs-lookup"><span data-stu-id="56bf8-104">The installer sets the **RollbackDisabled** property when rollback has been disabled.</span></span> <span data-ttu-id="56bf8-105">**RollbackDisabled** lo utilizan los autores de paquetes que necesitan asegurarse de que el instalador no haya deshabilitado la reversión.</span><span class="sxs-lookup"><span data-stu-id="56bf8-105">**RollbackDisabled** is used by package authors who need to ensure that the installer has not disabled rollback.</span></span> <span data-ttu-id="56bf8-106">La propiedad **RollbackDisabled** se puede usar en una expresión condicional que evita que continúe con la instalación si se establece la propiedad **RollbackDisabled** .</span><span class="sxs-lookup"><span data-stu-id="56bf8-106">The **RollbackDisabled** property can be used in a conditional expression that effectively refuses to continue with the installation if **RollbackDisabled** property is set.</span></span>

## <a name="default-value"></a><span data-ttu-id="56bf8-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="56bf8-107">Default Value</span></span>

<span data-ttu-id="56bf8-108">De forma predeterminada, la reversión está habilitada.</span><span class="sxs-lookup"><span data-stu-id="56bf8-108">By default, rollback is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="56bf8-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56bf8-109">Remarks</span></span>

<span data-ttu-id="56bf8-110">Dado que la [reversión](rollback-custom-actions.md) y la [confirmación](commit-custom-actions.md) no se ejecutan mientras la reversión está deshabilitada, el instalador no puede instalar correctamente un paquete que use estos tipos de acciones personalizadas en una transacción durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="56bf8-110">Because [rollback](rollback-custom-actions.md) and [commit](commit-custom-actions.md) do not run while rollback is disabled, the installer cannot properly install a package that uses these types of custom actions in a transaction during the installation.</span></span> <span data-ttu-id="56bf8-111">En este caso, el autor del paquete debe incluir una condición con DisableRollback que impida que la instalación continúe si la reversión está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="56bf8-111">In this case, the author of the package should include a condition using DisableRollback that prevents the installation from continuing if rollback is disabled.</span></span>

<span data-ttu-id="56bf8-112">Un administrador puede establecer el valor de la Directiva DisableRollback como parte de la asignación de la Directiva del sistema.</span><span class="sxs-lookup"><span data-stu-id="56bf8-112">The DisableRollback policy value can be set by an administrator as a part of assigning system policy.</span></span> <span data-ttu-id="56bf8-113">A los administradores se les aconseja no deshabilitar la reversión a menos que sea necesario.</span><span class="sxs-lookup"><span data-stu-id="56bf8-113">Administrators are advised to not disable rollback unless necessary.</span></span> <span data-ttu-id="56bf8-114">Para obtener más información sobre el valor de directiva de DisableRollback, consulte [Directiva del sistema](system-policy.md).</span><span class="sxs-lookup"><span data-stu-id="56bf8-114">For more information about DisableRollback policy value, see [System Policy](system-policy.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56bf8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56bf8-115">Requirements</span></span>



| <span data-ttu-id="56bf8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="56bf8-116">Requirement</span></span> | <span data-ttu-id="56bf8-117">Value</span><span class="sxs-lookup"><span data-stu-id="56bf8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56bf8-118">Versión</span><span class="sxs-lookup"><span data-stu-id="56bf8-118">Version</span></span><br/> | <span data-ttu-id="56bf8-119">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56bf8-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="56bf8-120">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56bf8-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="56bf8-121">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56bf8-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="56bf8-122">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="56bf8-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56bf8-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="56bf8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56bf8-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56bf8-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="56bf8-125">Revertir instalación</span><span class="sxs-lookup"><span data-stu-id="56bf8-125">Rollback Installation</span></span>](rollback-installation.md)
</dt> <dt>

[<span data-ttu-id="56bf8-126">Directiva del sistema</span><span class="sxs-lookup"><span data-stu-id="56bf8-126">System Policy</span></span>](system-policy.md)
</dt> <dt>

[<span data-ttu-id="56bf8-127">revertir acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="56bf8-127">rollback custom actions</span></span>](rollback-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="56bf8-128">Confirmar acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="56bf8-128">commit custom actions</span></span>](commit-custom-actions.md)
</dt> </dl>

 

 




