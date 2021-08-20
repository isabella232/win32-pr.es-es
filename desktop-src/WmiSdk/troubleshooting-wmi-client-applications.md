---
description: WMI contiene un conjunto de clases para solucionar problemas de aplicaciones cliente que usan proveedores WMI.
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
ms.openlocfilehash: 7fb9eb8c438faab8915691ee2c9c8a4c77d247c6802f8f114683a79d2833bd15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050033"
---
# <a name="troubleshooting-wmi-client-applications"></a>Solución de problemas de aplicaciones cliente WMI

WMI contiene un conjunto de clases para [solucionar](wmi-troubleshooting-classes.md) problemas de aplicaciones cliente que usan proveedores WMI. Las clases de eventos de solución de problemas están acopladas a las clases de eventos WMI, de modo que puede realizar un seguimiento de la ejecución de la aplicación mediante un registro de eventos de solución de problemas capturados.

La lista siguiente contiene ejemplos de clases de eventos de solución de problemas:

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Se genera antes de que WMI [**llame a IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Se genera después de que WMI llama [**a IWbemServices::ExecMethodAsync()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.

En el procedimiento siguiente se muestra cómo solucionar problemas de ejecución de aplicaciones.

**Para configurar la solución de problemas de WMI**

1.  Cree y compile un archivo MOF para usar el consumidor de eventos de registro wmi.
2.  Ejecute la aplicación cliente.
3.  Vea el archivo de registro de solución de problemas de todos los eventos de operación y error del proveedor y analice el registro para diagnosticar los problemas de cliente que se están detectando.

Otro enfoque de solución de problemas es ver la lista de proveedores que se encuentran actualmente en la memoria caché del equipo, enumerando los proveedores [**de MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) en el espacio de nombres **\\ cimv2** raíz. Hay métodos en esta clase que permiten cargar y descargar proveedores con fines de depuración o configuración.

En el ejemplo de código siguiente se usa el consumidor de eventos de registro wmi para capturar todos los eventos de la clase de eventos primaria, capturando así todos los eventos de operación del proveedor.

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

Cuando los mensajes de error indican un error de carga del proveedor, use [**MSFT \_ WmiProvider \_ LoadOperationFailureEvent para**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) identificar qué proveedor produjo el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
