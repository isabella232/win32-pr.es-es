---
description: Describir la instrucción SELECT para una consulta de datos.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06905cfd9ef5e55022b3fc2275ed705a670a0ecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706081"
---
# <a name="select-statement-for-data-queries"></a><span data-ttu-id="27ee3-103">Instrucción SELECT para consultas de datos</span><span class="sxs-lookup"><span data-stu-id="27ee3-103">SELECT Statement for Data Queries</span></span>

<span data-ttu-id="27ee3-104">Puede utilizar una serie de instrucciones SELECT para consultar información.</span><span class="sxs-lookup"><span data-stu-id="27ee3-104">You can use a variety of SELECT statements to query for information.</span></span> <span data-ttu-id="27ee3-105">Las instrucciones pueden ser instrucciones básicas o pueden ser más restrictivas para restringir el conjunto de resultados que se devuelve de la consulta.</span><span class="sxs-lookup"><span data-stu-id="27ee3-105">The statements can be basic statements or they can be more restrictive to narrow the result set that is returned from the query.</span></span>

<span data-ttu-id="27ee3-106">El ejemplo siguiente es una instrucción SELECT básica que se utiliza para consultar datos.</span><span class="sxs-lookup"><span data-stu-id="27ee3-106">The following example is a basic SELECT statement that is used to query for data.</span></span>


```sql
SELECT * FROM Class
```



<span data-ttu-id="27ee3-107">Esta instrucción devuelve instancias de la clase especificada y cualquiera de sus subclases.</span><span class="sxs-lookup"><span data-stu-id="27ee3-107">This statement returns instances of the specified class and any of its subclasses.</span></span> <span data-ttu-id="27ee3-108">Se incluyen todas las propiedades del sistema y definidas por el usuario para las clases.</span><span class="sxs-lookup"><span data-stu-id="27ee3-108">All of the system and user-defined properties for the classes are included.</span></span> <span data-ttu-id="27ee3-109">Si una propiedad del sistema no es relevante para una consulta determinada, contiene **null**.</span><span class="sxs-lookup"><span data-stu-id="27ee3-109">If a system property is not relevant for a particular query, it contains **NULL**.</span></span>

<span data-ttu-id="27ee3-110">Puede usar varias técnicas para reducir el ancho de banda necesario para recuperar el conjunto de resultados, si la ejecución de la consulta produce demasiada sobrecarga y el usuario solo está interesado en un subconjunto de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="27ee3-110">You can use several techniques to reduce the bandwidth required to retrieve the result set, if the execution of the query results in too much overhead and the user is only interested in a subset of the properties.</span></span> <span data-ttu-id="27ee3-111">En primer lugar, las consultas pueden reemplazar el asterisco por las propiedades deseadas.</span><span class="sxs-lookup"><span data-stu-id="27ee3-111">First, queries can replace the asterisk with the desired properties.</span></span>

<span data-ttu-id="27ee3-112">En el ejemplo siguiente se muestra cómo consultar propiedades específicas.</span><span class="sxs-lookup"><span data-stu-id="27ee3-112">The following example shows how to query for specific properties.</span></span>


```sql
SELECT property_1, property_2, property_3 FROM class
```



<span data-ttu-id="27ee3-113">El conjunto de resultados incluye todas las propiedades del sistema y las propiedades que no son del sistema especificadas.</span><span class="sxs-lookup"><span data-stu-id="27ee3-113">The result set includes all system properties and the specified nonsystem properties.</span></span>

<span data-ttu-id="27ee3-114">Otra técnica para limitar el ámbito del conjunto de resultados de una consulta es usar la propiedad del sistema de [**\_ \_ clase**](wmi-system-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="27ee3-114">Another technique for narrowing the scope of a query's result set is to use the [**\_\_CLASS**](wmi-system-properties.md) system property.</span></span> <span data-ttu-id="27ee3-115">De forma predeterminada, las consultas devuelven todas las instancias de la clase especificada y sus subclases.</span><span class="sxs-lookup"><span data-stu-id="27ee3-115">Queries by default return all instances of the specified class and its subclasses.</span></span> <span data-ttu-id="27ee3-116">Puede usar la propiedad System de **\_ \_ clase** para solicitar solo las instancias de la clase especificada, excluidas sus subclases.</span><span class="sxs-lookup"><span data-stu-id="27ee3-116">You can use the **\_\_CLASS** system property to request only instances of the specified class, excluding its subclasses.</span></span>

<span data-ttu-id="27ee3-117">En el ejemplo siguiente se muestra cómo usar la propiedad System de [**\_ \_ clase**](wmi-system-properties.md) en una cláusula WHERE.</span><span class="sxs-lookup"><span data-stu-id="27ee3-117">The following example shows how to use the [**\_\_CLASS**](wmi-system-properties.md) system property in a WHERE clause.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



<span data-ttu-id="27ee3-118">También puede usar la propiedad System de [**\_ \_ clase**](wmi-system-properties.md) para restringir el conjunto de resultados a las instancias de subclases determinadas.</span><span class="sxs-lookup"><span data-stu-id="27ee3-118">You can also use the [**\_\_CLASS**](wmi-system-properties.md) system property to restrict the result set to instances of particular subclasses.</span></span>

<span data-ttu-id="27ee3-119">En el ejemplo siguiente se muestra cómo restringir el conjunto de resultados a instancias de subclases determinadas.</span><span class="sxs-lookup"><span data-stu-id="27ee3-119">The following example shows how to restrict the result set to instances of particular subclasses.</span></span>


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> <span data-ttu-id="27ee3-120">Si crea una consulta con una ruta de acceso no válida para un objeto incrustado, la consulta no devuelve ningún error ni ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="27ee3-120">If you construct a query with an invalid path for an embedded object, your query does not return an error or any results.</span></span>

 

<span data-ttu-id="27ee3-121">En el ejemplo siguiente se devuelve una instancia de **mainclass**, suponiendo que existe una instancia de **mainclass** que contiene el objeto incrustado **EmbedObj** con una propiedad **P \_ Uint32** que es igual a "70011".</span><span class="sxs-lookup"><span data-stu-id="27ee3-121">The following example returns an instance of **MainClass**, assuming that an instance of **MainClass** exists containing the embedded object **EmbedObj** with a property **P\_Uint32** that is equal to "70011".</span></span>


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



<span data-ttu-id="27ee3-122">En el ejemplo siguiente no se devuelve ningún resultado y no se devuelve un error, suponiendo que el objeto incrustado **EmbedObj** en la instancia de **MainClass** no tiene una propiedad no **válida**.</span><span class="sxs-lookup"><span data-stu-id="27ee3-122">The following example returns no results and does not return an error, assuming that the embedded object **EmbedObj** in the instance of **MainClass** does not have a property **INVALID**.</span></span>


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



