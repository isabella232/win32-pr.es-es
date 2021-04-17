---
description: El instalador establece la propiedad OutOfNoRbDiskSpace en true si algún volumen que sea un destino de la instalación no tiene suficiente espacio en disco para alojar la instalación.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propiedad OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653799"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="8bcb3-103">Propiedad OutOfNoRbDiskSpace</span><span class="sxs-lookup"><span data-stu-id="8bcb3-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="8bcb3-104">El instalador establece la propiedad **OutOfNoRbDiskSpace** en true si algún volumen que sea un destino de la instalación no tiene suficiente espacio en disco para alojar la instalación.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="8bcb3-105">En este caso, la propiedad **OutOfNoRbDiskSpace** se establece en true incluso si se ha deshabilitado la reversión.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="8bcb3-106">Si todos los volúmenes tienen suficiente espacio, el valor es false.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="8bcb3-107">Un desarrollador de un paquete de instalación puede controlar la situación en la que la propiedad [**OutOfDiskSpace**](outofdiskspace.md) es true y la propiedad **OutOfNoRbDiskSpace** es falsa mediante la creación de una interfaz de usuario que presenta al usuario una opción para deshabilitar la reversión y continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="8bcb3-108">Para obtener información sobre cómo mostrar un cuadro de diálogo condicionalmente, consulte [información general de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8bcb3-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="8bcb3-109">Para obtener información sobre cómo deshabilitar la reversión, vea [EnableRollback ControlEvent,](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="8bcb3-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="8bcb3-110">La propiedad **OutOfNoRbDiskSpace** es válida en cualquier momento después de ejecutar la [acción CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8bcb3-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="8bcb3-111">El estado de la propiedad **OutOfNoRbDiskSpace** se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de la instalación de cualquier característica a través del [cuadro de diálogo de selección](selection-dialog.md)).</span><span class="sxs-lookup"><span data-stu-id="8bcb3-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="8bcb3-112">Acciones de resolución de selección use este valor para cancelar una instalación y generar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bcb3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bcb3-113">Requirements</span></span>



| <span data-ttu-id="8bcb3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bcb3-114">Requirement</span></span> | <span data-ttu-id="8bcb3-115">Value</span><span class="sxs-lookup"><span data-stu-id="8bcb3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8bcb3-116">Versión</span><span class="sxs-lookup"><span data-stu-id="8bcb3-116">Version</span></span><br/> | <span data-ttu-id="8bcb3-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8bcb3-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8bcb3-119">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8bcb3-120">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8bcb3-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8bcb3-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8bcb3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bcb3-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bcb3-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8bcb3-123">Información general de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8bcb3-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="8bcb3-124">**Propiedad OutOfDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="8bcb3-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="8bcb3-125">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="8bcb3-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="8bcb3-126">Acción CostFinalize</span><span class="sxs-lookup"><span data-stu-id="8bcb3-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="8bcb3-127">Cuadro de diálogo de selección</span><span class="sxs-lookup"><span data-stu-id="8bcb3-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




