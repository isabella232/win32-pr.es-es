---
description: Los consumidores temporales y permanentes tienen distintos métodos para proteger la entrega de eventos.
ms.assetid: cd02e5db-f9e2-438b-9632-0a1387a6d4e3
ms.tgt_platform: multiple
title: Recepción segura de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27d156213553ee17a346d780cbea0ff82beca83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667867"
---
# <a name="receiving-events-securely"></a>Recepción segura de eventos

Los consumidores temporales y permanentes tienen distintos métodos para proteger la entrega de eventos.

En este tema se describen las siguientes secciones:

-   [Protección de consumidores temporales](#securing-temporary-consumers)
-   [Protección de consumidores permanentes](#securing-permanent-consumers)
-   [Protección de la suscripción permanente](#securing-the-permanent-subscription)
-   [Establecimiento de un Administrator-Only SD](#setting-an-administrator-only-sd)
-   [Suplantar la identidad del proveedor de eventos](#impersonating-the-event-provider-identity)
-   [SID y suscripciones permanentes](#sids-and-permanent-subscriptions)
-   [Crear suscripciones permanentes mediante cuentas de dominio](#creating-permanent-subscriptions-using-domain-accounts)
-   [Temas relacionados](#related-topics)

## <a name="securing-temporary-consumers"></a>Protección de consumidores temporales

Un [*consumidor temporal*](gloss-t.md) se ejecuta hasta que se reinicia el sistema o se detiene WMI, pero no se puede iniciar si se produce un evento específico. Por ejemplo, una llamada a [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) crea un consumidor temporal.

Las llamadas [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) o [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) crean consumidores de eventos temporales. Los consumidores temporales no pueden controlar quién proporciona eventos al [*receptor*](gloss-s.md) de eventos que crean.

Las llamadas a métodos [**ExecNotificationQuery**](swbemservices-execnotificationquery.md) se pueden realizar sincrónicamente, de forma [*semisincrónica*](gloss-s.md)o asincrónica. Por ejemplo, [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) es un método sincrónico que se puede llamar sincrónicamente, en función de cómo se establezca el parámetro *iflags* . [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) es una llamada asincrónica.

Tenga en cuenta que la devolución de llamada al receptor para las versiones asincrónicas de estas llamadas podría no devolverse en el mismo nivel de autenticación que la llamada realizada por el script. Por lo tanto, se recomienda usar semisincrónico en lugar de llamadas asincrónicas. Si necesita una comunicación asincrónica, consulte [llamar a un método](calling-a-method.md) y [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

Los suscriptores de scripting no pueden comprobar los derechos de acceso de un proveedor de eventos para proporcionar eventos al receptor creado por el script. Por lo tanto, se recomienda que las llamadas a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utilicen la forma semisincrónica de la llamada y usen la configuración de seguridad específica. Para obtener más información, vea [crear una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="securing-permanent-consumers"></a>Protección de consumidores permanentes

Un [*consumidor permanente*](gloss-p.md) tiene una suscripción permanente a los eventos de un proveedor de eventos que se conservarán después de que se reinicie el sistema operativo. Un proveedor de eventos que admite consumidores permanentes es un [*proveedor de consumidores de eventos*](gloss-e.md). Si el proveedor de eventos no se está ejecutando cuando se produce un evento, WMI inicia el proveedor cuando necesita proporcionar eventos. WMI identifica a qué proveedor de consumidores deben entregarse los eventos, en función de la instancia de [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que asocia la instancia del proveedor de consumidores [**\_ \_ Win32Provider**](--win32provider.md) a una [*clase de consumidor lógica*](gloss-l.md) definida por el proveedor del consumidor. Para obtener más información sobre el rol de los proveedores de consumidores, consulte [escribir un proveedor de consumidor de eventos](writing-an-event-consumer-provider.md).

Los consumidores permanentes pueden controlar quién les envía eventos y los proveedores de eventos pueden controlar quién accede a sus eventos.

Las aplicaciones y los scripts de cliente crean instancias de la clase de consumidor lógico como parte de una suscripción. La clase de consumidor lógico define la información que contiene el evento, lo que el cliente puede hacer con el evento y cómo se entrega el evento.

Las [clases de consumidor estándar](standard-consumer-classes.md) de WMI proporcionan ejemplos del rol de las clases de consumidor lógico. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="securing-the-permanent-subscription"></a>Protección de la suscripción permanente

Las suscripciones permanentes tienen mayor potencial para causar problemas de seguridad en WMI y, por tanto, tienen los siguientes requisitos de seguridad:

-   La instancia de consumidor lógico, las instancias de [**\_ \_ EventFilter**](--eventfilter.md)y [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) deben tener el mismo identificador de seguridad (SID) individual en la propiedad **CreatorSID** . Para obtener más información, vea [mantener el mismo SID en todas las instancias de una suscripción permanente](#sids-and-permanent-subscriptions).
-   La cuenta que crea la suscripción debe ser una cuenta de dominio con privilegios de administrador local o la cuenta de grupo de administradores local. El uso del SID del grupo administradores permite que la suscripción siga funcionando en el equipo local, aunque esté desconectada de la red. El uso de una cuenta de dominio permite la identificación exacta del usuario.

    Sin embargo, si el equipo no está conectado y la cuenta de creación es una cuenta de dominio, se produce un error en el consumidor porque WMI no puede comprobar la identidad de la cuenta. Para evitar errores de suscripción si el equipo está desconectado de la red, use el SID del grupo de administradores para una suscripción. En este caso, debe asegurarse de que la cuenta LocalSystem puede tener acceso a los datos de pertenencia a grupos en el dominio. Algunos proveedores de consumidores de eventos tienen requisitos de seguridad especialmente elevados, ya que una suscripción no autorizada puede provocar un gran daño. Algunos ejemplos son los consumidores estándar, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) y [**CommandLineEventConsumer**](commandlineeventconsumer.md).

-   Puede configurar la suscripción permanente para que solo acepte eventos de identidades específicas del proveedor de eventos. Establezca el descriptor de seguridad en la propiedad **EventAccess** de la instancia de [**\_ \_ EventFilter**](--eventfilter.md) en las identidades del proveedor de eventos. WMI compara la identidad del proveedor de eventos con el descriptor de seguridad para determinar si el proveedor tiene acceso de **\_ \_ publicación derecho de WBEM** . Para obtener más información, vea [constantes de seguridad de WMI](wmi-security-constants.md).

    Si el filtro permite el acceso a la identidad del proveedor de eventos, también confiará en el evento. Esto permite al consumidor que recibió el evento generar un evento delegado.

    **Nota:**  El valor predeterminado para el descriptor de seguridad en **EventAccess** es **null**, lo que permite el acceso a todos. Se recomienda limitar el acceso en la instancia de suscripción de [**\_ \_ EventFilter**](--eventfilter.md) para mejorar la seguridad de los eventos.

## <a name="setting-an-administrator-only-sd"></a>Establecimiento de un Administrator-Only SD

En el siguiente ejemplo de código de C++ se crea un descriptor de seguridad solo de administrador en la instancia de [**\_ \_ EventFilter**](--eventfilter.md) . En este ejemplo se crea el descriptor de seguridad mediante el [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL). Para obtener más información sobre WBEM, consulte **\_ el \_** apartado sobre [constantes de seguridad WMI](wmi-security-constants.md).


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



El ejemplo de código anterior requiere las siguientes instrucciones de referencia e \# inclusión.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



## <a name="impersonating-the-event-provider-identity"></a>Suplantar la identidad del proveedor de eventos

Un consumidor permanente puede necesitar suplantar al proveedor de eventos para procesar el evento. Los consumidores permanentes solo pueden suplantar al proveedor de eventos cuando se cumplan las condiciones siguientes:

-   La instancia de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) tiene la propiedad **MaintainSecurityContext** establecida en **true**.
-   Un evento se entrega en el mismo contexto de seguridad en el que se encontraba el proveedor cuando generó el evento. Solo un consumidor implementado como un archivo DLL, un consumidor en proceso, puede recibir eventos en el contexto de seguridad del proveedor. Para obtener más información sobre la seguridad de los proveedores y consumidores en proceso, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).
-   El proveedor de eventos se está ejecutando en un proceso que permite la suplantación.

La cuenta que ejecuta el proceso de consumidor debe tener acceso de **\_ escritura completo** en el repositorio WMI (también conocido como repositorio CIM). En la suscripción, las instancias de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)y [**\_ \_ EventFilter**](--eventfilter.md) deben tener el mismo valor de identificador de seguridad (SID) individual en la propiedad **CreatorSID** . WMI almacena el SID en **CreatorSID** para cada instancia.

## <a name="sids-and-permanent-subscriptions"></a>SID y suscripciones permanentes

Una suscripción permanente no funciona cuando el mismo usuario no crea el enlace, el consumidor y el filtro, lo que significa que [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md), [**\_ \_ EventConsumer**](--eventconsumer.md)y [**\_ \_ EventFilter**](--eventfilter.md) deben tener el mismo valor de identificador de seguridad (SID) individual en la propiedad **CreatorSID** . Instrumental de administración de Windows (WMI) almacena este valor.

## <a name="creating-permanent-subscriptions-using-domain-accounts"></a>Crear suscripciones permanentes mediante cuentas de dominio

Se deben tener en cuenta varios problemas al usar cuentas de dominio para crear suscripciones permanentes. Todas las suscripciones permanentes deben seguir funcionando cuando ningún usuario haya iniciado sesión, lo que significa que funcionan con la cuenta integrada LocalSystem.

Si un usuario del dominio es el creador de una suscripción permanente para consumidores sensibles a la seguridad ([**ActiveScriptEventConsumer**](activescripteventconsumer.md), [**CommandLineEventConsumer**](commandlineeventconsumer.md)), WMI comprueba si la propiedad **CreatorSID** de la clase [**\_ \_ EventFilter**](--eventfilter.md) , la clase [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) y las instancias del consumidor pertenecen a un usuario que es miembro del grupo de administradores locales.

En el ejemplo de código siguiente se muestra cómo se puede especificar la propiedad **CreatorSID** .

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

En situaciones entre dominios, agregue usuarios autenticados al grupo de acceso de autorización de Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> <dt>

[Recibir un evento de WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
