---
title: 'Compatibilidad de cliente y servidor: Windows 8'
description: Compatibilidad de servidor y cliente de Windows 8 y Windows Server 2012
ms.assetid: 5067219A-EBA2-4FAF-8C17-7AB22C5EADD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca5b685ae10b97a7b8197737944ea7231d226514
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2019
ms.locfileid: "104358583"
---
# <a name="windows-8-and-windows-server-2012-client-and-server-compatibility"></a><span data-ttu-id="3319b-103">Compatibilidad de servidor y cliente de Windows 8 y Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3319b-103">Windows 8 and Windows Server 2012 client and server compatibility</span></span>

<span data-ttu-id="3319b-104">En esta sección se describen los cambios en el sistema operativo a los que debe prestar atención especial debido a los posibles impactos en las aplicaciones existentes y cómo deben diseñarse las nuevas aplicaciones en los clientes, en servidores o en clientes y servidores.</span><span class="sxs-lookup"><span data-stu-id="3319b-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="3319b-105">A continuación se muestra la lista de temas que se tratan en esta sección, agrupados por área de características:</span><span class="sxs-lookup"><span data-stu-id="3319b-105">Following is the list of topics covered in this section, grouped by feature area:</span></span>

<span data-ttu-id="3319b-106">**AppCompat**</span><span class="sxs-lookup"><span data-stu-id="3319b-106">**AppCompat**</span></span>

-   <span data-ttu-id="3319b-107">Actualización de reglas de detección de aplicaciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="3319b-107">Security app detection rules update</span></span>
-   <span data-ttu-id="3319b-108">Determinar el estado de la corrección de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="3319b-108">Determining shim status</span></span>
-   <span data-ttu-id="3319b-109">Las aplicaciones de servidor deben poder ejecutarse sin el shell gráfico de servidor</span><span class="sxs-lookup"><span data-stu-id="3319b-109">Server apps must be able to run without the Server Graphical Shell</span></span>
-   <span data-ttu-id="3319b-110">Los componentes de servidor RDS se quitan de Windows 8</span><span class="sxs-lookup"><span data-stu-id="3319b-110">RDS server components are removed from Windows 8</span></span>
-   <span data-ttu-id="3319b-111">Modelo de tipo de archivo y asociaciones de protocolo</span><span class="sxs-lookup"><span data-stu-id="3319b-111">File type and protocol associations model</span></span>
-   <span data-ttu-id="3319b-112">Moderador de la actividad del escritorio</span><span class="sxs-lookup"><span data-stu-id="3319b-112">Desktop Activity Moderator</span></span>
-   <span data-ttu-id="3319b-113">.NET Framework 4,5 es el valor predeterminado y .NET Framework 3,5 es opcional</span><span class="sxs-lookup"><span data-stu-id="3319b-113">.NET Framework 4.5 is default and .NET Framework 3.5 is optional</span></span>
-   <span data-ttu-id="3319b-114">Es posible que las aplicaciones de escritorio no estén visibles después de iniciar el explorador Web predeterminado</span><span class="sxs-lookup"><span data-stu-id="3319b-114">Desktop apps may not be visible after launching the default web browser</span></span>
-   <span data-ttu-id="3319b-115">Modo de contraste alto</span><span class="sxs-lookup"><span data-stu-id="3319b-115">High-contrast mode</span></span>
-   <span data-ttu-id="3319b-116">Manifiesto de aplicación (ejecutable)</span><span class="sxs-lookup"><span data-stu-id="3319b-116">App (executable) manifest</span></span>
-   <span data-ttu-id="3319b-117">El modelo de presentación en cola está en desuso</span><span class="sxs-lookup"><span data-stu-id="3319b-117">Queued present model is being deprecated</span></span>
-   <span data-ttu-id="3319b-118">Escenarios del Asistente para la compatibilidad de programas para Windows 8</span><span class="sxs-lookup"><span data-stu-id="3319b-118">Program Compatibility Assistant scenarios for Windows 8</span></span>
-   <span data-ttu-id="3319b-119">Gadgets de escritorio quitados</span><span class="sxs-lookup"><span data-stu-id="3319b-119">Desktop gadgets removed</span></span>

<span data-ttu-id="3319b-120">**Almacenamiento y sistema de archivos**</span><span class="sxs-lookup"><span data-stu-id="3319b-120">**Storage and File System**</span></span>

-   <span data-ttu-id="3319b-121">Actualización de compatibilidad de disco Advanced Format (4K)</span><span class="sxs-lookup"><span data-stu-id="3319b-121">Advanced format (4K) disk compatibility update</span></span>
-   <span data-ttu-id="3319b-122">Aprovisionamiento fino de unidades lógicas</span><span class="sxs-lookup"><span data-stu-id="3319b-122">Thin provisioning of logical units</span></span>
-   <span data-ttu-id="3319b-123">El almacenamiento mejorado ahora es opcional para el Entorno de preinstalación de Windows (WinPE) y el SKU de servidor</span><span class="sxs-lookup"><span data-stu-id="3319b-123">Enhanced storage is now optional for Windows Preinstallation Environment (WinPE) and server SKU</span></span>
-   <span data-ttu-id="3319b-124">El servicio de disco virtual está cambiando a la API de administración de almacenamiento de Windows basada en Instrumental de administración de Windows (WMI)</span><span class="sxs-lookup"><span data-stu-id="3319b-124">Virtual Disk Service is transitioning to the Windows Management Instrumentation (WMI)-based Windows Storage Management API</span></span>
-   <span data-ttu-id="3319b-125">Interfaz de usuario de versiones anteriores quitada para volúmenes locales</span><span class="sxs-lookup"><span data-stu-id="3319b-125">Previous versions UI removed for local volumes</span></span>
-   <span data-ttu-id="3319b-126">StorAHCI reemplaza a MSAHCI</span><span class="sxs-lookup"><span data-stu-id="3319b-126">StorAHCI replaces MSAHCI</span></span>
-   <span data-ttu-id="3319b-127">Copias de seguridad y restauración de Windows 7 en desuso</span><span class="sxs-lookup"><span data-stu-id="3319b-127">Windows 7 backup and restore deprecated</span></span>
-   <span data-ttu-id="3319b-128">Transferencias de datos descargados</span><span class="sxs-lookup"><span data-stu-id="3319b-128">Offloaded data transfers</span></span>

<span data-ttu-id="3319b-129">**Otros**</span><span class="sxs-lookup"><span data-stu-id="3319b-129">**Other**</span></span>

-   <span data-ttu-id="3319b-130">Administrador de ventanas de escritorio está siempre activado</span><span class="sxs-lookup"><span data-stu-id="3319b-130">Desktop Window Manager is always on</span></span>
-   <span data-ttu-id="3319b-131">Direct2D no admite la representación en metaarchivos "ricos" en Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="3319b-131">Direct2D does not support rendering to "rich" metafiles in Internet Explorer 9</span></span>
-   <span data-ttu-id="3319b-132">Cambios en la compatibilidad con hardware heredado de DX9</span><span class="sxs-lookup"><span data-stu-id="3319b-132">Changes in DX9 legacy hardware support</span></span>
-   <span data-ttu-id="3319b-133">MSAA no está disponible para las aplicaciones de la tienda Windows</span><span class="sxs-lookup"><span data-stu-id="3319b-133">MSAA is not available to Windows Store apps</span></span>
-   <span data-ttu-id="3319b-134">El puerto 3 está en desuso para los controladores NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="3319b-134">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

 

 
