---
description: WMI contiene un conjunto de clases para solucionar problemas de las aplicaciones cliente que utilizan proveedores WMI.
ms.assetid: f69b360a-2c24-4776-bcda-b51edde0dcde
ms.tgt_platform: multiple
title: Solución de problemas de aplicaciones cliente WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a84646aa42cd0ccd649e3937f0eba257343e9a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277922"
---
# <a name="troubleshooting-wmi-client-applications"></a><span data-ttu-id="f8b04-103">Solución de problemas de aplicaciones cliente WMI</span><span class="sxs-lookup"><span data-stu-id="f8b04-103">Troubleshooting WMI Client Applications</span></span>

<span data-ttu-id="f8b04-104">WMI contiene un conjunto de clases para [solucionar problemas](wmi-troubleshooting-classes.md) de las aplicaciones cliente que utilizan proveedores WMI.</span><span class="sxs-lookup"><span data-stu-id="f8b04-104">WMI contains a set of classes for [troubleshooting](wmi-troubleshooting-classes.md) client applications that use WMI providers.</span></span> <span data-ttu-id="f8b04-105">Las clases de eventos de solución de problemas están acopladas a las clases de eventos de WMI, de modo que puede realizar un seguimiento de la ejecución de la aplicación mediante un registro de eventos de solución de problemas capturados.</span><span class="sxs-lookup"><span data-stu-id="f8b04-105">The troubleshooting event classes are coupled to WMI event classes, such that you can track your application execution using a log of captured troubleshooting events.</span></span>

<span data-ttu-id="f8b04-106">La lista siguiente contiene ejemplos de solución de problemas de clases de eventos:</span><span class="sxs-lookup"><span data-stu-id="f8b04-106">The following list contains examples of troubleshooting event classes:</span></span>

-   [<span data-ttu-id="f8b04-107">**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ pre**</span><span class="sxs-lookup"><span data-stu-id="f8b04-107">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Pre**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    <span data-ttu-id="f8b04-108">Se genera antes de que WMI llame a [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f8b04-108">Raised before WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

-   [<span data-ttu-id="f8b04-109">**Publicación de msft \_ WmiProvider \_ ExecMethodAsyncEvent \_**</span><span class="sxs-lookup"><span data-stu-id="f8b04-109">**Msft\_WmiProvider\_ExecMethodAsyncEvent\_Post**</span></span>](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    <span data-ttu-id="f8b04-110">Se genera después de que WMI llame a [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.</span><span class="sxs-lookup"><span data-stu-id="f8b04-110">Raised after WMI calls [**IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) on the provider.</span></span>

<span data-ttu-id="f8b04-111">En el procedimiento siguiente se muestra cómo solucionar problemas de ejecución de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8b04-111">The following procedure shows how to troubleshoot application execution.</span></span>

<span data-ttu-id="f8b04-112">**Para configurar la solución de problemas de WMI**</span><span class="sxs-lookup"><span data-stu-id="f8b04-112">**To set up WMI troubleshooting**</span></span>

1.  <span data-ttu-id="f8b04-113">Crear y compilar un archivo MOF para usar el consumidor de eventos de registro de WMI.</span><span class="sxs-lookup"><span data-stu-id="f8b04-113">Create and compile a MOF file to use the WMI logging event consumer.</span></span>
2.  <span data-ttu-id="f8b04-114">Ejecute la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="f8b04-114">Run your client application.</span></span>
3.  <span data-ttu-id="f8b04-115">Vea el archivo de registro de solución de problemas para todos los eventos de operación y error del proveedor y analice el registro para diagnosticar los problemas de cliente que está detectando.</span><span class="sxs-lookup"><span data-stu-id="f8b04-115">View the troubleshooting log file for all provider operation and failure events, and analyze the log to diagnose the client problems you are encountering.</span></span>

<span data-ttu-id="f8b04-116">Otro enfoque de solución de problemas consiste en ver la lista de proveedores actualmente en la caché del equipo, mediante la enumeración de los [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) en el espacio de nombres **root \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="f8b04-116">Another troubleshooting approach is to view the list of providers currently in the computer cache, by enumerating [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) in the **root\\cimv2** namespace.</span></span> <span data-ttu-id="f8b04-117">Hay métodos en esta clase que permiten cargar y descargar proveedores para la depuración o el programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="f8b04-117">There are methods in this class that enable you to load and unload providers for debugging or setup purposes.</span></span>

<span data-ttu-id="f8b04-118">En el ejemplo de código siguiente se usa el consumidor de eventos de registro de WMI para capturar todos los eventos de la clase de eventos primaria, con lo que se capturan todos los eventos de operación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f8b04-118">The following code example uses the WMI logging event consumer to capture all events of the parent event class, thus capturing all provider operation events.</span></span>

``` syntax
#pragma autorecover
#pragma namespace("\\\\.\\root\\subscription")

instance of __EventFilter as $Filter
{
  Name = "ProviderOperationEvents" ;
  EventNamespace = "root\\cimv2" ;
  Query = "SELECT * FROM MSFT_WmiProvider_OperationEvent" ;
  QueryLanguage = "WQL" ;
} ;

Instance of LogFileEventConsumer as $Consumer
{
  Name = "ProviderOperationEvents" ;
  FileName = "C:\\test.txt" ;
  Text = "Operation - %__TEXT%" ;
} ;

instance of __FilterToConsumerBinding
{
  Filter = $Filter ;
  Consumer = $Consumer ;
  MaintainSecurityContext = TRUE ;
} ;
```

<span data-ttu-id="f8b04-119">Cuando los mensajes de error indiquen un error de carga del proveedor, use [**msft \_ WmiProvider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) para identificar el proveedor que causó el error.</span><span class="sxs-lookup"><span data-stu-id="f8b04-119">When error messages indicate provider load failure, use [**MSFT\_WmiProvider\_LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) to identify which provider caused the fault.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8b04-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8b04-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8b04-121">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="f8b04-121">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="f8b04-122">Clases de solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="f8b04-122">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
