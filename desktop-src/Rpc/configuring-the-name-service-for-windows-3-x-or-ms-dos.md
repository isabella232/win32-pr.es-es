---
title: Configurar el servicio de nombres para Windows 3. x o MS-DOS
description: Llamada a procedimiento remoto (RPC) y configurar el servicio de nombres para Windows 3. x o MS-DOS.
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075878"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="cfc47-103">Configurar el servicio de nombres para Windows 3. x o MS-DOS</span><span class="sxs-lookup"><span data-stu-id="cfc47-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="cfc47-104">Al ejecutar Setup.exe para instalar la biblioteca en tiempo de ejecución de RPC de 16 bits, se le pide que seleccione un proveedor de servicios de nombres:</span><span class="sxs-lookup"><span data-stu-id="cfc47-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="cfc47-105">Si elige **instalar proveedor de servicios de nombres predeterminados**, se instalará el NSP predeterminado, localizador de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cfc47-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="cfc47-106">Si elige **instalar proveedor de servicios de nombres personalizados**, complete el cuadro de diálogo **definir dirección de red** para instalar el DCE servicio de directorio de celdas como NSP.</span><span class="sxs-lookup"><span data-stu-id="cfc47-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="cfc47-107">El Servicio de directorio de celdas DCE es el NSP que se usa con servidores DCE.</span><span class="sxs-lookup"><span data-stu-id="cfc47-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="cfc47-108">La dirección de red es el nombre del equipo host que ejecuta el demonio NSI (NSID).</span><span class="sxs-lookup"><span data-stu-id="cfc47-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="cfc47-109">Este equipo actúa como puerta de enlace al Servicio de directorio de celdas de DCE, pasando llamadas a la función NSI entre equipos que ejecutan sistemas operativos de Microsoft y equipos DCE.</span><span class="sxs-lookup"><span data-stu-id="cfc47-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="cfc47-110">La dirección de red puede tener un máximo de 80 caracteres, por ejemplo, 11.1.9.169 es una dirección válida.</span><span class="sxs-lookup"><span data-stu-id="cfc47-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




