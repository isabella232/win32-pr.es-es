---
description: Las consultas de datos de esquema utilizan la instrucción SELECT con una sintaxis similar a la de las consultas de datos.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278760"
---
# <a name="select-statement-for-schema-queries"></a><span data-ttu-id="29a6d-103">Instrucción SELECT para consultas de esquema</span><span class="sxs-lookup"><span data-stu-id="29a6d-103">SELECT Statement for Schema Queries</span></span>

<span data-ttu-id="29a6d-104">Las consultas de datos de esquema utilizan la instrucción SELECT con una sintaxis similar a la de [las consultas de datos](select-statement-for-data-queries.md).</span><span class="sxs-lookup"><span data-stu-id="29a6d-104">Schema data queries use the SELECT statement with a syntax similar to that for [data queries](select-statement-for-data-queries.md).</span></span> <span data-ttu-id="29a6d-105">La diferencia es el uso de una clase especial denominada "meta \_ Class", que identifica la consulta como una consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="29a6d-105">The difference is the use of a special class called "meta\_class", which identifies the query as a schema query.</span></span>

<span data-ttu-id="29a6d-106">En el ejemplo siguiente se solicitan todas las definiciones de clase que se encuentran en el espacio de nombres actual.</span><span class="sxs-lookup"><span data-stu-id="29a6d-106">The following example requests all class definitions that are within the current namespace.</span></span>


```sql
SELECT * FROM meta_class
```



<span data-ttu-id="29a6d-107">Las consultas de esquema solo admiten " \* ".</span><span class="sxs-lookup"><span data-stu-id="29a6d-107">Schema queries only support "\*".</span></span> <span data-ttu-id="29a6d-108">Para restringir el ámbito de las definiciones devueltas, un proveedor puede Agregar una cláusula WHERE que especifique una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="29a6d-108">To narrow the scope of the definitions returned, a provider can add a WHERE clause that specifies a particular class.</span></span>

<span data-ttu-id="29a6d-109">En el ejemplo siguiente se muestra cómo agregar una cláusula WHERE para especificar una clase determinada.</span><span class="sxs-lookup"><span data-stu-id="29a6d-109">The following example shows how to add a WHERE clause to specify a particular class.</span></span>


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



<span data-ttu-id="29a6d-110">La propiedad **\_ \_ especial llamada identifica** la clase de destino de una consulta de esquema.</span><span class="sxs-lookup"><span data-stu-id="29a6d-110">The special property called **\_\_this** identifies the target class for a schema query.</span></span> <span data-ttu-id="29a6d-111">Tenga en cuenta que el operador ISA debe usarse con la propiedad **\_ \_ this** para solicitar definiciones para las subclases de la clase de destino.</span><span class="sxs-lookup"><span data-stu-id="29a6d-111">Note that the ISA operator must be used with the **\_\_this** property to request definitions for the subclasses of the target class.</span></span> <span data-ttu-id="29a6d-112">La consulta anterior devuelve la definición de la clase y las definiciones de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) para todas sus subclases.</span><span class="sxs-lookup"><span data-stu-id="29a6d-112">The preceding query returns the definition for the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class and definitions for all of its subclasses.</span></span>

<span data-ttu-id="29a6d-113">En el ejemplo siguiente se muestra cómo solicitar una definición de clase para una sola clase mediante la propiedad del sistema de **\_ \_ clase** .</span><span class="sxs-lookup"><span data-stu-id="29a6d-113">The following example shows how to request a class definition for a single class by using the **\_\_Class** system property.</span></span>


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



<span data-ttu-id="29a6d-114">Esta consulta es equivalente a llamar al método [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) con el parámetro Path del objeto establecido en "Win32 \_ LogicalDisk".</span><span class="sxs-lookup"><span data-stu-id="29a6d-114">This query is equivalent to calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or the [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) method with the object path parameter set to "Win32\_LogicalDisk".</span></span>

<span data-ttu-id="29a6d-115">El siguiente ejemplo de código de VBScript recupera todas las clases secundarias de una clase WMI de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="29a6d-115">The following VBScript code sample retrieves all child classes of a top level WMI class.</span></span> <span data-ttu-id="29a6d-116">La \_ \_ propiedad del sistema WMI Dynasty contiene el nombre de la clase de nivel superior de la que se deriva una clase, que se puede utilizar para recuperar todas las clases de un espacio de nombres derivado de una clase de nivel superior, incluida esa clase.</span><span class="sxs-lookup"><span data-stu-id="29a6d-116">The \_\_Dynasty WMI system property holds the name of the top-level class from which a class is derived, which you can use to retrieve all classes in a namespace derived from a top level class, including that class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Dynasty = 'Win32_CurrentTime'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="29a6d-117">El siguiente VBScript recupera las clases secundarias inmediatas para una clase WMI.</span><span class="sxs-lookup"><span data-stu-id="29a6d-117">The following VBScript retrieves an immediate child classes for a WMI class.</span></span>


```VB
' Retrieve immediate child classes for Cim_DataFile

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _ 
    ("Select * From meta_class " _
    & "Where __Superclass = 'Cim_DataFile'")

For Each objClass In colClasses 
    WScript.Echo objClass.SystemProperties_("__Class")
Next
```



<span data-ttu-id="29a6d-118">El siguiente VBScript recupera clases de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="29a6d-118">The following VBScript retrieves top level classes.</span></span> <span data-ttu-id="29a6d-119">Para todas las clases de nivel superior de un espacio de nombres WMI, la \_ \_ propiedad sistema de la superclase es NULL.</span><span class="sxs-lookup"><span data-stu-id="29a6d-119">For all the top level classes in a WMI namespace, the \_\_Superclass system property is Null.</span></span> <span data-ttu-id="29a6d-120">Por lo tanto, es posible recuperar las clases de nivel superior buscando una superclase nula.</span><span class="sxs-lookup"><span data-stu-id="29a6d-120">Therefore, it is possible to retrieve the top level classes by searching for a Null superclass.</span></span>


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
