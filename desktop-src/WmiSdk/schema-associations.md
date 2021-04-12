---
description: 'Las consultas de Asociación de esquema usan las mismas instrucciones que se utilizan en las consultas de Asociación de datos: ASOCIAdores de y referencias de.'
ms.assetid: b5fc2d86-702a-42cd-82e6-f15c905ba6aa
ms.tgt_platform: multiple
title: Asociaciones de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea2f0c3b753bf4657c66a635319bab7dbe435a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278761"
---
# <a name="schema-associations"></a><span data-ttu-id="074d1-103">Asociaciones de esquema</span><span class="sxs-lookup"><span data-stu-id="074d1-103">Schema Associations</span></span>

<span data-ttu-id="074d1-104">Las consultas de Asociación de esquema usan las mismas instrucciones que se utilizan en las consultas de Asociación de datos: ASOCIAdores de y referencias de.</span><span class="sxs-lookup"><span data-stu-id="074d1-104">Schema association queries use the same statements as are used in data association queries: ASSOCIATORS OF and REFERENCES OF.</span></span> <span data-ttu-id="074d1-105">Sin embargo, con las consultas de Asociación de datos, se devuelven instancias de clase y con consultas de Asociación de esquema, se devuelven los nombres de las clases que pueden participar en las relaciones de asociación.</span><span class="sxs-lookup"><span data-stu-id="074d1-105">However, with data association queries, class instances are returned, and with schema association queries, names of classes that can participate in association relationships are returned.</span></span> <span data-ttu-id="074d1-106">Por ejemplo, utilice una consulta de esquema para buscar todas las clases de asociación definidas en el esquema que hacen referencia a una clase de origen.</span><span class="sxs-lookup"><span data-stu-id="074d1-106">For example, use a schema query to find all of the association classes defined in the schema that reference a source class.</span></span>

<span data-ttu-id="074d1-107">La sintaxis de los ASOCIAdores de y las referencias de las instrucciones de es la misma para las consultas de Asociación de esquema que para las consultas de Asociación de datos con las excepciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="074d1-107">The syntax for the ASSOCIATORS OF and REFERENCES OF statements is the same for schema association queries as it is for data association queries with the following exceptions:</span></span>

-   <span data-ttu-id="074d1-108">El objeto de origen es una clase en lugar de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="074d1-108">The source object is a class rather than an instance.</span></span>
-   <span data-ttu-id="074d1-109">Hay una palabra clave adicional, **SchemaOnly**, que identifica la consulta como aplicable a un esquema en lugar de a los datos.</span><span class="sxs-lookup"><span data-stu-id="074d1-109">There is an additional keyword, **SchemaOnly**, which identifies the query as applying to a schema rather than to data.</span></span>
-   <span data-ttu-id="074d1-110">La palabra clave **ClassDefsOnly** no es válida.</span><span class="sxs-lookup"><span data-stu-id="074d1-110">The **ClassDefsOnly** keyword is not valid.</span></span>

<span data-ttu-id="074d1-111">En el ejemplo siguiente se muestra la sintaxis completa de la instrucción ASSOCIATORS OF para una consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="074d1-111">The following example shows the complete syntax of the ASSOCIATORS OF statement for a schema query.</span></span> <span data-ttu-id="074d1-112">Para obtener información detallada sobre la sintaxis, vea [ASSOCIATORS OF Statement](associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="074d1-112">For detailed syntax, see [ASSOCIATORS OF Statement](associators-of-statement.md).</span></span>


```sql
ASSOCIATORS OF {SourceClass} WHERE 
    AssocClass = AssocClassName
    RequiredAssocQualifier = QualifierName
    RequiredQualifier = QualifierName
    ResultClass = ClassName
    ResultRole = PropertyName
    Role = PropertyName
    SchemaOnly
```



<span data-ttu-id="074d1-113">En el ejemplo siguiente se muestra una consulta que devuelve las clases de **controlador** y de **Protocolo** , las dos clases que hacen referencia a la clase de origen.</span><span class="sxs-lookup"><span data-stu-id="074d1-113">The following example shows a query that returns the **Protocol** and **Driver** classes, the two classes that refer to the source class.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE SchemaOnly
```



<span data-ttu-id="074d1-114">La consulta siguiente devuelve solo la clase de **controlador** debido a la restricción colocada por la palabra clave **AssocClass** .</span><span class="sxs-lookup"><span data-stu-id="074d1-114">The following query returns only the **Driver** class because of the restriction placed by the **AssocClass** keyword.</span></span>


```sql
ASSOCIATORS OF {Adapter} WHERE AssocClass = AdapterDriver SchemaOnly
```



<span data-ttu-id="074d1-115">La sintaxis completa de las referencias de la instrucción para una consulta de esquema es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="074d1-115">The complete syntax of the REFERENCES OF statement for a schema query is as follows.</span></span> <span data-ttu-id="074d1-116">Para obtener información detallada sobre la sintaxis, vea [References of Statement](references-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="074d1-116">For detailed syntax, see [REFERENCES OF Statement](references-of-statement.md).</span></span>


```sql
REFERENCES OF {SourceClass} WHERE
    ResultClass = ClassName
    Role = PropertyName
    RequiredQualifier = QualifierName
    SchemaOnly
```



> [!Note]  
> <span data-ttu-id="074d1-117">Las consultas de Asociación de esquema pueden devolver objetos duplicados.</span><span class="sxs-lookup"><span data-stu-id="074d1-117">Schema association queries may return duplicate objects.</span></span>

 

<span data-ttu-id="074d1-118">Por ejemplo, la siguiente consulta devolverá la clase [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) varias veces al enumerar las clases en el espacio de nombres **root \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="074d1-118">For example, the following query will return the class [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) several times when enumerating classes in the **root\\cimv2** namespace.</span></span>


```sql
ASSOCIATORS OF {Win32_ComputerSystem} WHERE SchemaOnly
```



 

 
