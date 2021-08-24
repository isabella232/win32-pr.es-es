---
description: La clase NTEventLogEventConsumer escribe un mensaje en el Windows de eventos cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: ca998a91-d9f7-44ff-bb83-5ba92d68f31e
ms.tgt_platform: multiple
title: Registro en el registro de eventos NT basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c8c070b1a52fe41f32b8610ff0931d33be7feb33f9f5cd6f6067652e963f6824
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050713"
---
# <a name="logging-to-nt-event-log-based-on-an-event"></a>Registro en el registro de eventos NT basado en un evento

La [**clase NTEventLogEventConsumer**](nteventlogeventconsumer.md) escribe un mensaje en el Windows de eventos cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.

> [!Note]  
> Los usuarios autenticados no pueden, de forma predeterminada, registrar eventos en el registro de aplicaciones en un equipo remoto. Como resultado, se producirá un error en el ejemplo descrito en este tema si usa la propiedad **UNCServerName** de la clase [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) y especifica un equipo remoto como su valor. Para obtener información sobre cómo cambiar la seguridad del registro de eventos, consulte este [artículo de KB](https://support.microsoft.com/kb/323076).

 

El procedimiento básico para usar un consumidor estándar se describe en Supervisión y respuesta a [eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md) A continuación se indican pasos adicionales más allá del procedimiento básico, necesarios al usar la [**clase NTEventLogEventConsumer.**](nteventlogeventconsumer.md) En los pasos se describe cómo crear un consumidor de eventos que escribe en el registro de eventos de la aplicación.

En el procedimiento siguiente se describe cómo crear un consumidor de eventos que escribe en el registro de eventos NT.

**Para crear un consumidor de eventos que escriba en el registro Windows eventos**

1.  En un Managed Object Format (MOF), cree una instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md) para recibir los eventos que solicite en la consulta. Para obtener más información sobre cómo escribir código MOF, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).
2.  Cree y asigne un nombre a una instancia de [**\_ \_ EventFilter**](--eventfilter.md)y, a continuación, cree una consulta para especificar el tipo de evento que desencadena la escritura en el registro de eventos NT.

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

3.  Cree una instancia de [**\_ \_ FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar el filtro a la instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md).
4.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Ejemplo

El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación mediante [scripting API](scripting-api-for-wmi.md) para WMI o la API COM [para WMI.](com-api-for-wmi.md) En el ejemplo se muestra cómo crear un consumidor para escribir en el registro de eventos application mediante [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). El MOF crea una nueva clase denominada "NTLogCons Example", un filtro de eventos para consultar operaciones, como la creación, en una instancia de esta nueva clase y un enlace entre el filtro y el \_ consumidor. Dado que la última acción del MOF es crear una instancia de NTLogCons Example, puede ver inmediatamente el evento en el registro de eventos application ejecutando \_ Eventvwr.exe.

identifica `EventID=0x0A for SourceName="WinMgmt"` un mensaje con el texto siguiente. "%1", "%2", "%3" son marcadores de posición para las cadenas correspondientes especificadas en la matriz InsertionStringTemplates.

``` syntax
Event filter with query "%2" could not be [re]activated in 
namespace "%1" because of error %3. Events may not be delivered 
through this filter until the problem is corrected.
```

En el procedimiento siguiente se describe cómo usar el ejemplo.

**Para usar el ejemplo**

1.  Copie la lista MOF siguiente en un archivo de texto y guárdelo con una extensión .mof.
2.  En una ventana Comandos, compile el archivo MOF mediante el comando siguiente:

    **Mofcomp** *filename:.mof**

3.  Ejecute Eventvwr.exe. Mire el registro de eventos de la aplicación. Debería ver un evento con id. = 10 **(EventID),** Source = "WMI" y Type = Error.
4.  Haga doble clic en **el mensaje Tipo de** información de WMI con 10 en la **columna** Evento . Se mostrará la descripción siguiente para el evento.

    ``` syntax
    Event filter with query "STRING2" could not be [re]activated in 
    namespace "STRING1" because of error STRING3. Events cannot be 
    delivered through this filter until the problem is corrected.
    ```

``` syntax
// Set the namespace as root\subscription.
// The NTEventLogEventConsumer is already
// compiled in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")
class NTLogCons_Example
{
 [key] string name;
 string InsertionString;
};

// Create an instance of the NT Event log consumer
// and give it the alias $CONSUMER

instance of NTEventLogEventConsumer as $CONSUMER
{
    // Unique instance name
    Name = "NTConsumerTest"; 
    // System component that generates the event
    SourceName = "WinMgmt";
    // Event message WBEM_MC_CANNOT_ACTIVATE_FILTER
    EventID = 0xC000000A;
    // EVENTLOG_ERROR_TYPE
    EventType = 1;
    // WMI event messages do not have multiple categories
    Category = 0;
    // Number of strings in InsertionStringTemplates property
    NumberOfInsertionStrings = 3;

    InsertionStringTemplates =
       {"%TargetInstance.Name%",
        "%TargetInstance.InsertionString%",
        "STRING3"};
};

// Create an instance of the event filter
// and give it the alias $FILTER
// The filter queries for any instance operation event
// for instances of the NTLogCons_Example class

instance of __EventFilter as $FILTER
{
    // Unique instance name
    Name = "NTLogConsFilter";
    Query = "SELECT * from __InstanceOperationEvent"
            " WHERE TargetInstance ISA \"NTLogCons_Example\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding
// between filter and consumer instances.

instance of __FilterToConsumerBinding
{
    Consumer = $CONSUMER;
    Filter = $FILTER;
};

// Create an instance of this class right now. 

instance of NTLogCons_Example
{
   Name = "STRING1";
   InsertionString = "STRING2";
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



