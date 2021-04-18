---
title: Directrices para varios usuarios
description: Directrices para desarrollar aplicaciones para varios usuarios en un entorno de Servicios de Escritorio remoto.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685618"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="34f10-103">Directrices para varios usuarios</span><span class="sxs-lookup"><span data-stu-id="34f10-103">Multiple-user guidelines</span></span>

<span data-ttu-id="34f10-104">En las secciones siguientes se proporcionan instrucciones para desarrollar aplicaciones para varios usuarios en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="34f10-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="34f10-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="34f10-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="34f10-106">Configuración de la aplicación</span><span class="sxs-lookup"><span data-stu-id="34f10-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="34f10-107">La instalación de una aplicación para un solo usuario puede crear problemas en un entorno de Servicios de Escritorio remoto multiusuario.</span><span class="sxs-lookup"><span data-stu-id="34f10-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="34f10-108">Almacenar información específica del usuario</span><span class="sxs-lookup"><span data-stu-id="34f10-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="34f10-109">Las aplicaciones deben almacenar información específica del usuario en ubicaciones específicas del usuario, aparte de la información global que se aplica a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="34f10-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="34f10-110">Espacios de nombres de objetos de kernel</span><span class="sxs-lookup"><span data-stu-id="34f10-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="34f10-111">Servicios de Escritorio remoto utiliza varios espacios de nombres para los objetos de kernel; un espacio de nombres global se usa principalmente en los servicios de las aplicaciones cliente/servidor.</span><span class="sxs-lookup"><span data-stu-id="34f10-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="34f10-112">Direcciones IP y nombres de equipo</span><span class="sxs-lookup"><span data-stu-id="34f10-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="34f10-113">No es seguro suponer que el nombre del equipo o la dirección IP que se asignen al equipo se asocian a un único usuario, dado que varios usuarios pueden iniciar sesión a la vez en un servidor host de sesión de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="34f10-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="34f10-114">Como siempre, bloquee los archivos y las bases de datos mientras realiza cambios para evitar la pérdida accidental de datos.</span><span class="sxs-lookup"><span data-stu-id="34f10-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="34f10-115">La aplicación no debe bloquear ningún archivo de aplicación en tiempo de ejecución que no sea un archivo por usuario.</span><span class="sxs-lookup"><span data-stu-id="34f10-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="34f10-116">Los archivos de tiempo de ejecución bloqueados pueden mantener varias instancias de la aplicación o los procesos de la aplicación, como los asistentes, no se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="34f10-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="34f10-117">Una buena manera de comprobar qué archivos son los archivos de aplicación en tiempo de ejecución es realizar un seguimiento de los archivos que instala el programa de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34f10-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="34f10-118">Los archivos por usuario rara vez se instalan con el programa de instalación; por lo tanto, la mayoría de los archivos instalados por el programa de instalación son archivos de aplicación en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="34f10-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




