---
title: Crear una cláusula WHERE para el proveedor del registro
description: Los puntos principales a tener en cuenta al crear una cláusula WHERE adecuada para el proveedor del registro del sistema es que cada consulta de evento debe ser completa y explícita. Si no se completa y explícita, se producirá un mensaje de error.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498058"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Crear una cláusula WHERE para el proveedor del registro

Los puntos principales a tener en cuenta al crear una cláusula WHERE adecuada para el proveedor del registro del sistema es que cada consulta de evento debe ser completa y explícita. Si no se completa y explícita, se producirá un mensaje de error.

Para completarse, cada consulta de evento en el parámetro *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) debe contener una cláusula WHERE que incluya cada una de las propiedades de la clase de eventos especificada.

En el ejemplo siguiente se muestra cómo establecer *bstrQuery* para registrar los eventos de cambio de árbol en el árbol "HKEY \_ local \_ Machine \\ software".


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Para ser explícito, el proveedor debe ser capaz de deducir de la consulta una lista de valores posibles para cada propiedad de la clase de evento.

En el ejemplo siguiente se muestra la consulta de eventos que se registra correctamente para los eventos de cambio de árbol.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



El siguiente es un ejemplo de registro incorrecto.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Dado que no hay forma de evaluar los valores posibles para cada una de las propiedades, WMI rechaza con el error WBEM \_ E es \_ demasiado \_ amplio cualquier consulta que no tenga una cláusula WHERE o si la cláusula WHERE es demasiado amplia para ser de cualquier uso.

 

 



