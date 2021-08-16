---
description: Describe la sintaxis básica de una instrucción SELECT para las consultas de eventos.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e36eaa8f396f8dd7b7c0b0c013d1d6738fefeb7ed2ae565ee7114ebb524faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315844"
---
# <a name="select-statement-for-event-queries"></a>Instrucción SELECT para consultas de eventos

Puede usar una variedad de instrucciones SELECT para consultar la información del evento. Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.

El ejemplo siguiente es una instrucción SELECT básica que se usa para consultar información de eventos.


```sql
SELECT * FROM EventClass
```



Cuando un consumidor envía una consulta, es una solicitud para recibir una notificación de todas las apariciones del evento representado por **EventClass**. Esta solicitud incluye una solicitud de notificación sobre todas las propiedades del sistema de eventos y no del sistema. Cuando un proveedor de eventos envía una consulta, registra la compatibilidad para generar notificaciones cuando se produce un evento representado **por EventClass.**

Los consumidores pueden especificar propiedades individuales en lugar del asterisco ( \* ) en la instrucción SELECT.

En el ejemplo siguiente se muestra cómo consultar propiedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Sin embargo, se devuelven todas las propiedades de un objeto incrustado, incluso si la consulta especifica propiedades de objeto incrustado.

En el ejemplo siguiente se muestran dos consultas que devuelven los mismos datos.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Si una propiedad del sistema no es relevante para una consulta específica, contiene **NULL.** Por ejemplo, el valor de la propiedad del sistema **\_ \_ RELPATH** es **NULL para** todas las consultas de eventos.

Las siguientes propiedades del sistema contienen **NULL para** las consultas de eventos:

<dl> \_\_Nombres  
\_\_Camino  
\_\_RelPath  
\_\_Servidor  
</dl>

Para obtener más información, vea [Referencia de propiedades del sistema WMI.](wmi-system-properties.md)

Todas las consultas de eventos pueden incluir una cláusula [WHERE](where-clause.md)opcional, pero los consumidores usan principalmente las cláusulas WHERE para especificar un filtrado adicional. Se recomienda encarecidamente que los consumidores siempre especifiquen una cláusula WHERE. El costo de una consulta compleja es mínimo en comparación con el costo de entregar y procesar notificaciones innecesarios.

En el ejemplo siguiente se muestra una consulta que solicita notificaciones de todos los eventos de modificación de instancias que afectan a la clase hipotética **EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Si los eventos asociados **a EmailEvent** se producen con frecuencia, el consumidor se desborda con eventos. Una consulta mejor solicita eventos solo cuando condiciones específicas usan propiedades de la clase especificada, como cuando el nivel de importancia es alto.

En el ejemplo siguiente se muestra la consulta que puede usar si **EmailImportance** es una propiedad de la clase **EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Tenga en cuenta que WMI puede rechazar una consulta por varios motivos. Por ejemplo, la consulta puede ser demasiado compleja o con un uso intensivo de recursos para la evaluación. Cuando esto sucede, WMI devuelve códigos de error específicos, como **WBEM \_ E INVALID \_ \_ QUERY**.

Las propiedades de los objetos incrustados se pueden usar en la cláusula WHERE.

En el ejemplo siguiente se muestra cómo consultar objetos donde la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) es un objeto [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incrustado y **FreeSpace** es una propiedad de **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Ejemplos

El ejemplo de VBScript monitor creation event for [specific process name](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) on TechNet usa la instrucción SELECT para supervisar los eventos de creación de instancias WMI para el proceso Win32, filtrando por un nombre de proceso \_ específico.

 

 
