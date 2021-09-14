---
description: Las consultas de datos de esquema usan la instrucción SELECT con una sintaxis similar a la de las consultas de datos.
ms.assetid: e7150aaa-5829-4d64-a13b-39f83adc5b98
ms.tgt_platform: multiple
title: Instrucción SELECT para consultas de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f9f3f9ae8cc11a94d4d868e36af56ee7dffd2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965268"
---
# <a name="select-statement-for-schema-queries"></a>Instrucción SELECT para consultas de esquema

Las consultas de datos de esquema usan la instrucción SELECT con una sintaxis similar a la de las [consultas de datos](select-statement-for-data-queries.md). La diferencia es el uso de una clase especial denominada "meta \_ class", que identifica la consulta como una consulta de esquema.

En el ejemplo siguiente se solicitan todas las definiciones de clase que están dentro del espacio de nombres actual.


```sql
SELECT * FROM meta_class
```



Las consultas de esquema solo admiten " \* ". Para restringir el ámbito de las definiciones devueltas, un proveedor puede agregar una cláusula WHERE que especifique una clase determinada.

En el ejemplo siguiente se muestra cómo agregar una cláusula WHERE para especificar una clase determinada.


```sql
SELECT * FROM meta_class WHERE __this ISA "Win32_LogicalDisk"
```



La propiedad especial denominada **\_ \_ this** identifica la clase de destino para una consulta de esquema. Tenga en cuenta que el operador ISA debe usarse con **esta \_ \_** propiedad para solicitar definiciones para las subclases de la clase de destino. La consulta anterior devuelve la definición de la [**clase \_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) y las definiciones de todas sus subclases.

En el ejemplo siguiente se muestra cómo solicitar una definición de clase para una sola clase mediante la propiedad del sistema **\_ \_ Class.**


```sql
SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"
```



Esta consulta equivale a llamar al [**método IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) con el parámetro de ruta de acceso del objeto establecido en "Win32 \_ LogicalDisk".

El siguiente ejemplo de código VBScript recupera todas las clases secundarias de una clase WMI de nivel superior. La propiedad del sistema WMI de Wmi de Wmi contiene el nombre de la clase de nivel superior de la que se deriva una clase, que puede usar para recuperar todas las clases de un espacio de nombres derivado de una clase de nivel superior, incluida esa \_ \_ clase.


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



El siguiente VBScript recupera una clase secundaria inmediata para una clase WMI.


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



El siguiente VBScript recupera clases de nivel superior. Para todas las clases de nivel superior de un espacio de nombres WMI, la \_ \_ propiedad del sistema Superclass es Null. Por lo tanto, es posible recuperar las clases de nivel superior buscando una superclase Null.


```VB
 Retrieve top level classes in root\cimv2

Set objWmi = GetObject ("winmgmts:root\cimv2")

Set colClasses = objWmi.ExecQuery _
    ("Select * From meta_class Where __Superclass Is Null")

For Each objClass In colClasses
    WScript.Echo objClass.SystemProperties_("__Class")

```



 

 
