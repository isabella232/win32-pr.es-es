---
description: La instrucción REFERENCEs de recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada.
ms.assetid: 674be546-e7fd-4150-9d7c-2888d24bf1b3
ms.tgt_platform: multiple
title: REFERENCIAS de la instrucción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c7cc624a1e91220fc6bfc89ef0a75878a9cfb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648281"
---
# <a name="references-of-statement"></a><span data-ttu-id="df1f0-103">REFERENCIAS de la instrucción</span><span class="sxs-lookup"><span data-stu-id="df1f0-103">REFERENCES OF Statement</span></span>

<span data-ttu-id="df1f0-104">La instrucción REFERENCEs de recupera todas las instancias de asociación que hacen referencia a una instancia de origen determinada.</span><span class="sxs-lookup"><span data-stu-id="df1f0-104">The REFERENCES OF statement retrieves all association instances that refer to a particular source instance.</span></span> <span data-ttu-id="df1f0-105">La instrucción REFERENCEs de es similar a la instrucción ASSOCIATORS OF en su sintaxis.</span><span class="sxs-lookup"><span data-stu-id="df1f0-105">The REFERENCES OF statement is similar to the ASSOCIATORS OF statement in its syntax.</span></span> <span data-ttu-id="df1f0-106">Sin embargo, en lugar de recuperar instancias de extremo, recupera las instancias de asociación intermedias.</span><span class="sxs-lookup"><span data-stu-id="df1f0-106">However, rather than retrieving endpoint instances, it retrieves the intervening association instances.</span></span>

<span data-ttu-id="df1f0-107">Las referencias de la cláusula WHERE pueden incluir una o varias de las siguientes palabras clave predefinidas y sus valores:</span><span class="sxs-lookup"><span data-stu-id="df1f0-107">The REFERENCES OF WHERE clause can include one or more of the following predefined keywords and their values:</span></span>


```sql
REFERENCES OF {SourceObject} WHERE 
    ClassDefsOnly
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    Role = PropertyName
```



<span data-ttu-id="df1f0-108">Para especificar un objeto de origen, use una ruta de acceso de objeto válida para SourceObject.</span><span class="sxs-lookup"><span data-stu-id="df1f0-108">To specify a source object, use any valid object path for SourceObject.</span></span> <span data-ttu-id="df1f0-109">Al igual que con la instrucción SELECT, la cláusula WHERE es opcional y se usa para definir aún más la consulta.</span><span class="sxs-lookup"><span data-stu-id="df1f0-109">As with the SELECT statement, the WHERE clause is optional and is used to further define the query.</span></span> <span data-ttu-id="df1f0-110">Es decir, la siguiente instrucción es perfectamente válida:</span><span class="sxs-lookup"><span data-stu-id="df1f0-110">That is, the following statement is perfectly valid:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}
```



<span data-ttu-id="df1f0-111">La palabra clave **ClassDefsOnly** indica que la instrucción devuelve un conjunto de resultados de objetos de definición de clase en lugar de instancias reales de las clases de asociación.</span><span class="sxs-lookup"><span data-stu-id="df1f0-111">The **ClassDefsOnly** keyword indicates that the statement returns a result set of class definition objects rather than actual instances of the association classes.</span></span> <span data-ttu-id="df1f0-112">Estos objetos contienen definiciones de las clases a las que pertenecen las instancias que hacen referencia al objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="df1f0-112">These objects contain definitions of classes to which the instances that reference the source object belong.</span></span> <span data-ttu-id="df1f0-113">Por ejemplo, la siguiente instrucción devuelve definiciones para las clases **AdapterDriver** y **AdapterProtocol** :</span><span class="sxs-lookup"><span data-stu-id="df1f0-113">For example, the following statement returns definitions for the **AdapterDriver** and **AdapterProtocol** classes:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ClassDefsOnly
```



<span data-ttu-id="df1f0-114">La palabra clave **RequiredQualifier** indica que los objetos de asociación devueltos deben incluir el calificador especificado.</span><span class="sxs-lookup"><span data-stu-id="df1f0-114">The **RequiredQualifier** keyword indicates that the returned association objects must include the specified qualifier.</span></span> <span data-ttu-id="df1f0-115">La palabra clave **RequiredQualifier** se puede usar para incluir instancias particulares de asociaciones en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="df1f0-115">The **RequiredQualifier** keyword can be used to include particular instances of associations in the result set.</span></span> <span data-ttu-id="df1f0-116">Por ejemplo, la siguiente instrucción devuelve instancias de asociación que incluyen un calificador denominado **AdapterTag**:</span><span class="sxs-lookup"><span data-stu-id="df1f0-116">For example, the following statement returns association instances that include a qualifier called **AdapterTag**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"}  WHERE RequiredQualifier = AdapterTag
```



<span data-ttu-id="df1f0-117">La palabra clave **ResultClass** indica que los objetos de asociación devueltos deben pertenecer a la clase especificada o derivarse de ella.</span><span class="sxs-lookup"><span data-stu-id="df1f0-117">The **ResultClass** keyword indicates that the returned association objects must belong to or be derived from the specified class.</span></span> <span data-ttu-id="df1f0-118">Por ejemplo, la siguiente instrucción devuelve las asociaciones de la clase **AdapterDriver** o las subclases de **AdapterDriver**:</span><span class="sxs-lookup"><span data-stu-id="df1f0-118">For example, the following statement returns associations of the **AdapterDriver** class or subclasses of **AdapterDriver**:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE ResultClass = AdapterDriver
```



