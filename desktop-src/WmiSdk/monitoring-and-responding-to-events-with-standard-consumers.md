---
description: Puede usar las clases de consumidor estándar instaladas para realizar acciones basadas en eventos en un sistema operativo.
ms.assetid: 1979dc55-a440-4c31-832b-36fa84def4c9
ms.tgt_platform: multiple
title: Supervisión y respuesta a eventos con consumidores estándar
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b0b7e7b1d1e79e64fb1eb83f17f3aa2d118a9eb53b23c19cbdfd624e2c501a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992785"
---
# <a name="monitoring-and-responding-to-events-with-standard-consumers"></a>Supervisión y respuesta a eventos con consumidores estándar

Puede usar las clases de consumidor [estándar instaladas para](standard-consumer-classes.md) realizar acciones basadas en eventos en un sistema operativo. Los consumidores estándar son clases simples que ya están registradas y definen clases de consumidor permanentes. Cada consumidor estándar realiza una acción específica después de recibir una notificación de eventos. Por ejemplo, puede definir una instancia de [**ActiveScriptEventConsumer**](activescripteventconsumer.md) para ejecutar un script cuando el espacio libre en disco en un equipo es diferente de un tamaño especificado.

WMI compila los consumidores estándar en espacios de nombres predeterminados que dependen del sistema operativo, por ejemplo:

-   En Windows Server 2003, todos los consumidores estándar se compilan de forma predeterminada en el espacio de nombres "Suscripción \\ raíz".

> [!Note]  
> Para obtener los espacios de nombres predeterminados y los sistemas operativos específicos de cada clase WMI, vea las secciones Comentarios y requisitos de cada tema de clase.

 

En la tabla siguiente se enumeran y describen los consumidores estándar de WMI.



| Consumidor estándar                                              | Descripción                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActiveScriptEventConsumer**](activescripteventconsumer.md) | Ejecuta un script cuando recibe una notificación de eventos. Para obtener más información, vea [Ejecutar un script basado en un evento](running-a-script-based-on-an-event.md).                                                                                                                                                                                                                                                       |
| [**LogFileEventConsumer**](logfileeventconsumer.md)           | Escribe cadenas personalizadas en un archivo de registro de texto cuando recibe una notificación de eventos. Para obtener más información, [vea Escribir en un archivo de registro basado en un evento](writing-to-a-log-file-based-on-an-event.md).                                                                                                                                                                                                                  |
| [**NTEventLogEventConsumer**](nteventlogeventconsumer.md)     | Registra un mensaje específico en el registro de eventos de la aplicación. Para obtener más información, vea Registro en el registro de eventos [NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md).                                                                                                                                                                                                                                             |
| [**SMTPEventConsumer**](smtpeventconsumer.md)                 | Envía un mensaje de correo electrónico mediante SMTP cada vez que se le entrega un evento. Para obtener más información, vea [Enviar correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md).                                                                                                                                                                                                                                          |
| [**CommandLineEventConsumer**](commandlineeventconsumer.md)   | Inicia un proceso cuando se entrega un evento a un sistema local. El archivo ejecutable debe estar en una ubicación segura o estar protegido con una lista de control de acceso seguro (ACL) para evitar que un usuario no autorizado reemplace el ejecutable por otro ejecutable. Para obtener más información, vea [Ejecutar un programa desde la línea de comandos basada en un evento](running-a-program-from-the-command-line-based-on-an-event.md). |



 

En el procedimiento siguiente se describe cómo supervisar y responder a eventos mediante un consumidor estándar. Tenga en cuenta que el procedimiento es el mismo para un archivo Managed Object Format (MOF), un script o una aplicación.

**Para supervisar y responder a eventos con un consumidor estándar**

