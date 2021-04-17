---
description: La interfaz IVssComponent permite a un escritor ajustar exactamente cómo se restauran los archivos componente por componente.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Establecimiento de destinos de restauración de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696968"
---
# <a name="setting-vss-restore-targets"></a><span data-ttu-id="4caab-103">Establecimiento de destinos de restauración de VSS</span><span class="sxs-lookup"><span data-stu-id="4caab-103">Setting VSS Restore Targets</span></span>

<span data-ttu-id="4caab-104">La interfaz [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permite a un escritor ajustar exactamente cómo se restauran los archivos componente por componente.</span><span class="sxs-lookup"><span data-stu-id="4caab-104">The [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) interface enables a writer to fine-tune exactly how files are restored on a component-by-component basis.</span></span>

<span data-ttu-id="4caab-105">Dado que es posible que la configuración del sistema durante la restauración no sea la esperada durante la copia de seguridad, se proporciona el mecanismo de destino de la restauración.</span><span class="sxs-lookup"><span data-stu-id="4caab-105">Because it is possible that the system configuration during restore is something other than that anticipated during backup, the restore target mechanism is provided.</span></span>

<span data-ttu-id="4caab-106">Permite a los escritores llamar a [**IVssComponent:: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) para cambiar el modo en que se restauran los componentes que se [*incluyen explícitamente*](vssgloss-e.md) en el documento de componentes de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4caab-106">It allows writers to call [**IVssComponent::SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) to change how those components that are [*explicitly included*](vssgloss-e.md) in the Backup Components Document are restored.</span></span> <span data-ttu-id="4caab-107">Esto también cambia el mecanismo de restauración usado en los componentes que se incluyen de forma [*implícita*](vssgloss-i.md).</span><span class="sxs-lookup"><span data-stu-id="4caab-107">This also changes the restoration mechanism used on those components that are [*implicitly included*](vssgloss-i.md).</span></span>

<span data-ttu-id="4caab-108">La restauración de archivos que tiene lugar durante un reinicio del sistema (bajo los valores de enumeración de RESTOREMETHOD de la enumeración de la enumeración [**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) de VSS la \_ \_ restauración \_ de RME al \_ reiniciar y VSS \_ RME \_ restore \_ en el \_ reinicio \_ si \_ no se puede \_ reemplazar) no puede verse afectado por los destinos de restauración porque no hay ningún servicio VSS en ejecución cuando **MoveFileEx** copia los archivos en su ubicación</span><span class="sxs-lookup"><span data-stu-id="4caab-108">File restoration that takes place during a system reboot (under the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration values VSS\_RME\_RESTORE\_AT\_REBOOT and VSS\_RME\_RESTORE\_AT\_REBOOT\_IF\_CANNOT\_REPLACE) cannot be affected by restore targets because there are no running VSS services when **MoveFileEx** copies files to their final location.</span></span>

<span data-ttu-id="4caab-109">Del mismo modo, las \_ restauraciones personalizadas de RME de VSS \_ pueden verse afectadas o no, ya que cada restauración personalizada es específica de un escritor determinado y puede decidir o omitir los destinos de restauración.</span><span class="sxs-lookup"><span data-stu-id="4caab-109">Similarly, VSS\_RME\_CUSTOM restores may or may not be affected, because each custom restore is specific to a given writer and can choose to respect or ignore restore targets.</span></span>

<span data-ttu-id="4caab-110">Los solicitantes y escritores pueden usar [**IVssComponent:: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) para comprobar el destino de restauración de un conjunto de componentes.</span><span class="sxs-lookup"><span data-stu-id="4caab-110">Requesters and writers can use [**IVssComponent::GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) to check the restore target of a component set.</span></span>

<span data-ttu-id="4caab-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) admite los siguientes destinos de restauración, que se pueden establecer en un componente establecido por el conjunto de componentes:</span><span class="sxs-lookup"><span data-stu-id="4caab-111">[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) supports the following restore targets, which can be set on a component set by component set basis:</span></span>

-   <span data-ttu-id="4caab-112">VSS \_ RT \_ original.</span><span class="sxs-lookup"><span data-stu-id="4caab-112">VSS\_RT\_ORIGINAL.</span></span> <span data-ttu-id="4caab-113">Se respetará el método restore especificado por la enumeración de enumeración [**\_ \_ RESTOREMETHOD de VSS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) .</span><span class="sxs-lookup"><span data-stu-id="4caab-113">The restore method specified by the [**VSS\_RESTOREMETHOD\_ENUM**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) enumeration will be respected.</span></span>
-   <span data-ttu-id="4caab-114">VSS \_ RT \_ alternativo.</span><span class="sxs-lookup"><span data-stu-id="4caab-114">VSS\_RT\_ALTERNATE.</span></span> <span data-ttu-id="4caab-115">Los archivos se restauran en una ubicación determinada a partir de una asignación de ubicación alternativa existente.</span><span class="sxs-lookup"><span data-stu-id="4caab-115">The files are restored to a location determined from an existing alternate location mapping.</span></span> <span data-ttu-id="4caab-116">Si existe una asignación de ubicación alternativa que coincide con una ruta de acceso en un subcomponente de conjunto de componentes, restaure a la ubicación alternativa si es posible; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="4caab-116">If an alternate location mapping matching a path in a component set subcomponent exists, restore to the alternate location if possible; otherwise, return an error.</span></span>

 

 



