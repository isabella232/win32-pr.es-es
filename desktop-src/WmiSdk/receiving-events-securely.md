---
description: Los consumidores temporales y permanentes tienen diferentes métodos para proteger la entrega de eventos.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Recepción de eventos de forma segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64db5b0289abd9a43caee6ddb3b68da94a9560b0ea8f591d95ee472cf900b4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316532"
---
# <a name="receiving-events-securely"></a>Recepción de eventos de forma segura

Los consumidores temporales y permanentes tienen diferentes métodos para proteger la entrega de eventos.

En este tema se de abordan las siguientes secciones:

-   [Protección de consumidores temporales](#securing-temporary-consumers)
-   [Protección de consumidores permanentes](#securing-permanent-consumers)
-   [Protección de la suscripción permanente](#securing-the-permanent-subscription)
-   [Establecimiento de una Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Suplantación de la identidad del proveedor de eventos](#impersonating-the-event-provider-identity)
-   [SID y suscripciones permanentes](#sids-and-permanent-subscriptions)
-   [Creación de suscripciones permanentes mediante cuentas de dominio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Temas relacionados](#related-topics)

## <a name="securing-temporary-consumers"></a>Protección de consumidores temporales

Un [*consumidor temporal se ejecuta*](gloss-t.md) hasta que se reinicia el sistema o wmi se detiene, pero no se puede iniciar si se genera un evento específico. Por ejemplo, una llamada a [**SWbemServices.ExecNotificationQueryAsync crea**](swbemservices-execnotificationqueryasync.md) un consumidor temporal.

Las llamadas [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) o [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) crean consumidores de eventos temporales. Los consumidores temporales no pueden controlar quién proporciona eventos al receptor [*de eventos*](gloss-s.md) que crean.

Las llamadas [**a los métodos ExecNotificationQuery**](swbemservices-execnotificationquery.md) se pueden realizar de forma sincrónica, [*semisincronosa*](gloss-s.md)o asincrónica. Por ejemplo, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) es un método sincrónico que se puede llamar semisincronía, dependiendo de cómo se establezca el parámetro *iflags.* [**SWbemServices.ExecNotificationQueryAsync es**](swbemservices-execnotificationqueryasync.md) una llamada asincrónica.

Tenga en cuenta que es posible que la devolución de llamada al receptor para las versiones asincrónicas de estas llamadas no se devuelva en el mismo nivel de autenticación que la llamada al script realizado. Por lo tanto, se recomienda usar llamadas semisincrónicas en lugar de llamadas asincrónicas. Si necesita comunicación asincrónica, vea [Llamar a un método y](calling-a-method.md) Establecer la seguridad en una llamada [asincrónica.](setting-security-on-an-asynchronous-call.md)

Los suscriptores de scripting no pueden comprobar los derechos de acceso de un proveedor de eventos para proporcionar eventos al receptor creado por el script. Por lo tanto, se recomienda que las llamadas [**aSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usen la forma semisincronosa de la llamada y usen una configuración de seguridad específica. Para obtener más información, vea [Realizar una llamada semisincronosa con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="securing-permanent-consumers"></a>Protección de consumidores permanentes

Un [*consumidor permanente tiene*](gloss-p.md) una suscripción permanente a eventos de un proveedor de eventos que se conservará después de reiniciar el sistema operativo. Un proveedor de eventos que admite consumidores permanentes es un [*proveedor de consumidores de eventos*](gloss-e.md). Si el proveedor de eventos no se está ejecutando cuando se produce un evento, WMI inicia el proveedor cuando necesita entregar eventos. WMI identifica a qué proveedor de consumidores se deben entregar los eventos, en función de la instancia [**\_ \_ eventConsumerProviderRegistration,**](--eventconsumerproviderregistration.md) que asocia la instancia [**\_ \_ win32Provider**](--win32provider.md) del proveedor de consumidores [*con*](gloss-l.md) una clase de consumidor lógica definida por el proveedor de consumidores. Para obtener más información sobre el rol de los proveedores de consumidores, vea [Escribir un proveedor de consumidores de eventos](writing-an-event-consumer-provider.md).

Los consumidores permanentes pueden controlar quién los envía y los proveedores de eventos pueden controlar quién accede a sus eventos.

Los scripts de cliente y las aplicaciones crean instancias de la clase de consumidor lógico como parte de una suscripción. La clase de consumidor lógico define qué información contiene el evento, qué puede hacer el cliente con el evento y cómo se entrega el evento.

Las clases [de consumidor estándar wmi](standard-consumer-classes.md) proporcionan ejemplos del rol de las clases de consumidor lógico. Para obtener más información, vea [Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="securing-the-permanent-subscription"></a>Protección de la suscripción permanente

Las suscripciones permanentes tienen mayor potencial para causar problemas de seguridad en WMI y, por tanto, tienen los siguientes requisitos de seguridad:

-   Las instancias de consumidor lógico, [**\_ \_ EventFilter**](--eventfilter.md)y [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) deben tener el mismo identificador de seguridad individual (SID) en la **propiedad CreatorSID.** Para obtener más información, vea [Mantener el mismo SID en todas las instancias de una suscripción permanente.](#sids-and-permanent-subscriptions)
-   La cuenta que crea la suscripción debe ser una cuenta de dominio con privilegios de administrador local o la cuenta de grupo Administradores local. El uso del SID del grupo Administradores permite que la suscripción siga funcionando en el equipo local, incluso si está desconectada de la red. El uso de una cuenta de dominio permite la identificación exacta del usuario.

    Sin embargo, si el equipo no está conectado y la cuenta de creación es una cuenta de dominio, se produce un error en el consumidor porque WMI no puede comprobar la identidad de la cuenta. Para evitar errores de suscripción si el equipo está desconectado de la red, use el SID del grupo Administradores para una suscripción. En este caso, debe asegurarse de que la cuenta LocalSystem puede acceder a los datos de pertenencia a grupos en el dominio. Algunos proveedores de consumidores de eventos tienen requisitos de seguridad especialmente elevados, ya que una suscripción no fiable puede causar grandes daños. Algunos ejemplos son los consumidores [**estándar, ActiveScriptEventConsumer**](activescripteventconsumer.md) [**y CommandLineEventConsumer.**](commandlineeventconsumer.md)

-   Puede configurar la suscripción permanente para que solo acepte eventos de identidades específicas del proveedor de eventos. Establezca el descriptor de seguridad de la **propiedad EventAccess** de la [**\_ \_ instancia de EventFilter**](--eventfilter.md) en las identidades del proveedor de eventos. WMI compara la identidad del proveedor de eventos con el descriptor de seguridad para determinar si el proveedor tiene **acceso WBEM \_ RIGHT \_ PUBLISH.** Para obtener más información, vea [Wmi Security Constants](wmi-security-constants.md).

    Si el filtro permite el acceso a la identidad del proveedor de eventos, también confía en el evento. Esto permite al consumidor que recibió el evento generar un evento delegado.

    **Nota**  El valor predeterminado del descriptor de seguridad **de EventAccess** **es NULL,** que permite el acceso a todos los usuarios. Se recomienda limitar el acceso en la instancia de suscripción [**\_ \_ de EventFilter**](--eventfilter.md) para mejorar la seguridad de los eventos.

## <a name="setting-an-administrator-only-sd"></a>Establecimiento de una Administrator-Only SD

En el siguiente ejemplo de código de C++ se crea un descriptor de seguridad de solo administrador en la [**\_ \_ instancia de EventFilter.**](--eventfilter.md) En este ejemplo se crea el descriptor de seguridad mediante [lenguaje de definición de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL). Para obtener más información sobre **WBEM \_ RIGHT \_ SUBSCRIBE**, vea [Wmi Security Constants](wmi-security-constants.md).


```C++
// Create SD that allows only administrators 
//    to send events to this filter. 
// The SDDL settings are O:BAG:BAD:(A;;0x80;;;BA)
// Set the EventAccess property in the 
//    IWbemClassObject of the __EventFilter instance. 
   long lMask = WBEM_RIGHT_PUBLISH;
     WCHAR wBuf[MAX_PATH];
     _ltow( lMask, wBuf, 16 );
 
HRESULT hRes = pEventFilterInstance->Put( L"EventAccess", 0,
    &_variant_t( L"O:BAG:BAD:(A;;0x80;;;BA)" ), NULL );
```



El ejemplo de código anterior requiere las siguientes instrucciones reference e \# include.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Suplantación de la identidad del proveedor de eventos

Es posible que un consumidor permanente tenga que suplantar al proveedor de eventos para procesar el evento. Los consumidores permanentes solo pueden suplantar al proveedor de eventos cuando existen las condiciones siguientes:

-   La instancia de [**\_ \_ FilterToConsumerBinding tiene**](--filtertoconsumerbinding.md) la propiedad **MaintainSecurityContext** establecida en **True.**
-   Un evento se entrega en el mismo contexto de seguridad en el que estaba el proveedor cuando generó el evento. Solo un consumidor implementado como un archivo DLL, un consumidor en proceso, puede recibir eventos en el contexto de seguridad del proveedor. Para obtener más información sobre la seguridad de los proveedores y consumidores en proceso, vea [Provider Hosting and Security](provider-hosting-and-security.md).
-   El proveedor de eventos se ejecuta en un proceso que permite la suplantación.

La cuenta que ejecuta el proceso de consumidor debe tener **acceso DE \_** ESCRITURA COMPLETA al repositorio WMI (también conocido como repositorio CIM). En la suscripción, las instancias [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)y [**\_ \_ EventFilter**](--eventfilter.md) deben tener el mismo valor de identificador de seguridad individual (SID) en la **propiedad CreatorSID.** WMI almacena el SID en **CreatorSID** para cada instancia.

## <a name="sids-and-permanent-subscriptions"></a>SID y suscripciones permanentes

Una suscripción permanente no funciona cuando el enlace, el consumidor y el filtro no los crea el mismo usuario, lo que significa que [**\_ \_ FilterToConsumerBinding,**](--filtertoconsumerbinding.md) [**\_ \_ EventConsumer**](--eventconsumer.md)y [**\_ \_ EventFilter**](--eventfilter.md) deben tener el mismo valor de identificador de seguridad individual (SID) en la **propiedad CreatorSID.** Windows Instrumental de administración (WMI) almacena este valor.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Creación de suscripciones permanentes mediante cuentas de dominio

Se deben tener en cuenta varios problemas al usar cuentas de dominio para crear suscripciones permanentes. Todas las suscripciones permanentes seguirán funcionando cuando ningún usuario haya iniciado sesión, lo que significa que funcionan en la cuenta localSystem integrada.

Si un usuario de dominio es el creador de una suscripción permanente para consumidores confidenciales de seguridad [**(ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer),**](commandlineeventconsumer.md)WMI comprueba si la propiedad **CreatorSID** de la clase [**\_ \_ EventFilter,**](--eventfilter.md) la clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) y las instancias de consumidor pertenecen a un usuario que es miembro del grupo de administradores local.

En el ejemplo de código siguiente se muestra cómo se puede especificar la **propiedad CreatorSID.**

``` syntax
 instance of __EventFilter as $FILTER
    {
        // this is the Administrators SID in array of bytes format
        CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};    
        // Add filter code here ...
    }

    instance of ActiveScriptEventConsumer as $CONSUMER
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       // Add consumer code here ...
    }

    instance of __FilterToConsumerBinding
    {
       CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0};
       Consumer = $CONSUMER;
       Filter = $FILTER;
       // Add binding code here ...
    }
```

Para situaciones entre dominios, agregue Usuarios autenticados al "Windows de acceso de autorización".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protección de eventos WMI](securing-wmi-events.md)
</dt> <dt>

[Recepción de un evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
