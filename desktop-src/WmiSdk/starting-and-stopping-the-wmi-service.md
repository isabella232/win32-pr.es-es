---
description: WMI se ejecuta como un servicio con el nombre para mostrar &\# 0034; Instrumental de administración de Windows&\# 0034 y el nombre del servicio &\# 0034; winmgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Iniciar y detener el servicio WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276131"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="94750-103">Iniciar y detener el servicio WMI</span><span class="sxs-lookup"><span data-stu-id="94750-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="94750-104">WMI se ejecuta como un servicio con el nombre para mostrar "Instrumental de administración de Windows" y el nombre de servicio "WinMgmt".</span><span class="sxs-lookup"><span data-stu-id="94750-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="94750-105">WMI se ejecuta automáticamente al iniciar el sistema en la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="94750-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="94750-106">Si WMI no se está ejecutando, se inicia automáticamente cuando la primera aplicación de administración o el script solicita la conexión a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="94750-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="94750-107">Otros servicios dependen del servicio WMI, en función de la versión del sistema operativo que esté ejecutando el sistema.</span><span class="sxs-lookup"><span data-stu-id="94750-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="94750-108">Iniciando el servicio WinMgmt</span><span class="sxs-lookup"><span data-stu-id="94750-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="94750-109">En el procedimiento siguiente se describe cómo iniciar el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="94750-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="94750-110">**Para iniciar el servicio WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="94750-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="94750-111">En un símbolo del sistema, escriba **net** **Start** **WinMgmt** \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="94750-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="94750-112">Para obtener más información acerca de los modificadores que están disponibles, vea [WinMgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="94750-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="94750-113">Use la cuenta predefinida Administrador o una cuenta en el grupo administradores que se ejecuta con permisos elevados para iniciar el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="94750-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="94750-114">Para obtener más información, vea [control de cuentas de usuario y WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="94750-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="94750-115">Otros servicios que dependen del servicio WMI, como el host de agente de SMS o el Firewall de Windows, no se reiniciarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="94750-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="94750-116">Deteniendo el servicio WinMgmt</span><span class="sxs-lookup"><span data-stu-id="94750-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="94750-117">En el procedimiento siguiente se describe cómo detener el servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="94750-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="94750-118">**Para detener el servicio WinMgmt**</span><span class="sxs-lookup"><span data-stu-id="94750-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="94750-119">En un símbolo del sistema, escriba **net stop WinMgmt**.</span><span class="sxs-lookup"><span data-stu-id="94750-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="94750-120">Otros servicios que dependen del servicio WMI también se detienen, como el host de agente de SMS o el Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="94750-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="94750-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="94750-121">Examples</span></span>

<span data-ttu-id="94750-122">La galería de TechNet contiene el [script de vigilancia del servicio WMI](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), que describe cómo cerrar y reiniciar el servicio WinMgmt mediante programación con PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94750-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94750-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="94750-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94750-124">Uso de las herramientas de Command-Line WMI</span><span class="sxs-lookup"><span data-stu-id="94750-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



