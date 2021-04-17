---
description: En el siguiente procedimiento se muestra cómo depurar un monitor.
ms.assetid: 499f409c-e25a-4ab3-b0aa-e6b308fc7169
title: Depurar un monitor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4641818b7f1cd1740c2732ced5527a2e278793a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545382"
---
# <a name="debugging-a-monitor"></a><span data-ttu-id="62fc7-103">Depurar un monitor</span><span class="sxs-lookup"><span data-stu-id="62fc7-103">Debugging a Monitor</span></span>

<span data-ttu-id="62fc7-104">En el siguiente procedimiento se muestra cómo depurar un monitor.</span><span class="sxs-lookup"><span data-stu-id="62fc7-104">The following procedure demonstrates how to debug a monitor.</span></span>

<span data-ttu-id="62fc7-105">**Para depurar un monitor**</span><span class="sxs-lookup"><span data-stu-id="62fc7-105">**To debug a monitor**</span></span>

1.  <span data-ttu-id="62fc7-106">Instale el archivo DLL del monitor y el archivo de base de datos de programa (. pdb) que se genera al compilar el monitor en la ubicación correcta.</span><span class="sxs-lookup"><span data-stu-id="62fc7-106">Install the monitor DLL and the program database (.pdb) file generated when you compiled the monitor in the correct location.</span></span> <span data-ttu-id="62fc7-107">Consulte [instalación de un monitor en monitor de red](installing-a-monitor-to-network-monitor.md) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="62fc7-107">See [Installing a Monitor to Network Monitor](installing-a-monitor-to-network-monitor.md) for further details.</span></span>
2.  <span data-ttu-id="62fc7-108">Compruebe que el servicio de control de supervisión está configurado como un servidor en lugar de un servicio seleccionando panel de control, servicios.</span><span class="sxs-lookup"><span data-stu-id="62fc7-108">Verify that the Monitor Control Service is configured as a server instead of a service by selecting Control Panel, Services.</span></span>
3.  <span data-ttu-id="62fc7-109">Abra un símbolo del sistema y vaya al directorio Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="62fc7-109">Open a command prompt and go to the Network Monitor directory.</span></span> <span data-ttu-id="62fc7-110">Escriba:</span><span class="sxs-lookup"><span data-stu-id="62fc7-110">Type:</span></span>

    <span data-ttu-id="62fc7-111">**Mcsvc.exe/RegServer**</span><span class="sxs-lookup"><span data-stu-id="62fc7-111">**Mcsvc.exe /RegServer**</span></span>

    <span data-ttu-id="62fc7-112">Una vez completada la sesión de depuración del monitor, puede devolver el valor de MCSVC a su condición predeterminada; para ello, escriba:</span><span class="sxs-lookup"><span data-stu-id="62fc7-112">After the monitor debugging session is complete, you can return the MCSVC to its default condition by typing:</span></span>

    <span data-ttu-id="62fc7-113">**Mcsvc.exe/Service**</span><span class="sxs-lookup"><span data-stu-id="62fc7-113">**Mcsvc.exe /Service**</span></span>

4.  <span data-ttu-id="62fc7-114">En Microsoft Visual Studio, Inicie Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="62fc7-114">In Microsoft Visual Studio, launch Microsoft Visual C++.</span></span>
5.  <span data-ttu-id="62fc7-115">En la opción de menú **archivo**, **abrir** , seleccione el nombre de la dll del monitor.</span><span class="sxs-lookup"><span data-stu-id="62fc7-115">From the **File**, **Open** menu option, select the name of your monitor DLL.</span></span>
6.  <span data-ttu-id="62fc7-116">Después de cargar Microsoft Visual C++, haga clic en **proyecto**, **configuración**.</span><span class="sxs-lookup"><span data-stu-id="62fc7-116">After Microsoft Visual C++ loads, click **Project**, **Settings**.</span></span>
7.  <span data-ttu-id="62fc7-117">Haga clic en la pestaña **depurar** en **ejecutable** para sesión de depuración y escriba la ruta de acceso completa de Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="62fc7-117">Click the **Debug** tab under **Executable** for debug session and type the full path of Mcsvc.exe.</span></span> <span data-ttu-id="62fc7-118">Por ejemplo, C: \\ archivos de programa \\ Netmon2 \\Mcsvc.exe.</span><span class="sxs-lookup"><span data-stu-id="62fc7-118">For example, C:\\Program files\\Netmon2\\Mcsvc.exe.</span></span>
8.  <span data-ttu-id="62fc7-119">Establezca los puntos de interrupción en el código.</span><span class="sxs-lookup"><span data-stu-id="62fc7-119">Set the breakpoints in the code.</span></span>

> [!Note]  
> <span data-ttu-id="62fc7-120">No use un cuadro de mensaje para la depuración de monitores.</span><span class="sxs-lookup"><span data-stu-id="62fc7-120">Do not use a message box for monitor debugging.</span></span> <span data-ttu-id="62fc7-121">Si el MCSVC se ejecuta como un servicio, no verá el elemento emergente y MCSVC parecerá que deja de responder.</span><span class="sxs-lookup"><span data-stu-id="62fc7-121">If the MCSVC is running as a service, you will not see the popup, and MCSVC will appear to hang.</span></span>

 

 

 



