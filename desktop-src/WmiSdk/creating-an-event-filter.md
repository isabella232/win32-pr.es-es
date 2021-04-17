---
description: Un filtro de eventos es una clase WMI que describe qué eventos entrega WMI a un consumidor físico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Crear un filtro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 693e4ef2eee5de14550b8efbf25a9b6720d6a8b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717203"
---
# <a name="creating-an-event-filter"></a>Crear un filtro de eventos

Un filtro de eventos es una clase WMI que describe qué eventos entrega WMI a un consumidor físico. Por ejemplo, un filtro de eventos puede indicar a WMI que entregue a un consumidor todos los eventos de administración de energía o todos los eventos de reinicio del sistema. Un filtro de eventos también describe las condiciones en las que WMI entrega los eventos. Un filtro de eventos puede especificar un evento intrínseco o extrínseco; y el filtro puede hacer referencia a los eventos que se originan en el espacio de nombres, es decir, que no sean el espacio de nombres del filtro. El consumidor permanente debe tener el mismo [**CreatorSID**](--eventconsumer.md) en las instancias de consumidor, filtro y enlace. Para obtener más información, consulte [recepción de eventos de forma segura](receiving-events-securely.md).

En el procedimiento siguiente se describe cómo crear un filtro de eventos.

**Para crear un filtro de eventos**

1.  Cree una instancia de la clase del sistema [**\_ \_ EventFilter**](--eventfilter.md) de WMI.
2.  Cree un identificador único para el filtro con la propiedad **Name** , de una de estas dos maneras:

    -   Use un esquema privado.

        El nombre arbitrario de los filtros de eventos funciona siempre y cuando no esté en conflicto con otros esquemas de nomenclatura de filtros. Debe evitar conflictos de nombres porque al agregar una instancia con un valor de **nombre** duplicado se sobrescribe la instancia anterior.

    -   Use un identificador único global (GUID).

        Si deja **el nombre** vacío, WMI rellena **el nombre** con un GUID.

3.  Describa el tipo de evento que desea filtrar con la propiedad de **consulta** .

    La propiedad **query** contiene la consulta de lenguaje de consulta de WMI (WQL) que describe el tipo de evento que desea filtrar. Puede lograr un filtrado preciso mediante una variedad de operadores y extensiones para WQL.

    Un evento de registro NT se genera cuando se produce un error en una consulta de un consumidor de eventos permanente. El origen del evento es WinMgmt, el ID. de evento es 10 y el tipo de evento es error.

    WMI es más eficaz en el procesamiento de consultas específicas y restrictivas que las consultas amplias. Mediante la creación de una consulta específica, puede evitar la comunicación entre procesos y el tráfico de red innecesarios. En los casos de eventos generados por un proveedor, WMI realiza el filtrado en proceso para el proveedor; Esto garantiza que solo los eventos que coinciden con el filtro incurren en el costo de comunicación entre procesos. Para obtener más información, consulte [consultar WMI](querying-wmi.md).

4.  Establezca la propiedad **QueryLanguage** en el tipo de lenguaje de consulta que use en la propiedad **query** .

    Casi siempre se establece **QueryLanguage** en "WQL".

En el ejemplo de código siguiente se describe un filtro de eventos que señala a un evento cada vez que WMI crea una instancia de la clase [**\_ \_ TimerEvent**](--timerevent.md) en el \\ espacio de nombres root cimv2.

``` syntax
instance of __EventFilter as $FILTER
{
    Name = "MyFilterName";
    Query = "select * from __TimerEvent where TimerID=\"MyTimer\"";
    QueryLanguage = "WQL";
    EventNamespace = "\root\cimv2";

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

La propiedad **EventNamespace** especifica el espacio de nombres desde el que se originan los eventos. No es necesario crear una instancia de los filtros en el espacio de nombres en el que se originan los eventos. Si no especifica el espacio de nombres, WMI crea el filtro en el espacio de nombres predeterminado. Las clases de eventos intrínsecos, como [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md) , están disponibles en todos los espacios de nombres.

Para registrar el consumidor lógico para las notificaciones de eventos, debe enlazar los filtros de eventos a un consumidor lógico. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

 

 



