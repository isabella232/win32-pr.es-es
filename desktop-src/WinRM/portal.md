---
title: Administración remota de Windows
description: Administración remota de Windows (Administración remota de Windows) es la implementación de Microsoft de WS-Management protocolo, un protocolo estándar basado en SOAP y compatible con firewall que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.
ms.assetid: 6429e748-e0bf-431a-8989-db5b211665d5
ms.tgt_platform: multiple
keywords:
- Administración remota de Windows (WinRM), página de inicio
- WS-Management
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbOrient
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27311699fe0321eddc1d3117b17acf3e49e9d518
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995286"
---
# <a name="windows-remote-management"></a><span data-ttu-id="80f79-105">Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="80f79-105">Windows Remote Management</span></span>

## <a name="purpose"></a><span data-ttu-id="80f79-106">Propósito</span><span class="sxs-lookup"><span data-stu-id="80f79-106">Purpose</span></span>

<span data-ttu-id="80f79-107">La Administración remota de Windows (WinRM) es la implementación de Microsoft del [Protocolo WS-Management](ws-management-protocol.md), un protocolo estándar compatible con firewall y basado en el Protocolo simple de acceso a objetos (SOAP) que permite que interoperen el hardware y los sistemas operativos de diferentes proveedores.</span><span class="sxs-lookup"><span data-stu-id="80f79-107">Windows Remote Management (WinRM) is the Microsoft implementation of [WS-Management Protocol](ws-management-protocol.md), a standard Simple Object Access Protocol (SOAP)-based, firewall-friendly protocol that allows hardware and operating systems, from different vendors, to interoperate.</span></span>

