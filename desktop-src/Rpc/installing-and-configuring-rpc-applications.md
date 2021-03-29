---
title: Instalación y configuración de aplicaciones RPC
description: Cuando el sistema operativo Microsoft Windows se instala en un servidor o un cliente, el programa de instalación instala automáticamente los archivos de tiempo de ejecución de RPC.
ms.assetid: cfcada3d-cf7c-42a9-9ed4-0b1bba7a98cf
keywords:
- Llamada a procedimiento remoto RPC, tareas, instalación y configuración de aplicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90837261c571276a74bb3a5354c7b9a5db2da6cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487042"
---
# <a name="installing-and-configuring-rpc-applications"></a><span data-ttu-id="24aff-104">Instalación y configuración de aplicaciones RPC</span><span class="sxs-lookup"><span data-stu-id="24aff-104">Installing and Configuring RPC Applications</span></span>

<span data-ttu-id="24aff-105">Cuando el sistema operativo Microsoft Windows se instala en un servidor o un cliente, el programa de instalación instala automáticamente los archivos de tiempo de ejecución de RPC.</span><span class="sxs-lookup"><span data-stu-id="24aff-105">When the Microsoft Windows operating system is installed on a server or client, setup automatically installs the RPC run-time files.</span></span> <span data-ttu-id="24aff-106">No es necesaria ninguna otra instalación de RPC.</span><span class="sxs-lookup"><span data-stu-id="24aff-106">No further RPC installation is required.</span></span> <span data-ttu-id="24aff-107">Sin embargo, debe asegurarse de que la versión de Windows que instale admita todas las características usadas en la aplicación distribuida.</span><span class="sxs-lookup"><span data-stu-id="24aff-107">You must ensure, however, that the version of Windows you install supports all the features used in your distributed application.</span></span>

<span data-ttu-id="24aff-108">Cuando use una aplicación RPC en un sistema operativo Windows 3. x o Microsoft MS-DOS, debe copiar los archivos ejecutables en tiempo de ejecución de RPC en los equipos con Windows 3. x o MS-DOS que vayan a usar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="24aff-108">When you use an RPC application on a Windows 3.x or Microsoft MS-DOS operating system, you must copy the RPC run-time executable files to the Windows 3.x or MS-DOS computers that will be using the application.</span></span> <span data-ttu-id="24aff-109">El directorio \\ mstools \\ RPC \_ RT16 del CD del kit de desarrollo de software (SDK) de la plataforma contiene una imagen de disco de estos archivos junto con un programa de instalación para instalar los archivos.</span><span class="sxs-lookup"><span data-stu-id="24aff-109">The directory \\mstools\\rpc\_rt16 on the Platform Software Development Kit (SDK) CD contains a disk image of these files along with a setup program to install the files.</span></span> <span data-ttu-id="24aff-110">Use esta imagen de disco para crear un disco de instalación para la distribución con la aplicación RPC.</span><span class="sxs-lookup"><span data-stu-id="24aff-110">Use this disk image to create an install disk for distribution with your RPC application.</span></span> <span data-ttu-id="24aff-111">También puede usar aplicaciones cliente de 16 bits destinadas a MS-DOS o Windows en un sistema operativo Windows de 32 bits o 64 bits.</span><span class="sxs-lookup"><span data-stu-id="24aff-111">You can also use 16-bit client applications targeted toward MS-DOS or Windows on a 32-bit/64-bit Windows operating system.</span></span> <span data-ttu-id="24aff-112">Sin embargo, el programa de instalación de la aplicación debe instalar los archivos ejecutables contenidos en esta imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="24aff-112">However, your application's installation program must install the executable files contained in this disk image.</span></span>

<span data-ttu-id="24aff-113">Al compilar una aplicación RPC para un cliente Macintosh, debe vincular los archivos necesarios a la aplicación en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="24aff-113">When you build an RPC application for a Macintosh client, you must link the necessary files to the application at build time.</span></span> <span data-ttu-id="24aff-114">No es necesaria ninguna otra instalación de RPC.</span><span class="sxs-lookup"><span data-stu-id="24aff-114">No additional RPC installation is needed.</span></span>

<span data-ttu-id="24aff-115">Para obtener más información acerca de los archivos redistribuibles y los contratos de licencia, consulteRedist.txt de licencias \\ \\ y \\ \\License.txt de licencias en el CD de Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="24aff-115">For more details about redistributable files and licensing agreements, see \\LICENSE\\Redist.txt and \\LICENSE\\License.txt on the Platform SDK CD.</span></span>

<span data-ttu-id="24aff-116">Esta sección contiene información sobre cómo configurar las aplicaciones RPC en una variedad de plataformas de hardware y software.</span><span class="sxs-lookup"><span data-stu-id="24aff-116">This section contains information about setting up RPC applications on a variety of hardware and software platforms.</span></span> <span data-ttu-id="24aff-117">Presenta la explicación en las secciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="24aff-117">It presents the discussion in the following sections:</span></span>

-   [<span data-ttu-id="24aff-118">Configurar el proveedor de servicios de nombres</span><span class="sxs-lookup"><span data-stu-id="24aff-118">Configuring the Name Service Provider</span></span>](configuring-the-name-service-provider.md)
-   [<span data-ttu-id="24aff-119">Información del registro</span><span class="sxs-lookup"><span data-stu-id="24aff-119">Registry Information</span></span>](registry-information.md)
-   [<span data-ttu-id="24aff-120">Usar RPC con el proxy Winsock</span><span class="sxs-lookup"><span data-stu-id="24aff-120">Using RPC with Winsock Proxy</span></span>](using-rpc-with-winsock-proxy.md)
-   [<span data-ttu-id="24aff-121">Instalación de SPX/IPX</span><span class="sxs-lookup"><span data-stu-id="24aff-121">SPX/IPX Installation</span></span>](spx-ipx-installation.md)
-   [<span data-ttu-id="24aff-122">Configuración del servidor de seguridad</span><span class="sxs-lookup"><span data-stu-id="24aff-122">Configuring the Security Server</span></span>](configuring-the-security-server.md)

 

 




