---
title: Extender Terminal Services agente de sesiones
description: Puede extender TS \ 160; Agente de sesiones mediante la interfaz COM IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793119"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="d5acb-103">Extender Terminal Services agente de sesiones</span><span class="sxs-lookup"><span data-stu-id="d5acb-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="d5acb-104">Terminal Services agente de sesiones (agente de sesiones de TS) determina si un usuario que inicia una conexión ya tiene una sesión abierta.</span><span class="sxs-lookup"><span data-stu-id="d5acb-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="d5acb-105">Si es así, el agente de sesiones de TS enruta la conexión entrante al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) con la sesión existente.</span><span class="sxs-lookup"><span data-stu-id="d5acb-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="d5acb-106">De lo contrario, el agente de sesiones de TS enruta la conexión entrante al servidor host de sesión de escritorio remoto con el menor número de sesiones.</span><span class="sxs-lookup"><span data-stu-id="d5acb-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="d5acb-107">Puede extender el agente de sesiones de TS mediante la interfaz com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="d5acb-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="d5acb-108">Puede usar esta interfaz para administrar las conexiones a los servidores host de sesión de escritorio remoto, así como a cualquier tipo de conexión Protocolo de escritorio remoto (RDP), por ejemplo, las conexiones a las máquinas virtuales invitadas que ejecutan el escritorio centralizado de Windows Vista Enterprise (VECD) en un host de máquina virtual de Hyper-V de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d5acb-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="d5acb-109">La interfaz [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) ofrece varias ventajas:</span><span class="sxs-lookup"><span data-stu-id="d5acb-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="d5acb-110">No es necesario instalar un agente en el cliente o en el servidor host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d5acb-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="d5acb-111">El complemento puede interactuar sin problemas con otros servicios de rol de Servicios de Escritorio remoto, como Escritorio remoto puerta de enlace de RD, y basarse en la información del agente de sesiones de TS sobre los Estados de sesión y equipo.</span><span class="sxs-lookup"><span data-stu-id="d5acb-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="d5acb-112">Puede usar el complemento para administrar conexiones con dispositivos cliente o servidor que admitan RDP 5,2 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d5acb-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="d5acb-113">Puede usar el complemento para habilitar las soluciones de escritorio centralizadas de Windows Vista Enterprise.</span><span class="sxs-lookup"><span data-stu-id="d5acb-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="d5acb-114">Cuando implemente los métodos de esta interfaz, tenga en cuenta los puntos siguientes:</span><span class="sxs-lookup"><span data-stu-id="d5acb-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="d5acb-115">El agente de sesiones de TS podría llamar a los métodos de este objeto COM desde varios subprocesos.</span><span class="sxs-lookup"><span data-stu-id="d5acb-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="d5acb-116">Si alguno de los métodos a los que se llama no vuelve inmediatamente y correctamente, el agente de sesiones de TS no realiza más llamadas al complemento y revierte a su lógica de equilibrio de carga nativa.</span><span class="sxs-lookup"><span data-stu-id="d5acb-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="d5acb-117">Para reanudar las llamadas al complemento, debe reiniciar el servicio agente de sesiones de Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="d5acb-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="d5acb-118">Debe registrar el complemento como un objeto COM en todo el sistema mediante Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="d5acb-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="d5acb-119">Dado que el servicio agente de sesiones de Terminal Services se ejecuta bajo la cuenta "NetworkService", debe proporcionar a la cuenta "NetworkService" los permisos de inicio, activación y acceso necesarios mediante Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="d5acb-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="d5acb-120">El servicio agente de sesiones de Terminal Services busca el CLSID del objeto COM que representa el complemento en la subclave del Registro siguiente:</span><span class="sxs-lookup"><span data-stu-id="d5acb-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="d5acb-121">**HKEY \_ \_** Parámetros de Tssdis de sistema de equipo local de \\  \\ **CurrentControlSet** \\ **Services** \\  \\  \\ **ExtensibilityPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="d5acb-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="d5acb-122">Para obtener más información acerca de Dcomcnfg.exe, vea [Habilitar la seguridad de com mediante DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="d5acb-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5acb-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5acb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5acb-124">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="d5acb-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 