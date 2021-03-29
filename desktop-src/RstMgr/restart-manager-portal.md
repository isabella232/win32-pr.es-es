---
title: Administrador de reinicio
description: Escriba instaladores personalizados para eliminar los reinicios del sistema necesarios para completar la actualización de un archivo en uso. Cierre y reinicie todos los servicios de sistema, pero críticos, de programas.
ms.assetid: 44b7975a-0093-4c8f-9a14-2a6bfd7a68a5
keywords:
- Admin. de reinicio del administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1244cff7bc22fd2e7b6d2540051bd0984596086
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078089"
---
# <a name="restart-manager"></a><span data-ttu-id="46716-105">Administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="46716-105">Restart Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="46716-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="46716-106">Purpose</span></span>

<span data-ttu-id="46716-107">La API del administrador de reinicio puede eliminar o reducir el número de reinicios del sistema necesarios para completar una instalación o actualización.</span><span class="sxs-lookup"><span data-stu-id="46716-107">The Restart Manager API can eliminate or reduce the number of system restarts that are required to complete an installation or update.</span></span> <span data-ttu-id="46716-108">La razón principal por la que las actualizaciones de software requieren un reinicio del sistema durante una instalación o actualización es que algunos de los archivos que se están actualizando se están usando actualmente en una aplicación o servicio en ejecución.</span><span class="sxs-lookup"><span data-stu-id="46716-108">The primary reason software updates require a system restart during an installation or update is that some of the files that are being updated are currently being used by a running application or service.</span></span> <span data-ttu-id="46716-109">El administrador de reinicio permite que todos los [servicios del sistema críticos](critical-system-services.md) se apaguen y se reinicien.</span><span class="sxs-lookup"><span data-stu-id="46716-109">The Restart Manager enables all but the [critical system services](critical-system-services.md) to be shut down and restarted.</span></span> <span data-ttu-id="46716-110">Esto libera los archivos que se están usando y permite que se completen las operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="46716-110">This frees files that are in use and allows installation operations to complete.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="46716-111">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="46716-111">Where applicable</span></span>

<span data-ttu-id="46716-112">El archivo DLL del administrador de reinicio exporta una interfaz pública de C que puede ser cargada por instaladores estándar o personalizados.</span><span class="sxs-lookup"><span data-stu-id="46716-112">The Restart Manager DLL exports a public C interface that can be loaded by standard or custom installers.</span></span> <span data-ttu-id="46716-113">El instalador puede usar el administrador de reinicio para registrar archivos que deben reemplazarse durante la instalación de una aplicación o una actualización.</span><span class="sxs-lookup"><span data-stu-id="46716-113">The installer can use the Restart Manager to register files that should be replaced during the installation of an application or update.</span></span> <span data-ttu-id="46716-114">Después, durante una actualización o instalación posterior, el instalador puede usar el administrador de reinicio para determinar qué archivos no se pueden actualizar porque están actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="46716-114">Then during a subsequent update or installation, the installer can use the Restart Manager to determine which files cannot be updated because they are currently in use.</span></span> <span data-ttu-id="46716-115">El administrador de reinicio puede apagar y reiniciar los servicios no críticos o las aplicaciones que usan actualmente esos archivos.</span><span class="sxs-lookup"><span data-stu-id="46716-115">Restart Manager can shut down and restart the non-critical services or applications that are currently using those files.</span></span> <span data-ttu-id="46716-116">Los instaladores pueden dirigir el administrador de reinicio para apagar y reiniciar aplicaciones o servicios según el archivo en uso, el ID. de proceso (PID) o el nombre corto de un servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="46716-116">Installers can direct the Restart Manager to shut down and restart applications or services based on the file in use, the process ID (PID), or the short-name of a Windows service.</span></span>

<span data-ttu-id="46716-117">El administrador de reinicio está diseñado para el desarrollo de aplicaciones de estilo de escritorio.</span><span class="sxs-lookup"><span data-stu-id="46716-117">Restart Manager is intended for the development of desktop style applications.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="46716-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="46716-118">Developer audience</span></span>

<span data-ttu-id="46716-119">Esta documentación está dirigida a los desarrolladores de aplicaciones de instalación que desean aprovechar las capacidades del instalador en Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="46716-119">This documentation is intended for developers of installation applications who want to take advantage of the installer capabilities in Windows Vista or Windows Server 2008.</span></span> <span data-ttu-id="46716-120">Las aplicaciones que utilizan la [Windows Installer](/windows/desktop/Msi/windows-installer-portal) versión 4,0 para la instalación y el mantenimiento usan automáticamente el administrador de reinicio para reducir los reinicios del sistema.</span><span class="sxs-lookup"><span data-stu-id="46716-120">Applications that use the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) version 4.0 for installation and servicing automatically use the Restart Manager to reduce system restarts.</span></span> <span data-ttu-id="46716-121">Los instaladores personalizados también pueden diseñarse para que llamen a la API del administrador de reinicio para apagar y reiniciar las aplicaciones y los servicios.</span><span class="sxs-lookup"><span data-stu-id="46716-121">Custom installers can also be designed to call the Restart Manager API to shut down and restart applications and services.</span></span> <span data-ttu-id="46716-122">En los casos en los que no se puede evitar el reinicio del sistema, los instaladores pueden usar la API del administrador de reinicio para programar los reinicios de forma que se minimice la interrupción del flujo de trabajo del usuario.</span><span class="sxs-lookup"><span data-stu-id="46716-122">In cases where a system restart is unavoidable, installers can use the Restart Manager API to schedule restarts in such a way that it minimizes the disruption of the user's work flow.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="46716-123">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="46716-123">Run-time requirements</span></span>

<span data-ttu-id="46716-124">La API del administrador de reinicio está disponible a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="46716-124">The Restart Manager API is available beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="46716-125">El administrador de reinicio consta de un solo archivo DLL que las aplicaciones pueden cargar para tener acceso a la API del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="46716-125">Restart Manager consists of a single DLL that applications can load to access the Restart Manager API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="46716-126">En esta sección</span><span class="sxs-lookup"><span data-stu-id="46716-126">In this section</span></span>



| <span data-ttu-id="46716-127">Tema</span><span class="sxs-lookup"><span data-stu-id="46716-127">Topic</span></span>                                                                 | <span data-ttu-id="46716-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="46716-128">Description</span></span>                                                     |
|-----------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="46716-129">Acerca del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="46716-129">About Restart Manager</span></span>](about-restart-manager.md)<br/>         | <span data-ttu-id="46716-130">Temas de información general que describen el administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="46716-130">Overview topics that describe the Restart Manager.</span></span><br/>   |
| [<span data-ttu-id="46716-131">Uso del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="46716-131">Using Restart Manager</span></span>](using-restart-manager.md)<br/>         | <span data-ttu-id="46716-132">Temas de información general sobre el uso de la API del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="46716-132">Overview topics about using the Restart Manager API.</span></span><br/> |
| [<span data-ttu-id="46716-133">Referencia del administrador de reinicio</span><span class="sxs-lookup"><span data-stu-id="46716-133">Restart Manager Reference</span></span>](restart-manager-reference.md)<br/> | <span data-ttu-id="46716-134">Temas de referencia de la API del administrador de reinicio.</span><span class="sxs-lookup"><span data-stu-id="46716-134">Reference topics for the Restart Manager API.</span></span><br/>        |



 

 

