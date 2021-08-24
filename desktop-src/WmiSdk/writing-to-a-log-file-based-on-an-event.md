---
description: La clase LogFileEventConsumer puede escribir texto predefinido en un archivo de registro cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.
ms.assetid: c337e9f7-f40c-4d7d-a180-c053e24c882b
ms.tgt_platform: multiple
title: Escribir en un archivo de registro basado en un evento
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 881435986a1097c2ba97160693ed15e28bae3d86019fb703adf6bf1e8b07f8a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049733"
---
# <a name="writing-to-a-log-file-based-on-an-event"></a>Escribir en un archivo de registro basado en un evento

La [**clase LogFileEventConsumer**](logfileeventconsumer.md) puede escribir texto predefinido en un archivo de registro cuando se produce un evento especificado. Esta clase es un consumidor de eventos estándar que proporciona WMI.

El procedimiento básico para usar consumidores estándar es siempre el mismo y se encuentra en Supervisión y respuesta a eventos [con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

El procedimiento siguiente agrega al procedimiento básico, es específico de la clase [**LogFileEventConsumer**](logfileeventconsumer.md) y describe cómo crear un consumidor de eventos que ejecuta un programa.

**Para crear un consumidor de eventos que escribe en un archivo de registro**

1.  En el archivo Managed Object Format (MOF), cree una instancia de [**LogFileEventConsumer**](logfileeventconsumer.md) para recibir los eventos que solicite en la consulta, asigne un nombre a la instancia en la propiedad **Name** y, a continuación, coloque la ruta de acceso al archivo de registro en la propiedad **Filename.**

    Para obtener más información, vea [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).

2.  Proporcione la plantilla de texto para escribir en el archivo de registro en la propiedad Text.

    Para obtener más información, vea [Usar plantillas de cadena estándar.](using-standard-string-templates.md)

3.  Cree una instancia de [**\_ \_ EventFilter**](--eventfilter.md) y defina una consulta para especificar los eventos que activarán el consumidor.

    Para obtener más información, [vea Consulta con WQL.](querying-with-wql.md)

4.  Cree una instancia de [**\_ \_ FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar el filtro a la instancia de [**LogFileEventConsumer.**](logfileeventconsumer.md)
5.  Para controlar quién lee o escribe en el archivo de registro, establezca la seguridad en el directorio donde se encuentra el registro en el nivel requerido.
6.  Compile el archivo MOF mediante [**Mofcomp.exe**](mofcomp.md).

## <a name="example"></a>Ejemplo

El ejemplo de esta sección está en código MOF, pero puede crear las instancias mediante programación mediante [scripting API](scripting-api-for-wmi.md) para WMI o la API COM [para WMI.](com-api-for-wmi.md) En el ejemplo se usa el estándar LogFileEventConsumer para crear una clase de consumidor denominada LogFileEvent que escribe una línea en el archivo c: Logfile.log cuando se crea una instancia de la \\ clase LogFileEvent.

En el procedimiento siguiente se describe cómo usar el ejemplo.

**Para usar el ejemplo**

1.  Copie la lista MOF siguiente en un archivo de texto y guárdelo con una extensión .mof.
2.  En una ventana de comandos, compile el archivo MOF mediante el comando siguiente.

    **Mofcomp** *filename:.mof**

3.  Abra Logfile.log para ver la línea especificada por LogFileEvent.Name: "Evento de consumidor de eventos de archivo de registro".

``` syntax
// Set the namespace as root\subscription.
// The LogFileEventConsumer is already compiled 
//     in the root\subscription namespace. 

#pragma namespace ("\\\\.\\Root\\subscription")

class LogFileEvent
{
    [key]string Name;
};

// Create an instance of the standard log
// file consumer and give it the alias $CONSUMER

instance of LogFileEventConsumer as $CONSUMER
{
    // If the file does not already exist, it is created.
    Filename = "c:\\Logfile.log";  
    IsUnicode = FALSE;
    // Name of this instance of LogFileEventConsumer
    Name = "LogfileEventConsumer_Example";  
    // See "Using Standard String Templates"; 
    Text = "%TargetInstance.Name%"; 
    // TargetInstance is the instance of LogFileEvent 
    //    requested in the filter        
                                         
};

// Create an instance of the event filter 
// and give it the alias $FILTER
// Query for any instance operation type,
// such as instance creation, for LogFileEvent class

instance of __EventFilter as $FILTER
{
    Name = "LogFileFilter";
    Query = "SELECT * FROM __InstanceOperationEvent "
        "WHERE TargetInstance.__class = \"LogFileEvent\"";
    QueryLanguage = "WQL";
};

// Create an instance of the binding.

instance of __FilterToConsumerBinding
{
    Consumer=$CONSUMER;
    Filter=$FILTER;
 DeliverSynchronously=FALSE;
};

// Create an instance of this class right now
// Look at the file c:\Logfile.log to see
// that a line has been written.

instance of LogFileEvent
{
 Name = "Logfile Event Consumer event";  
};
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> </dl>

 

 



