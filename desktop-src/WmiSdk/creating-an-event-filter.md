---
description: Un filtro de eventos es una clase WMI que describe los eventos que WMI entrega a un consumidor físico.
ms.assetid: c0ce26a4-5ff2-44b4-8550-c7d8ad0ba0f0
ms.tgt_platform: multiple
title: Creación de un filtro de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f44f49c9a7f38b23353dc8c6343ca1d72194e3b7f121538c93f545e45c31e3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568835"
---
# <a name="creating-an-event-filter"></a>Creación de un filtro de eventos

Un filtro de eventos es una clase WMI que describe los eventos que WMI entrega a un consumidor físico. Por ejemplo, un filtro de eventos puede indicar a WMI que entregue a un consumidor todos los eventos de administración de energía o todos los eventos de reinicio del sistema. Un filtro de eventos también describe las condiciones en las que WMI entrega los eventos. Un filtro de eventos puede especificar un evento intrínseco o extrínseco; y el filtro puede hacer referencia a eventos que se originan en el espacio de nombres , es decir, que no sea el espacio de nombres del filtro. El consumidor permanente debe tener el mismo [**CreatorSID**](--eventconsumer.md) en las instancias de consumidor, filtro y enlace. Para obtener más información, [vea Recepción de eventos de forma segura.](receiving-events-securely.md)

En el procedimiento siguiente se describe cómo crear un filtro de eventos.

**Para crear un filtro de eventos**

1.  Cree una instancia de la clase [**\_ \_ del sistema EventFilter**](--eventfilter.md) de WMI.
2.  Cree un identificador único para el filtro con la **propiedad Name** de una de estas dos maneras:

    -   Use un esquema privado.

        El nombre arbitrario de los filtros de eventos funciona siempre que no entre en conflicto con otros esquemas de nomenclatura de filtros. Debe evitar conflictos de nomenclatura porque al agregar una instancia con un valor **name** duplicado se sobrescribe la instancia anterior.

    -   Use un identificador único global (GUID).

        Si deja nombre **vacío,** WMI rellena **nombre** con un GUID.

3.  Describa el tipo de evento que desea filtrar con la **propiedad Query.**

    La **propiedad Query** contiene la lenguaje de consulta de WMI (WQL) que describe el tipo de evento que desea filtrar. Puede lograr un filtrado preciso mediante una variedad de operadores y extensiones para WQL.

    Se genera un evento de registro NT cuando se produce un error en una consulta de un consumidor de eventos permanente. El origen del evento es WinMgmt, el identificador de evento es 10 y el tipo de evento es Error.

    WMI es más eficaz en el procesamiento de consultas específicas restrictivas que las consultas generales. Al crear una consulta específica, puede evitar la comunicación entre procesos innecesaria y el tráfico de red. En los casos de eventos generados por un proveedor, WMI realiza el filtrado en proceso al proveedor; esto garantiza que solo los eventos que coincidan con el filtro incurran en el costo de comunicación entre procesos. Para obtener más información, [vea Consulta de WMI.](querying-wmi.md)

4.  Establezca la **propiedad QueryLanguage en** el tipo de lenguaje de consulta que se usa en la **propiedad Query.**

    Casi siempre establecerá **QueryLanguage en** "WQL".

En el ejemplo de código siguiente se describe un filtro de eventos que señala un evento cada vez que WMI crea una instancia de la [**\_ \_ clase TimerEvent**](--timerevent.md) en el espacio de nombres \\ cimv2 raíz.

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

La **propiedad EventNamespace** especifica el espacio de nombres desde el que se originan los eventos. No es necesario crear una instancia de los filtros en el espacio de nombres donde se originan los eventos. Si no especifica el espacio de nombres, WMI crea el filtro en el espacio de nombres predeterminado. Las clases de eventos intrínsecos, [**\_ \_ como InstanceOperationEvent,**](--instanceoperationevent.md) están disponibles en cada espacio de nombres.

Para registrar el consumidor lógico para las notificaciones de eventos, debe enlazar los filtros de eventos a un consumidor lógico. Para obtener más información, vea [Enlazar un filtro de eventos con un consumidor lógico.](binding-an-event-filter-with-a-logical-consumer.md)

 

 