<span data-ttu-id="df1f0-119">Las palabras clave **ClassDefsOnly** y **ResultClass** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="df1f0-119">The **ClassDefsOnly** and **ResultClass** keywords are mutually exclusive.</span></span> <span data-ttu-id="df1f0-120">Si se usan conjuntamente, se producirá un error de consulta no válido.</span><span class="sxs-lookup"><span data-stu-id="df1f0-120">Using them together causes an invalid query error.</span></span>

<span data-ttu-id="df1f0-121">La palabra clave **role** indica que las asociaciones devueltas son solo aquellas en las que el objeto de origen desempeña un rol determinado.</span><span class="sxs-lookup"><span data-stu-id="df1f0-121">The **Role** keyword indicates that the returned associations are only those in which the source object plays a particular role.</span></span> <span data-ttu-id="df1f0-122">El rol se define mediante la propiedad especificada, una propiedad de referencia de tipo [ref](references.md). La palabra clave **role** es útil en las asociaciones en las que un determinado objeto puede desempeñar un rol en algunos casos y otro rol en otros, como en las asociaciones jerárquicas.</span><span class="sxs-lookup"><span data-stu-id="df1f0-122">The role is defined by the specified property, a reference property of type [ref](references.md). The **Role** keyword is useful in associations where a certain object can play one role in some cases and another role in others, such as in hierarchical associations.</span></span> <span data-ttu-id="df1f0-123">La palabra clave **role** se puede usar para recuperar todas las asociaciones en las que el objeto de origen desempeña el rol del elemento primario, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="df1f0-123">The **Role** keyword can be used to retrieve all of the associations in which the source object plays the role of parent, for example.</span></span> <span data-ttu-id="df1f0-124">La siguiente instrucción ilustra la sintaxis para recuperar asociaciones que tienen una propiedad **primaria** que hace referencia al objeto de origen como elemento primario:</span><span class="sxs-lookup"><span data-stu-id="df1f0-124">The following statement illustrates the syntax for retrieving associations that have a **parent** property referencing the source object as the parent:</span></span>


```sql
REFERENCES OF {Adapter="AHA-294X"} WHERE Role = parent
```



> [!Note]  
> <span data-ttu-id="df1f0-125">Las consultas complejas no pueden usar "and" o "or" para separar palabras clave para los ASOCIAdores de y las referencias de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="df1f0-125">Complex queries cannot use "And" or "Or" to separate keywords for ASSOCIATORS OF and REFERENCES OF statements.</span></span> <span data-ttu-id="df1f0-126">Además, el signo igual es el único operador válido que se puede usar con las palabras clave en estas consultas.</span><span class="sxs-lookup"><span data-stu-id="df1f0-126">Furthermore, the equal sign is the only valid operator that can be used with the keywords in these queries.</span></span> <span data-ttu-id="df1f0-127">Por ejemplo, la consulta siguiente es válida:</span><span class="sxs-lookup"><span data-stu-id="df1f0-127">For example, the following query is valid:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier = Dynamic"
```



> [!Note]  
> <span data-ttu-id="df1f0-128">Los ejemplos siguientes no son válidos.</span><span class="sxs-lookup"><span data-stu-id="df1f0-128">The next examples are not valid.</span></span> <span data-ttu-id="df1f0-129">En el primer ejemplo no se usa el signo igual y el segundo ejemplo intenta usar erróneamente la palabra clave **y** :</span><span class="sxs-lookup"><span data-stu-id="df1f0-129">The first example does not use the equal sign and the second example erroneously attempts to use the **AND** keyword:</span></span>

 


```sql
"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
    "WHERE resultclass = Win32_NetworkAdapterSetting " +
    "requiredQualifier <> Dynamic"

"REFERENCES OF {Win32_NetworkAdapter.DeviceID="0"} " +
"WHERE resultclass = Win32_NetworkAdapterSetting " +
"AND requiredQualifier = Dynamic"
```



 

 



