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
# <a name="troubleshooting-wmi-client-applications"></a>Solución de problemas de aplicaciones cliente WMI

WMI contiene un conjunto de clases para [solucionar problemas](wmi-troubleshooting-classes.md) de las aplicaciones cliente que utilizan proveedores WMI. Las clases de eventos de solución de problemas están acopladas a las clases de eventos de WMI, de modo que puede realizar un seguimiento de la ejecución de la aplicación mediante un registro de eventos de solución de problemas capturados.

La lista siguiente contiene ejemplos de solución de problemas de clases de eventos:

-   [**Msft \_ WmiProvider \_ ExecMethodAsyncEvent \_ pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-pre)

    Se genera antes de que WMI llame a [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.

-   [**Publicación de msft \_ WmiProvider \_ ExecMethodAsyncEvent \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-execmethodasyncevent-post)

    Se genera después de que WMI llame a [**IWbemServices:: ExecMethodAsync ()**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) en el proveedor.

En el procedimiento siguiente se muestra cómo solucionar problemas de ejecución de la aplicación.

**Para configurar la solución de problemas de WMI**

1.  Crear y compilar un archivo MOF para usar el consumidor de eventos de registro de WMI.
2.  Ejecute la aplicación cliente.
3.  Vea el archivo de registro de solución de problemas para todos los eventos de operación y error del proveedor y analice el registro para diagnosticar los problemas de cliente que está detectando.

Otro enfoque de solución de problemas consiste en ver la lista de proveedores actualmente en la caché del equipo, mediante la enumeración de los [**\_ proveedores de msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) en el espacio de nombres **root \\ cimv2** . Hay métodos en esta clase que permiten cargar y descargar proveedores para la depuración o el programa de instalación.

En el ejemplo de código siguiente se usa el consumidor de eventos de registro de WMI para capturar todos los eventos de la clase de eventos primaria, con lo que se capturan todos los eventos de operación del proveedor.

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

Cuando los mensajes de error indiquen un error de carga del proveedor, use [**msft \_ WmiProvider \_ LoadOperationFailureEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-loadoperationfailureevent) para identificar el proveedor que causó el error.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Clases de solución de problemas de WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
