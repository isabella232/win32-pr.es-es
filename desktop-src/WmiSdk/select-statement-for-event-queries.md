---
description: Describe la sintaxis básica de una instrucción SELECT para las consultas de eventos.
ms.assetid: 8882fdcb-3768-41e3-82ab-3006d903f3a0
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab840072269d04987bf42939f1f566ee6b99afab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278762"
---
# <a name="select-statement-for-event-queries"></a>Instrucción SELECT para consultas de eventos

Puede utilizar una serie de instrucciones SELECT para consultar información de eventos. Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.

El ejemplo siguiente es una instrucción SELECT básica que se utiliza para consultar la información de eventos.


```sql
SELECT * FROM EventClass
```



Cuando un consumidor envía una consulta, se trata de una solicitud para recibir notificaciones de todas las repeticiones del evento representado por **EventClass**. Esta solicitud incluye una solicitud de notificación sobre todas las propiedades del sistema de eventos y las que no son del sistema. Cuando un proveedor de eventos envía una consulta, registra la compatibilidad para generar notificaciones cuando se produce un evento representado por **EventClass** .

Los consumidores pueden especificar propiedades individuales en lugar del asterisco ( \* ) en la instrucción SELECT.

En el ejemplo siguiente se muestra cómo consultar propiedades específicas.


```sql
SELECT property_1, property_2, property_3 FROM MyEventClass
```



Sin embargo, se devuelven todas las propiedades de un objeto incrustado, aunque la consulta especifique las propiedades del objeto incrustado.

En el ejemplo siguiente se muestran dos consultas que devuelven los mismos datos.


```sql
SELECT targetInstance FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```




```sql
SELECT targetInstance.Name FROM __InstanceCreationEvent within 2
    WHERE targetinstance isa "Win32_Process"
```



Si una propiedad del sistema no es relevante para una consulta específica, contiene **null**. Por ejemplo, el valor de la propiedad del sistema **\_ \_ RELPATH** es **null** para todas las consultas de eventos.

Las siguientes propiedades del sistema contienen **valores NULL** para las consultas de eventos:

<dl> \_\_System.IO  
\_\_Camino  
\_\_RelPath  
\_\_Servidor  
</dl>

Para obtener más información, vea [referencia de propiedades del sistema WMI](wmi-system-properties.md).

Todas las consultas de eventos pueden incluir una [cláusula WHERE](where-clause.md)opcional, pero los consumidores usan principalmente las cláusulas WHERE para especificar filtros adicionales. Se recomienda encarecidamente que los consumidores especifiquen siempre una cláusula WHERE. El costo de una consulta compleja es mínimo en comparación con el costo de entrega y procesamiento de notificaciones innecesarias.

En el ejemplo siguiente se muestra una consulta que solicita notificaciones de todos los eventos de modificación de instancia que afectan a la clase hipotética **EmailEvent**.


```sql
SELECT * FROM EmailEvent
```



Si los eventos asociados a **EmailEvent** se producen con frecuencia, el consumidor se inunda con eventos. Una consulta mejor solicita eventos solo cuando las condiciones específicas usan propiedades de la clase especificada, como cuando el nivel de importancia es alto.

En el ejemplo siguiente se muestra la consulta que se puede usar si **EmailImportance** es una propiedad de la clase **EmailEvent**.


```sql
SELECT * FROM EmailEvent WHERE EmailImportance > 3
```



Tenga en cuenta que WMI puede rechazar una consulta por una serie de motivos. Por ejemplo, la consulta puede ser demasiado compleja o consumir muchos recursos para su evaluación. Cuando esto ocurre, WMI devuelve códigos de error específicos, como **la \_ \_ \_ consulta no válida WBEM E**.

Las propiedades de los objetos incrustados se pueden usar en la cláusula WHERE.

En el ejemplo siguiente se muestra cómo consultar objetos en los que la propiedad **TargetInstance** de la clase del sistema [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) es un objeto [**\_ LogicalDisk Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) incrustado y **FreeSpace** es una propiedad de **Win32 \_ LogicalDisk**.


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
    WHERE TargetInstance ISA "Win32_LogicalDisk" 
    AND   TargetInstance.FreeSpace < 1000000
```



## <a name="examples"></a>Ejemplos

El [evento de creación de monitor para el nombre de proceso específico](https://Gallery.TechNet.Microsoft.Com/52716121-f386-49de-86cd-46ca54d1714f) ejemplo de VBScript en TechNet usa la instrucción SELECT para supervisar los eventos de creación de instancia de WMI para \_ el proceso de Win32, filtrando por un nombre de proceso específico.

 

 
