---
description: El instalador establece el valor de la propiedad MsiSystemRebootPending en 1 si hay una operación pendiente para cambiar el nombre de un archivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propiedad MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680635"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="7f72e-103">Propiedad MsiSystemRebootPending</span><span class="sxs-lookup"><span data-stu-id="7f72e-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="7f72e-104">El instalador establece el valor de la propiedad **MsiSystemRebootPending** en 1 si hay una operación pendiente para cambiar el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="7f72e-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="7f72e-105">Los autores de paquetes pueden basar una condición en la [tabla LaunchCondition](launchcondition-table.md) de esta propiedad para evitar la instalación de su paquete en los casos en los que hay una operación pendiente de cambiar el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="7f72e-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="7f72e-106">Esto puede realizarse para evitar que se reinicie el sistema operativo causado por el cambio de nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="7f72e-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="7f72e-107">El instalador no establece la propiedad **MsiSystemRebootPending** en todos los casos que requieren un reinicio del sistema.</span><span class="sxs-lookup"><span data-stu-id="7f72e-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f72e-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f72e-108">Requirements</span></span>



| <span data-ttu-id="7f72e-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f72e-109">Requirement</span></span> | <span data-ttu-id="7f72e-110">Value</span><span class="sxs-lookup"><span data-stu-id="7f72e-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f72e-111">Versión</span><span class="sxs-lookup"><span data-stu-id="7f72e-111">Version</span></span><br/> | <span data-ttu-id="7f72e-112">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f72e-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7f72e-113">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f72e-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7f72e-114">Windows Installer 4,5 en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7f72e-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7f72e-115">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="7f72e-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7f72e-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7f72e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f72e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7f72e-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="7f72e-118">Reinicios del sistema</span><span class="sxs-lookup"><span data-stu-id="7f72e-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="7f72e-119">No se admite en Windows Installer 3,1 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="7f72e-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




