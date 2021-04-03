---
title: Usar IMAPi
description: En los temas siguientes se muestra el uso de la API de maestro de imágenes.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccd44d01e925d07d251e93a29c5268cc7e9c5076
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903876"
---
# <a name="using-imapi"></a><span data-ttu-id="d180c-103">Usar IMAPi</span><span class="sxs-lookup"><span data-stu-id="d180c-103">Using IMAPI</span></span>

<span data-ttu-id="d180c-104">En los temas siguientes se muestra el uso de la API de maestro de imágenes.</span><span class="sxs-lookup"><span data-stu-id="d180c-104">The following topics demonstrate the use of the image mastering API.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="d180c-105">Escenarios de uso</span><span class="sxs-lookup"><span data-stu-id="d180c-105">Usage Scenarios</span></span>

<span data-ttu-id="d180c-106">La siguiente documentación proporciona instrucciones detalladas para escenarios comunes de IMAPi.</span><span class="sxs-lookup"><span data-stu-id="d180c-106">The following documentation provides detailed guidance for common IMAPI scenarios.</span></span>



| <span data-ttu-id="d180c-107">Escenario</span><span class="sxs-lookup"><span data-stu-id="d180c-107">Scenario</span></span>                                                                                                         | <span data-ttu-id="d180c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d180c-108">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d180c-109">Comprobando la compatibilidad con la unidad</span><span class="sxs-lookup"><span data-stu-id="d180c-109">Checking Drive Support</span></span>](checking-drive-support.md)                                                             | <span data-ttu-id="d180c-110">Muestra la detección de la compatibilidad de una unidad de medios.</span><span class="sxs-lookup"><span data-stu-id="d180c-110">Demonstrates the detection of support for a media drive.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="d180c-111">Comprobando la compatibilidad con medios</span><span class="sxs-lookup"><span data-stu-id="d180c-111">Checking Media Support</span></span>](checking-media-support.md)                                                             | <span data-ttu-id="d180c-112">Muestra la detección de compatibilidad con los medios.</span><span class="sxs-lookup"><span data-stu-id="d180c-112">Demonstrates the detection of support for media.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="d180c-113">Grabación de una imagen de disco</span><span class="sxs-lookup"><span data-stu-id="d180c-113">Burning a Disc Image</span></span>](burning-a-disc.md)                                                                       | <span data-ttu-id="d180c-114">Muestra la maestra (grabación de un disco) mediante IMAPi.</span><span class="sxs-lookup"><span data-stu-id="d180c-114">Demonstrates mastering (burning a disc) using IMAPI.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="d180c-115">Agregar una imagen de arranque</span><span class="sxs-lookup"><span data-stu-id="d180c-115">Adding a Boot Image</span></span>](adding-a-boot-image.md)                                                                   | <span data-ttu-id="d180c-116">Se basa en el ejemplo de [grabación de una imagen de disco](burning-a-disc.md) mediante la adición de código para incluir una imagen de arranque en la sección de arranque del disco.</span><span class="sxs-lookup"><span data-stu-id="d180c-116">Builds on the [Burning a Disc Image](burning-a-disc.md) example by adding code to include a bootable image in the boot section of the disc.</span></span><br/>               |
| [<span data-ttu-id="d180c-117">Creación de un disco de múltiples sesiones</span><span class="sxs-lookup"><span data-stu-id="d180c-117">Creating a Multisession Disc</span></span>](creating-a-multisession-disc.md)                                                 | <span data-ttu-id="d180c-118">Muestra la creación de un disco de múltiples sesiones mediante IMAPi.</span><span class="sxs-lookup"><span data-stu-id="d180c-118">Demonstrates the creation of a multisession disc using IMAPI.</span></span><br/>                                                                                              |
| [<span data-ttu-id="d180c-119">Supervisar el progreso con eventos</span><span class="sxs-lookup"><span data-stu-id="d180c-119">Monitoring Progress With Events</span></span>](monitoring-progress-with-events.md)                                           | <span data-ttu-id="d180c-120">Muestra el uso de interfaces específicas para permitir la implementación de un controlador de eventos para que se pueda recibir información de progreso.</span><span class="sxs-lookup"><span data-stu-id="d180c-120">Demonstrates the use of specific interfaces in order to allow the implementation of an event handler so that progress information may be received.</span></span> <br/>        |
| [<span data-ttu-id="d180c-121">Evitar el cierre de sesión o la suspensión durante una grabación</span><span class="sxs-lookup"><span data-stu-id="d180c-121">Preventing Logoff or Suspend During a Burn</span></span>](preventing-logoff-or-suspend-during-a-burn.md)                     | <span data-ttu-id="d180c-122">Contiene información que detalla las consideraciones de desarrollo de aplicaciones que se deben realizar en lo que respecta a los escenarios que implican el usuario ' Logoff ' y ' Suspend ' en Windows.</span><span class="sxs-lookup"><span data-stu-id="d180c-122">Contains information detailing application development considerations to be made in regards to scenarios involving user 'Logoff' and 'Suspend' in Windows.</span></span><br/> |
| [<span data-ttu-id="d180c-123">Proporcionar permisos de usuario para dispositivos de grabación de multimedia</span><span class="sxs-lookup"><span data-stu-id="d180c-123">Providing User Permissions for Media Burning Devices</span></span>](providing-user-permissions-for-media-burning-devices.md) | <span data-ttu-id="d180c-124">Detalla el proceso necesario para asegurarse de que un usuario tiene los permisos adecuados para el uso de dispositivos de grabación multimedia en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="d180c-124">Details the process required to ensure a user has adequate permissions to utilize media burning devices on Windows XP and Windows Server 2003.</span></span><br/>             |



 

## <a name="application-compatibility"></a><span data-ttu-id="d180c-125">Compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="d180c-125">Application Compatibility</span></span>

<span data-ttu-id="d180c-126">La siguiente documentación contiene información importante que se debe tener en cuenta al desarrollar una aplicación que use IMAPi.</span><span class="sxs-lookup"><span data-stu-id="d180c-126">The following documentation contains important information to take consideration while developing an application that utilizes IMAPI.</span></span>



| <span data-ttu-id="d180c-127">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="d180c-127">Guidance</span></span>                                                   | <span data-ttu-id="d180c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d180c-128">Description</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d180c-129">Distribución de la multisesión de IMAPi</span><span class="sxs-lookup"><span data-stu-id="d180c-129">IMAPI Multisession Layout</span></span>](imapi-multisession-layout.md) | <span data-ttu-id="d180c-130">Detalla el diseño del disco que IMAPi emplea para implementar la multisesión.</span><span class="sxs-lookup"><span data-stu-id="d180c-130">Details the disc layout that IMAPI utilizes to implement multisession.</span></span> <span data-ttu-id="d180c-131">Esta información se utiliza para garantizar la interoperabilidad entre IMAPi y otro software de grabación, además de permitir la creación de imágenes de disco multisesión compatibles con IMAPi.</span><span class="sxs-lookup"><span data-stu-id="d180c-131">This information is used to ensure interoperability between IMAPI and other burning software, as well as allow the creation of IMAPI-compatible multisession disc images.</span></span><br/> |



 

 

 