<span data-ttu-id="80f79-108">La especificación del protocolo WS-Management proporciona una manera común de que los sistemas tengan acceso a la información de administración de una infraestructura de ti y la intercambie.</span><span class="sxs-lookup"><span data-stu-id="80f79-108">The WS-Management protocol specification provides a common way for systems to access and exchange management information across an IT infrastructure.</span></span> <span data-ttu-id="80f79-109">WinRM y la [*interfaz de administración de plataforma inteligente (IPMI)*](windows-remote-management-glossary.md), junto con el [recopilador de eventos](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) , son componentes de las características de administración de hardware de [Windows](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="80f79-109">WinRM and [*Intelligent Platform Management Interface (IPMI)*](windows-remote-management-glossary.md), along with the [Event Collector](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) are components of the [Windows Hardware Management](/previous-versions/windows/it-pro/windows-server-2003/cc785056(v=ws.10)) features.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="80f79-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="80f79-110">Where applicable</span></span>

<span data-ttu-id="80f79-111">Puede usar objetos de scripting de WinRM, la herramienta de línea de comandos de WinRM o la herramienta de línea de comandos de shell remoto de Windows WinRS para obtener datos de administración de equipos locales y remotos que pueden tener [*controladores de administración de placa base (BMC)*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="80f79-111">You can use WinRM scripting objects, the WinRM command-line tool, or the Windows Remote Shell command line tool WinRS to obtain management data from local and remote computers that may have [*baseboard management controllers (BMCs)*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="80f79-112">Si el equipo ejecuta una versión de sistema operativo basada en Windows que incluye WinRM, [instrumental de administración de Windows (WMI)](/windows/desktop/WmiSdk/wmi-start-page)proporciona los datos de administración.</span><span class="sxs-lookup"><span data-stu-id="80f79-112">If the computer runs a Windows-based operating system version that includes WinRM, the management data is supplied by [Windows Management Instrumentation (WMI)](/windows/desktop/WmiSdk/wmi-start-page).</span></span>

<span data-ttu-id="80f79-113">También puede obtener datos del hardware y del sistema a partir de las implementaciones del protocolo WS-Management que se ejecuten en sistemas operativos diferentes de Windows en su empresa.</span><span class="sxs-lookup"><span data-stu-id="80f79-113">You can also obtain hardware and system data from WS-Management protocol implementations running on operating systems other than Windows in your enterprise.</span></span> <span data-ttu-id="80f79-114">WinRM establece una sesión con un equipo remoto a través del protocolo WS-Management basado en SOAP, en lugar de una conexión a través de DCOM, como hace WMI.</span><span class="sxs-lookup"><span data-stu-id="80f79-114">WinRM establishes a session with a remote computer through the SOAP-based WS-Management protocol rather than a connection through DCOM, as WMI does.</span></span> <span data-ttu-id="80f79-115">Los datos devueltos por el protocolo WS-Management tienen formato XML, en lugar de formato de objeto.</span><span class="sxs-lookup"><span data-stu-id="80f79-115">Data returned to WS-Management protocol are formatted in XML rather than in objects.</span></span>

<span data-ttu-id="80f79-116">El proveedor WMI de [interfaz de administración de plataforma inteligente (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) es un proveedor de WMI estándar con clases que obtienen datos del sensor de BMC de equipos con el hardware adecuado.</span><span class="sxs-lookup"><span data-stu-id="80f79-116">The [Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI provider is a standard WMI provider with classes that obtain BMC sensor data from computers with appropriate hardware.</span></span> <span data-ttu-id="80f79-117">Se puede tener acceso a los datos de IPMI mediante la API de scripting de WinRM, el [scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi)de WMI o las API de [com](/windows/desktop/WmiSdk/com-api-for-wmi) .</span><span class="sxs-lookup"><span data-stu-id="80f79-117">IPMI data can be accessed using the WinRM scripting API, the WMI [Scripting](/windows/desktop/WmiSdk/scripting-api-for-wmi), or [COM](/windows/desktop/WmiSdk/com-api-for-wmi) APIs.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="80f79-118">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="80f79-118">Developer audience</span></span>

<span data-ttu-id="80f79-119">El público del desarrollador es el profesional de ti que escribe scripts para automatizar la administración de servidores o el desarrollador de ISV que obtiene los datos para las aplicaciones de administración.</span><span class="sxs-lookup"><span data-stu-id="80f79-119">The developer audience is the IT Pro who writes scripts to automate the management of servers or the ISV developer obtaining data for management applications.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="80f79-120">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="80f79-120">Run-time requirements</span></span>

<span data-ttu-id="80f79-121">WinRM forma parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="80f79-121">WinRM is part of the operating system.</span></span> <span data-ttu-id="80f79-122">Sin embargo, para obtener datos de equipos remotos, debe configurar un [*agente de escucha*](windows-remote-management-glossary.md#l)de WinRM.</span><span class="sxs-lookup"><span data-stu-id="80f79-122">However, to obtain data from remote computers, you must configure a WinRM [*listener*](windows-remote-management-glossary.md#l).</span></span> <span data-ttu-id="80f79-123">Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="80f79-123">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="80f79-124">Si se detecta un BMC al iniciar el sistema, se carga el proveedor IPMI; de lo contrario, los objetos de scripting de WinRM y la herramienta de línea de comandos de WinRM seguirán estando disponibles.</span><span class="sxs-lookup"><span data-stu-id="80f79-124">If a BMC is detected at system startup, then the IPMI provider loads; otherwise, the WinRM scripting objects and the WinRM command-line tool are still available.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="80f79-125">En esta sección</span><span class="sxs-lookup"><span data-stu-id="80f79-125">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="80f79-126">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="80f79-126">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="80f79-127">Vínculo a la especificación del protocolo público WS-Management, la arquitectura de WinRM, la relación con WMI, la administración de hardware con el proveedor IPMI, la configuración y la instalación.</span><span class="sxs-lookup"><span data-stu-id="80f79-127">Link to public WS-Management protocol specification, WinRM architecture, relationship to WMI, hardware management with the IPMI provider, configuration and installation.</span></span>

</dd> <dt>

[<span data-ttu-id="80f79-128">Usar Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="80f79-128">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dd>

<span data-ttu-id="80f79-129">Introducción al uso de la API de scripting de WinRM y la administración de hardware.</span><span class="sxs-lookup"><span data-stu-id="80f79-129">Getting started using the WinRM scripting API and hardware management.</span></span>

</dd> <dt>

[<span data-ttu-id="80f79-130">Referencia de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="80f79-130">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> <dd>

<span data-ttu-id="80f79-131">Lista de interfaces de scripting definidas por los servicios Web de Microsoft para la automatización de administración (WS-Management) y las definiciones de clase de las clases WMI creadas por el proveedor IPMI y las clases que se comunican con el controlador IPMI para obtener los datos del [controlador de administración de placa base (BMC)](windows-remote-management-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="80f79-131">List of scripting interfaces defined by Microsoft Web Services for Management (WS-Management) Automation and class definitions of the WMI classes created by the IPMI provider and classes that communicate with the IPMI driver to obtain [baseboard management controller (BMC)](windows-remote-management-glossary.md) data.</span></span>

</dd> </dl>

 

 