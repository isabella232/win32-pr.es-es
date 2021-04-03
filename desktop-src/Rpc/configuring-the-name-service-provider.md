---
title: Configurar el proveedor de servicios de nombres
description: Si la aplicación distribuida registra su interfaz con un servicio de nombres, tanto el cliente como el servidor deben usar el mismo servicio de nombres.
ms.assetid: a3f201e1-1a01-4794-9026-05e51a96afc0
keywords:
- RPC llamada a procedimiento remoto, tareas, configurar proveedor de servicios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7a44ec9a1c83eb7c37f10caae6ca3870679bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075702"
---
# <a name="configuring-the-name-service-provider"></a><span data-ttu-id="d6d83-104">Configurar el proveedor de servicios de nombres</span><span class="sxs-lookup"><span data-stu-id="d6d83-104">Configuring the Name Service Provider</span></span>

<span data-ttu-id="d6d83-105">Si la aplicación distribuida registra su interfaz con un servicio de nombres, tanto el cliente como el servidor deben usar el mismo servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="d6d83-105">If your distributed application registers its interface with a name service, both the client and server must be using the same name service.</span></span> <span data-ttu-id="d6d83-106">Microsoft RPC interopera con el localizador de Microsoft y cualquier proveedor de servicios de nombres (NSP) que se adhiere a la interfaz de servicio de nombres RPC (NSI) de Microsoft, por ejemplo, el DCE Servicio de directorio de celdas tener acceso a través del demonio de servicio de nombres de Digital Equipment Corporation (NSID).</span><span class="sxs-lookup"><span data-stu-id="d6d83-106">Microsoft RPC interoperates with Microsoft Locator and any name service provider (NSP) that adheres to the Microsoft RPC name service interface (NSI)—for example, the DCE Cell Directory Service accessed through Digital Equipment Corporation's name service daemon (NSID).</span></span> <span data-ttu-id="d6d83-107">El localizador de Microsoft, que está diseñado para su uso en entornos Windows, es el proveedor de servicios de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d6d83-107">Microsoft Locator, which is designed for use in Windows environments, is the default name service provider.</span></span>

<span data-ttu-id="d6d83-108">En esta sección se presenta una descripción de la instalación y configuración de proveedores de servicios de nombres:</span><span class="sxs-lookup"><span data-stu-id="d6d83-108">This section presents a discussion of installing and configuring name service providers:</span></span>

-   [<span data-ttu-id="d6d83-109">Configuración del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6d83-109">Configuring the Name Service</span></span>](configuring-the-name-service-for-windows-xp-windows-2000-or-windows-nt.md)
-   [<span data-ttu-id="d6d83-110">Configurar el servicio de nombres para Windows 95</span><span class="sxs-lookup"><span data-stu-id="d6d83-110">Configuring the Name Service for Windows 95</span></span>](configuring-the-name-service-for-windows-95.md)
-   [<span data-ttu-id="d6d83-111">Configurar el servicio de nombres para Windows 3. x o MS-DOS</span><span class="sxs-lookup"><span data-stu-id="d6d83-111">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>](configuring-the-name-service-for-windows-3-x-or-ms-dos.md)
-   [<span data-ttu-id="d6d83-112">Iniciar y detener el localizador de Microsoft</span><span class="sxs-lookup"><span data-stu-id="d6d83-112">Starting and Stopping Microsoft Locator</span></span>](starting-and-stopping-microsoft-locator.md)

 

 




