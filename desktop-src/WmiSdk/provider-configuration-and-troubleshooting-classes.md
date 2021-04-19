---
description: La \_ clase de proveedores de msft y las clases de solución de problemas de WMI son un grupo de las clases de eventos msft acopladas a eventos del proveedor WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Clases de solución de problemas y configuración del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716201"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="84cf9-103">Clases de solución de problemas y configuración del proveedor</span><span class="sxs-lookup"><span data-stu-id="84cf9-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="84cf9-104">La clase de [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) y las clases de solución de problemas de WMI son un grupo de las [clases de eventos msft](msft-classes.md) acopladas a eventos del proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="84cf9-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="84cf9-105">La clase de [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contiene información de configuración para los proveedores e incluye los siguientes métodos que le permiten cargar y descargar proveedores, o suspender y reanudar las operaciones del proveedor:</span><span class="sxs-lookup"><span data-stu-id="84cf9-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="84cf9-106">**Método Load de la \_ clase de proveedores msft**</span><span class="sxs-lookup"><span data-stu-id="84cf9-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="84cf9-107">**Método Unload de la \_ clase de proveedores de msft**</span><span class="sxs-lookup"><span data-stu-id="84cf9-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="84cf9-108">**Método resume de la \_ clase de proveedores msft**</span><span class="sxs-lookup"><span data-stu-id="84cf9-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="84cf9-109">**Método Suspend de la \_ clase de proveedores msft**</span><span class="sxs-lookup"><span data-stu-id="84cf9-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="84cf9-110">Las [clases de solución de problemas de WMI](wmi-troubleshooting-classes.md) se denominan para indicar si el evento se desencadena antes o después de un evento de proveedor.</span><span class="sxs-lookup"><span data-stu-id="84cf9-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="84cf9-111">Por ejemplo, el [**objeto \_ \_ \_ anterior AccessCheck WmiProvider AccessCheck**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) se genera inmediatamente antes de llamar a la implementación del proveedor de **IWbemEventSecurity:: AccessCheck**, mientras que el objeto post de la llamada a [**\_ \_ AccessCheck \_ WmiProvider de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) se llama inmediatamente después de.</span><span class="sxs-lookup"><span data-stu-id="84cf9-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="84cf9-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="84cf9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84cf9-113">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="84cf9-113">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="84cf9-114">Clases de solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="84cf9-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