1.  Especifique el espacio de nombres en un archivo MOF mediante el comando de preprocesador [ \# MOF pragma namespace](pragma-namespace.md). En un script o aplicación, especifique el espacio de nombres en el código que se conecta a WMI.

    En el siguiente ejemplo de código MOF se muestra cómo especificar el espacio de nombres de \\ la suscripción raíz.

    ```syntax
    #pragma namespace ("\\\\.\\root\\subscription")
    ```

    La [*mayoría de los eventos*](gloss-i.md) intrínsecos están asociados a cambios en las instancias de clase del espacio de nombres \\ cimv2 raíz. Sin embargo, el proveedor del Registro del sistema desencadena eventos del Registro como [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) en el espacio de \\ nombres predeterminado [raíz.](/previous-versions/windows/desktop/regprov/system-registry-provider)

    Un consumidor puede incluir clases de eventos ubicadas en otros espacios de nombres especificando el espacio de nombres en la **propiedad EventNamespace** en la [**\_ \_ consulta EventFilter**](--eventfilter.md) para eventos. Las [*clases de eventos intrínsecos,*](gloss-i.md) como [**\_ \_ InstanceOperationEvent,**](--instanceoperationevent.md) están disponibles en cada espacio de nombres.

2.  Cree y rellene una instancia de una clase de consumidor estándar.

    Esta instancia puede tener un valor único en la **propiedad Name.** Puede actualizar un consumidor existente si vuelve a usar el mismo nombre.

    **InsertionStringTemplates** contiene el texto que se va a insertar en un evento que especifique en **EventType**. Puede usar cadenas literales o hacer referencia directamente a una propiedad. Para obtener más información, vea [Usar plantillas de cadena estándar](using-standard-string-templates.md) e Instrucción SELECT para consultas de [eventos](select-statement-for-event-queries.md).

    Use un origen existente para el registro de eventos que admita una cadena de inserción sin texto asociado.

    En el ejemplo de código MOF siguiente se muestra cómo usar un origen existente de WSH y un **valor eventID** de 8.

    ```syntax
    instance of NTEventLogEventConsumer as $Consumer
    {
        Name = "RunKeyEventlogConsumer";
        SourceName = "WSH";               
        EventID = 8;
        // Warning                              
        EventType = 2;
        // One string supplies the entire message          
        NumberOfInsertionStrings = 1;             
        // the %Hive% and %KeyPath% are properties of
        // the RegistryKeyChangeEvent instance 
        InsertionStringTemplates = 
            {"The key %Hive%\\%RootPath% has been modified."
            "Check if the change is intentional"};
    };
    ```

3.  Cree una instancia de [**\_ \_ EventFilter y**](--eventfilter.md) defina una consulta para los eventos.

    En el ejemplo siguiente, el filtro supervisa la clave del Registro donde se registran los programas de inicio. La supervisión de esta clave del Registro puede ser importante porque un programa no autorizado puede registrarse en la clave, lo que hace que se inicie cuando se inicie el equipo.

    ```syntax
    instance of __EventFilter as $Filter
    {
    Name = "RunKeyFilter";
    QueryLanguage = "WQL"; 
    Query = "Select * from RegistryTreeChangeEvent"
        " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
        "RootPath = \"Software\\\\Microsoft\\\\Windows"
        "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire in root\default namespace
    EventNamespace = "root\\default";                       
    };
    ```

4.  Identifique un evento para supervisar y crear una consulta de eventos.

    Puede comprobar si hay un evento intrínseco o extrínseco que use. Por ejemplo, use la [**clase RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) del proveedor del Registro para supervisar los cambios en el registro del sistema.

    Si no existe una clase que describa un evento que debe supervisar, debe crear su propio proveedor de eventos y definir nuevas clases de eventos extrínsecos. Para obtener más información, vea [Escribir un proveedor de eventos.](writing-an-event-provider.md)

    En un archivo MOF, puede definir un [*alias*](gloss-a.md) para el filtro y el consumidor, lo que proporciona una manera fácil de describir las rutas de acceso de instancia.

    En el ejemplo siguiente se muestra cómo definir un [*alias*](gloss-a.md) para el filtro y el consumidor.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of LogFileEventConsumer as $CONSUMER
    ```

5.  Cree una instancia de [**\_ \_ FilterToConsumerBinding para**](--filtertoconsumerbinding.md) asociar el filtro y las clases de consumidor. Esta instancia determina que cuando se produce un evento que coincide con el filtro especificado, debe producirse la acción especificada por el consumidor. [**\_ \_ EventFilter,**](--eventfilter.md) [**\_ \_ EventConsumer**](--eventconsumer.md)y **\_ \_ FilterToConsumerBinding** deben tener el mismo identificador de seguridad individual (SID) en la **propiedad CreatorSID.** Para obtener más información, vea [Enlazar un filtro de eventos con un consumidor lógico.](binding-an-event-filter-with-a-logical-consumer.md)

    En el ejemplo siguiente se muestra cómo identificar una instancia por la ruta de acceso del objeto o usar un alias como expresión abreviada para la ruta de acceso del objeto.

    ```syntax
    instance of __EventFilter as $FILTER
    instance of NTEventLogEventConsumer as $CONSUMER
    ```

    En el ejemplo siguiente se enlaza el filtro al consumidor mediante alias.

    ```syntax
    instance of __FilterToConsumerBinding
    {
        Filter = $FILTER;
        Consumer = $CONSUMER;
        
    };
    ```

    Puede enlazar un filtro a varios consumidores, lo que indica que, cuando se producen eventos de coincidencia, se deben realizar varias acciones. o puede enlazar un consumidor a varios filtros, lo que indica que la acción debe realizarse cuando se produzcan eventos que coincidan con uno de los filtros.

    Las siguientes acciones se toman en función de la condición de los consumidores y los eventos:

    -   Si se produce un error en uno de los consumidores permanentes, otros consumidores que solicitan el evento reciben una notificación.
    -   Si se descarta un evento, WMI genera [**\_ \_ EventDroppedEvent**](--eventdroppedevent.md).
    -   Si se suscribe a este evento, devuelve el evento que se ha eliminado y una referencia a [**\_ \_ EventConsumer**](--eventconsumer.md) representa el consumidor con errores.
    -   Si se produce un error en un consumidor, WMI genera [**\_ \_ ConsumerFailureEvent**](--consumerfailureevent.md), que puede contener más información en las propiedades **ErrorCode**, **ErrorDescription** **y ErrorObject.**

    Para obtener más información, vea [Enlazar un filtro de eventos con un consumidor lógico.](binding-an-event-filter-with-a-logical-consumer.md)

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra el MOF de una instancia de [**NTEventLogEventConsumer**](nteventlogeventconsumer.md). Después de compilar este MOF, cualquier intento de crear, eliminar o modificar un valor en la ruta de acceso del Registro **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run** registra una entrada en el registro de eventos de la aplicación, en el origen "WSH".


```mof
#pragma namespace ("\\\\.\\root\\subscription")
 
instance of __EventFilter as $Filter
{
    Name = "RunKeyFilter";
    QueryLanguage = "WQL";
    Query = "Select * from RegistryTreeChangeEvent"
            " where (Hive = \"HKEY_LOCAL_MACHINE\" and "
            "KeyPath = \"Software\\\\Microsoft\\\\Windows"
            "\\\\CurrentVersion\\\\Run\")";

    // RegistryTreeChangeEvents only fire
    // in root\default namespace
    EventNamespace = "root\\default";   
};
 
instance of NTEventLogEventConsumer as $Consumer
{
    Name = "RunKeyEventlogConsumer";
    SourceName = "WSH";               
    EventID = 8;
    EventType = 2;                            // Warning
    Category = 0;
    NumberOfInsertionStrings = 1;

    // the %Hive% and %KeyPath% are properties
    // of the RegistryKeyChangeEvent instance 
    InsertionStringTemplates = {"The key %Hive%\\%RootPath% "
        "has been modified. Check if the change is intentional"};
};
 

// Bind the filter to the consumer
instance of __FilterToConsumerBinding
{
    Filter = $Filter;
    Consumer = $Consumer;
};
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recepción de eventos de forma segura](receiving-events-securely.md)
</dt> </dl>

 

 
