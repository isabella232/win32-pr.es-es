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
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="eb612-104">Crear una cláusula WHERE para el proveedor del registro</span><span class="sxs-lookup"><span data-stu-id="eb612-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="eb612-105">Los puntos principales a tener en cuenta al crear una cláusula WHERE adecuada para el proveedor del registro del sistema es que cada consulta de evento debe ser completa y explícita.</span><span class="sxs-lookup"><span data-stu-id="eb612-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="eb612-106">Si no se completa y explícita, se producirá un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="eb612-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="eb612-107">Para completarse, cada consulta de evento en el parámetro *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) debe contener una cláusula WHERE que incluya cada una de las propiedades de la clase de eventos especificada.</span><span class="sxs-lookup"><span data-stu-id="eb612-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="eb612-108">En el ejemplo siguiente se muestra cómo establecer *bstrQuery* para registrar los eventos de cambio de árbol en el árbol "HKEY \_ local \_ Machine \\ software".</span><span class="sxs-lookup"><span data-stu-id="eb612-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="eb612-109">Para ser explícito, el proveedor debe ser capaz de deducir de la consulta una lista de valores posibles para cada propiedad de la clase de evento.</span><span class="sxs-lookup"><span data-stu-id="eb612-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="eb612-110">En el ejemplo siguiente se muestra la consulta de eventos que se registra correctamente para los eventos de cambio de árbol.</span><span class="sxs-lookup"><span data-stu-id="eb612-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="eb612-111">El siguiente es un ejemplo de registro incorrecto.</span><span class="sxs-lookup"><span data-stu-id="eb612-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="eb612-112">Dado que no hay forma de evaluar los valores posibles para cada una de las propiedades, WMI rechaza con el error WBEM \_ E es \_ demasiado \_ amplio cualquier consulta que no tenga una cláusula WHERE o si la cláusula WHERE es demasiado amplia para ser de cualquier uso.</span><span class="sxs-lookup"><span data-stu-id="eb612-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



