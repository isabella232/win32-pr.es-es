---
title: Administrador de conexiones
description: Los clientes que deseen desarrollar marcadores personalizados mediante la API del servicio de acceso remoto pueden investigar el administrador de conexiones de Microsoft y el kit de administración de Connection Manager.
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077380"
---
# <a name="connection-manager"></a><span data-ttu-id="6e823-103">Administrador de conexiones</span><span class="sxs-lookup"><span data-stu-id="6e823-103">Connection Manager</span></span>

<span data-ttu-id="6e823-104">Los clientes que deseen desarrollar marcadores personalizados mediante la API del servicio de acceso remoto pueden investigar el administrador de conexiones de Microsoft y el kit de administración de Connection Manager.</span><span class="sxs-lookup"><span data-stu-id="6e823-104">Customers who intend to develop custom dialers using the Remote Access Service API may want to investigate Microsoft Connection Manager and the Connection Manager Administration Kit.</span></span> <span data-ttu-id="6e823-105">El administrador de conexiones es el cliente de acceso remoto administrado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6e823-105">Connection Manager is Microsoft's managed remote access client.</span></span> <span data-ttu-id="6e823-106">Permite a un administrador crear un paquete de configuración de acceso remoto que se va a distribuir a los usuarios remotos del administrador.</span><span class="sxs-lookup"><span data-stu-id="6e823-106">It allows an administrator to build a remote access configuration package to be distributed to the administrator's remote users.</span></span> <span data-ttu-id="6e823-107">Para obtener más información sobre el administrador de conexiones y el kit de administración de Connection Manager, vea la ayuda en pantalla de Microsoft Windows 2000 Server y los sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="6e823-107">For more information on Connection Manager and the Connection Manager Administration Kit, see the online help for Microsoft Windows 2000 Server and later operating systems.</span></span>

<span data-ttu-id="6e823-108">Puede encontrar el código fuente de una acción personalizada del administrador de conexiones de ejemplo en el kit de desarrollo de software (SDK) completo de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="6e823-108">You can find the source code for a sample Connection Manager custom action in the complete Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="6e823-109">El SDK de la plataforma se puede descargar en el [sitio web de Microsoft](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6e823-109">The Platform SDK can be downloaded at the [Microsoft Web site](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="6e823-110">Después de la instalación, la ruta de acceso al código de ejemplo es% install path% \\ Microsoft SDK \\ Samples \\ netds \\ ras \\ ConnectionManager, donde% install path% designa el directorio de instalación base del SDK de la plataforma (por ejemplo, C: \\ archivos de programa).</span><span class="sxs-lookup"><span data-stu-id="6e823-110">After installation, the path to the sample code is %Install Path%\\Microsoft SDK\\Samples\\netds\\Ras\\ConnectionManager, where %Install Path% designates the base installation directory of the Platform SDK (for example, C:\\Program Files).</span></span>

<span data-ttu-id="6e823-111">Las acciones personalizadas permiten que el cliente de acceso remoto realice acciones específicas en varios puntos del proceso de conexión.</span><span class="sxs-lookup"><span data-stu-id="6e823-111">Custom actions make it possible for the remote access client to take specific actions at various points in the connection process.</span></span> <span data-ttu-id="6e823-112">La acción personalizada que se muestra en el ejemplo ajusta automáticamente la configuración del servidor proxy para una conexión basada en la dirección del servidor de la conexión.</span><span class="sxs-lookup"><span data-stu-id="6e823-112">The custom action demonstrated in the sample automatically adjusts the proxy server configuration for a connection based on the connection's server address.</span></span> <span data-ttu-id="6e823-113">Los clientes pueden usar este ejemplo como punto de partida para crear sus propias acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="6e823-113">Customers can use this sample as a starting point for creating their own custom actions.</span></span>

 

 




