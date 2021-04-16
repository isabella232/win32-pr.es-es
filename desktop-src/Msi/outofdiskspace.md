---
description: El instalador establece la propiedad OutOfDiskSpace en TRUE si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para alojar la instalación.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propiedad OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679526"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="b7b84-103">Propiedad OutOfDiskSpace</span><span class="sxs-lookup"><span data-stu-id="b7b84-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="b7b84-104">El instalador establece la propiedad **OutOfDiskSpace** en true si algún volumen que sea un destino de la instalación actual no tiene suficiente espacio en disco para alojar la instalación.</span><span class="sxs-lookup"><span data-stu-id="b7b84-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="b7b84-105">Si todos los volúmenes tienen suficiente espacio, el valor es FALSE.</span><span class="sxs-lookup"><span data-stu-id="b7b84-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="b7b84-106">Acciones de resolución de selección use este valor para cancelar una instalación y generar un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="b7b84-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="b7b84-107">Esta propiedad es válida en cualquier momento después de ejecutar la [acción CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b84-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="b7b84-108">El estado de la propiedad [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) se actualiza dinámicamente cada vez que se vuelve a calcular el costo total de instalación (por ejemplo, cada vez que se cambia el estado de la instalación de cualquier característica a través del cuadro de diálogo de [selección](selection-dialog.md) ).</span><span class="sxs-lookup"><span data-stu-id="b7b84-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b84-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b7b84-109">Remarks</span></span>

<span data-ttu-id="b7b84-110">Cualquier cuadro de diálogo que dependa de la propiedad **OutOfDiskSpace** para determinar si se debe mostrar un cuadro de diálogo debe establecer el [bit de estilo de cuadro de diálogo TrackDiskSpace](trackdiskspace-dialog-style-bit.md) del cuadro de diálogo para actualizar dinámicamente el espacio en los volúmenes de destino.</span><span class="sxs-lookup"><span data-stu-id="b7b84-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7b84-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7b84-111">Requirements</span></span>



| <span data-ttu-id="b7b84-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7b84-112">Requirement</span></span> | <span data-ttu-id="b7b84-113">Value</span><span class="sxs-lookup"><span data-stu-id="b7b84-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7b84-114">Versión</span><span class="sxs-lookup"><span data-stu-id="b7b84-114">Version</span></span><br/> | <span data-ttu-id="b7b84-115">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7b84-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7b84-116">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b7b84-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b7b84-117">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b7b84-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b7b84-118">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b7b84-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7b84-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b7b84-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b84-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7b84-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




