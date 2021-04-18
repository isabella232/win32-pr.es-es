---
title: Usar Servicios de Escritorio remoto
description: Cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac575a89d1ae8c7c065199aca136f2f0e5fc7459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685552"
---
# <a name="using-remote-desktop-services"></a><span data-ttu-id="43662-104">Usar Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-104">Using Remote Desktop Services</span></span>

<span data-ttu-id="43662-105">En las secciones siguientes se describe cómo programar en el entorno de Servicios de Escritorio remoto y cómo extender la tecnología de Servicios de Escritorio remoto (antes conocida como Terminal Services) a la web mediante el uso de Conexión web a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="43662-105">The following sections describe how to program in the Remote Desktop Services environment and how to extend Remote Desktop Services (formerly known as Terminal Services) technology to the web by using Remote Desktop Web Connection.</span></span> <span data-ttu-id="43662-106">Si está buscando información de usuario para conexiones Escritorio remoto, consulte [conectarse a otro equipo mediante conexión a escritorio remoto](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span><span class="sxs-lookup"><span data-stu-id="43662-106">If you are looking for user information for Remote Desktop connections, See [Connect to another computer using Remote Desktop Connection](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).</span></span>

> [!Note]  
> <span data-ttu-id="43662-107">Este tema está destinado a los desarrolladores de software.</span><span class="sxs-lookup"><span data-stu-id="43662-107">This topic is for software developers.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="43662-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="43662-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="43662-109">Detectar si está instalado el rol de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-109">Detecting Whether the Remote Desktop Services Role Is Installed</span></span>](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

<span data-ttu-id="43662-110">Ejemplo de código de C# que muestra un método que devuelve **true** si la función de servidor servicios de escritorio remoto está instalada y en ejecución, o **false** en caso contrario, a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="43662-110">C# code example that shows a method that returns **True** if the Remote Desktop Services server role is installed and running or **false** otherwise, beginning with Windows Server 2008.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-111">Extender Terminal Services agente de sesiones</span><span class="sxs-lookup"><span data-stu-id="43662-111">Extending Terminal Services Session Broker</span></span>](extending-ts-session-broker.md)
</dt> <dd>

<span data-ttu-id="43662-112">Puede extender el agente de sesiones de TS mediante la interfaz com [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .</span><span class="sxs-lookup"><span data-stu-id="43662-112">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-113">Implementación de un enumerador de punto de conexión de audio personalizado</span><span class="sxs-lookup"><span data-stu-id="43662-113">Implementing a Custom Audio Endpoint Enumerator</span></span>](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

<span data-ttu-id="43662-114">A partir de Windows Server 2008 R2, puede implementar un enumerador de punto de conexión de audio remoto personalizado como parte de un proveedor de protocolo Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="43662-114">Beginning with Windows Server 2008 R2, you can implement a custom remote audio endpoint enumerator as part of a Remote Desktop protocol provider.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-115">Monikers de sesión</span><span class="sxs-lookup"><span data-stu-id="43662-115">Session Monikers</span></span>](session-monikers.md)
</dt> <dd>

<span data-ttu-id="43662-116">COM distribuido (DCOM) permite la activación de objetos por sesión mediante el uso de un moniker de sesión proporcionado por el sistema.</span><span class="sxs-lookup"><span data-stu-id="43662-116">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied session moniker.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-117">Uso de la extensión ADSI para Servicios de Escritorio remoto la configuración de usuario</span><span class="sxs-lookup"><span data-stu-id="43662-117">Using the ADSI Extension for Remote Desktop Services User Configuration</span></span>](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

<span data-ttu-id="43662-118">La administración de propiedades de usuario específicas de Servicios de Escritorio remoto es posible mediante el uso de los métodos implementados por la extensión de interfaces de servicio Active Directory (ADSI), que se incluye con la biblioteca de vínculos dinámicos Tsuserex.dll.</span><span class="sxs-lookup"><span data-stu-id="43662-118">Administration of Remote Desktop Services-specific user properties is possible by using the methods implemented by the Active Directory Service Interfaces (ADSI) extension, which is packaged with the dynamic-link library Tsuserex.dll.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-119">Uso de la API de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-119">Using the Remote Desktop Services API</span></span>](using-the-terminal-services-api.md)
</dt> <dd>

<span data-ttu-id="43662-120">Describe cómo puede usar la API de Servicios de Escritorio remoto para permitir que las aplicaciones realicen tareas en un entorno de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="43662-120">Describes how you can use the Remote Desktop Services API to enable applications to perform tasks in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-121">Uso de la API de virtualización de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-121">Using the Remote Desktop Virtualization API</span></span>](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

<span data-ttu-id="43662-122">Los desarrolladores pueden usar esta API para personalizar la lógica que usa Conexión a Escritorio remoto Broker (agente de conexión a escritorio remoto) para determinar el mejor destino para una conexión de cliente entrante.</span><span class="sxs-lookup"><span data-stu-id="43662-122">Developers can use this API to customize the logic that Remote Desktop Connection Broker (RD Connection Broker) uses to determine the best destination for an incoming client connection.</span></span>

</dd> <dt>

[<span data-ttu-id="43662-123">Interfaz WSDL para soluciones VDI personalizadas</span><span class="sxs-lookup"><span data-stu-id="43662-123">WSDL Interface for Custom VDI Solutions</span></span>](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

<span data-ttu-id="43662-124">Los desarrolladores pueden crear servicios web personalizados que administren soluciones de infraestructura de escritorio virtual (VDI).</span><span class="sxs-lookup"><span data-stu-id="43662-124">Developers can create custom web services that manage virtual desktop infrastructure (VDI) solutions.</span></span>

</dd> </dl>

<span data-ttu-id="43662-125">Para obtener más información, vea [instrucciones de programación de servicios de escritorio remoto](terminal-services-programming-guidelines.md).</span><span class="sxs-lookup"><span data-stu-id="43662-125">For more information, see [Remote Desktop Services Programming Guidelines](terminal-services-programming-guidelines.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="43662-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43662-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43662-127">Terminal Services es ahora Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-127">Terminal Services Is Now Remote Desktop Services</span></span>](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[<span data-ttu-id="43662-128">Detección del entorno de Servicios de Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="43662-128">Detecting the Remote Desktop Services Environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




