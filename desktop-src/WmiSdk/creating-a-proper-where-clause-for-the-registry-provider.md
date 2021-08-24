---
title: Creación de una cláusula WHERE para el proveedor del Registro
description: Los puntos principales que se deben tener en cuenta al crear una cláusula WHERE adecuada para el proveedor del Registro del sistema es que cada consulta de eventos debe ser completa y explícita. Si no se completa y se explicita, se producirá un mensaje de error.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0fc037b746233bd9eb2f9bdd4afad942d07dc832b4dfd60cd9ca6ae9f273efca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679835"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Creación de una cláusula WHERE para el proveedor del Registro

Los puntos principales que se deben tener en cuenta al crear una cláusula WHERE adecuada para el proveedor del Registro del sistema es que cada consulta de eventos debe ser completa y explícita. Si no se completa y se explicita, se producirá un mensaje de error.

Para completarse, cada consulta de eventos del parámetro *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) debe contener una cláusula WHERE que incluya cada una de las propiedades de la clase de eventos especificada.

En el ejemplo siguiente se muestra cómo establecer *bstrQuery para registrar* eventos de cambio de árbol en el árbol "HKEY \_ LOCAL MACHINE \_ \\ Software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Para ser explícito, el proveedor debe poder deducir de la consulta una lista de valores posibles para cada propiedad de la clase de evento.

En el ejemplo siguiente se muestra la consulta de eventos que se registra correctamente para los eventos de cambio de árbol.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



A continuación se muestra un ejemplo de un registro incorrecto.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Dado que no hay ninguna manera de evaluar los valores posibles para cada una de las propiedades, WMI rechaza con el error WBEM E TOO BROAD cualquier consulta que no tenga una cláusula WHERE o si la cláusula WHERE es demasiado amplia para ser de cualquier \_ \_ \_ uso.

 

 



