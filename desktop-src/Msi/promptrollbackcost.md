---
description: La propiedad PROMPTROLLBACKCOST especifica la acción que realiza el instalador si están habilitadas las funcionalidades de instalación de reversión y no hay suficiente espacio en disco para completar la instalación. Los valores posibles de PROMPTROLLBACKCOST son los siguientes. ValueActionPDisplay un cuadro de diálogo en el que se le pregunta si desea continuar sin una reversión. DDisable revertir y continuar sin preguntar al usuario. FFail con el mensaje de error de espacio insuficiente en disco.
ms.assetid: 6ffd0b3f-79b8-4ce3-a262-4d27ffc5a175
title: Propiedad PROMPTROLLBACKCOST
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3801ee894a66ad6e458cbad37252e289f724b9ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653914"
---
# <a name="promptrollbackcost-property"></a><span data-ttu-id="a8d34-103">Propiedad PROMPTROLLBACKCOST</span><span class="sxs-lookup"><span data-stu-id="a8d34-103">PROMPTROLLBACKCOST property</span></span>

<span data-ttu-id="a8d34-104">La propiedad **PROMPTROLLBACKCOST** especifica la acción que realiza el instalador si están habilitadas las funcionalidades de [instalación de reversión](rollback-installation.md) y no hay suficiente espacio en disco para completar la instalación.</span><span class="sxs-lookup"><span data-stu-id="a8d34-104">The **PROMPTROLLBACKCOST** property specifies the action the installer takes if [rollback installation](rollback-installation.md) capabilities are enabled and there is insufficient disk space to complete the installation.</span></span>

<span data-ttu-id="a8d34-105">Los valores posibles de **PROMPTROLLBACKCOST** son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="a8d34-105">The possible values of **PROMPTROLLBACKCOST** are as follows.</span></span>



| <span data-ttu-id="a8d34-106">Value</span><span class="sxs-lookup"><span data-stu-id="a8d34-106">Value</span></span> | <span data-ttu-id="a8d34-107">Acción</span><span class="sxs-lookup"><span data-stu-id="a8d34-107">Action</span></span>                                                              |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="a8d34-108">P</span><span class="sxs-lookup"><span data-stu-id="a8d34-108">P</span></span>     | <span data-ttu-id="a8d34-109">Muestra un cuadro de diálogo en el que se le pregunta si desea continuar sin una reversión.</span><span class="sxs-lookup"><span data-stu-id="a8d34-109">Display a dialog box asking whether to continue without a rollback.</span></span> |
| <span data-ttu-id="a8d34-110">D</span><span class="sxs-lookup"><span data-stu-id="a8d34-110">D</span></span>     | <span data-ttu-id="a8d34-111">Deshabilite la reversión y continúe sin preguntar al usuario.</span><span class="sxs-lookup"><span data-stu-id="a8d34-111">Disable rollback and continue without asking user.</span></span>                  |
| <span data-ttu-id="a8d34-112">F</span><span class="sxs-lookup"><span data-stu-id="a8d34-112">F</span></span>     | <span data-ttu-id="a8d34-113">Error con el mensaje de error de espacio insuficiente en disco.</span><span class="sxs-lookup"><span data-stu-id="a8d34-113">Fail with the out-of-disk-space error prompt.</span></span>                       |



 

## <a name="remarks"></a><span data-ttu-id="a8d34-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8d34-114">Remarks</span></span>

<span data-ttu-id="a8d34-115">Cuando la interfaz de usuario se ejecuta en el nivel básico o sin interfaz de usuario, el instalador controla automáticamente toda la lógica de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="a8d34-115">When the user interface is run at the Basic or no UI level, the installer handles all the out-of-disk-space logic automatically.</span></span>

<span data-ttu-id="a8d34-116">Cuando la interfaz de usuario se ejecuta en el nivel completo, se pueden proporcionar opciones adicionales al usuario, como preguntar antes de continuar con una reversión, deshabilitar la reversión o continuar sin reversión cuando el disco está lleno.</span><span class="sxs-lookup"><span data-stu-id="a8d34-116">When the user interface runs at the Full level, the user can be given additional options, such as prompting before proceeding with a rollback, disabling rollback, or proceeding without rollback when the disk is full.</span></span> <span data-ttu-id="a8d34-117">Depende del desarrollador de paquetes crear la secuencia del cuadro de diálogo para proporcionar las opciones adecuadas al usuario.</span><span class="sxs-lookup"><span data-stu-id="a8d34-117">It is up to the package developer to author the dialog box sequence to provide the appropriate choices to the user.</span></span> <span data-ttu-id="a8d34-118">Los elementos disponibles para ello son las propiedades [EnableRollback ControlEvent,](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) , [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) y **PROMPTROLLBACKCOST** .</span><span class="sxs-lookup"><span data-stu-id="a8d34-118">The elements available to do this are the [EnableRollback ControlEvent](enablerollback-controlevent.md), [**OutOfDiskSpace**](outofdiskspace.md) property, [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property, and the **PROMPTROLLBACKCOST** property.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d34-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d34-119">Requirements</span></span>



| <span data-ttu-id="a8d34-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d34-120">Requirement</span></span> | <span data-ttu-id="a8d34-121">Value</span><span class="sxs-lookup"><span data-stu-id="a8d34-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d34-122">Versión</span><span class="sxs-lookup"><span data-stu-id="a8d34-122">Version</span></span><br/> | <span data-ttu-id="a8d34-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8d34-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8d34-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8d34-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8d34-125">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8d34-125">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a8d34-126">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a8d34-126">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8d34-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a8d34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d34-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8d34-128">Properties</span></span>](properties.md)
</dt> </dl>

 

 




