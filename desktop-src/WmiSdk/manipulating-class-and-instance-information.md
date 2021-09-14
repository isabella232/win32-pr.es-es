---
description: WMI proporciona una variedad de técnicas para recuperar y manipular información de clase e instancia de WMI, mediante Microsoft PowerShell, Visual&\# 160; Basic Scripting Edition (VBScript) y C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipulación de la información de clase e instancia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967164"
---
# <a name="manipulating-class-and-instance-information"></a>Manipulación de la información de clase e instancia

WMI proporciona una variedad de técnicas para recuperar y manipular información de clase e instancia de WMI, mediante Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) y C++.

En la tabla siguiente se enumeran los temas que tratan las técnicas para recuperar y manipular información de instancias y clases WMI.



| Tema                                                                                  | Descripción                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recuperar datos de instancia o clase WMI](retrieving-class-or-instance-data.md)         | Recuperar y establecer datos desde y en el repositorio de información de WMI.                                                                                                                 |
| [Modificar una propiedad de instancia](modifying-an-instance-property.md)                   | Cambie la información de la instancia después de recuperarla.                                                                                                                     |
| [Cambiar la herencia de una instancia](changing-the-inheritance-of-an-instance.md) | Cambie la clase primaria de una instancia de .                                                                                                                                           |
| [Modificar un método](modifying-a-method.md)                                           | Modifique los parámetros de una instancia de .                                                                                                                                             |
| [Enumeración de WMI](enumerating-wmi.md)                                                 | Enumerar objetos WMI.                                                                                                                                                            |
| [Consulta de WMI](querying-wmi.md)                                                       | Consulta de objetos WMI.                                                                                                                                                                |
| [Llamar a un método](calling-a-method.md)                                               | Use métodos asociados creados por Microsoft u otros desarrolladores de terceros para manipular aún más los objetos WMI, o bien afectar directamente al objeto que representa el objeto WMI. |
| [Acceso a una colección](accessing-a-collection.md)                                   | Enumerar colecciones en el script.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Manipulación de datos mediante VBScript

Puede usar el acceso directo para tener acceso a las propiedades WMI de una clase [](accessing-a-collection.md) o instancia de WMI directamente en [**un objeto SWbemObject,**](swbemobject.md)en lugar de a través de la colección de propiedades de ese objeto. También puede ejecutar métodos en ese objeto en el estilo nativo del lenguaje de programación en lugar de usar la [**llamada SWbemServices.ExecMethod.**](swbemservices-execmethod.md) Por ejemplo, el [**método Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) del proceso [**\_ win32**](/windows/desktop/CIMWin32Prov/win32-process) tenía tres parámetros en Windows 2000, pero tiene cuatro parámetros en Windows Server 2003.

Mediante el acceso directo, puede tratar las propiedades y los métodos wmi como si fueran propiedades de automatización y métodos [**de SWbemObject**](swbemobject.md).

En el ejemplo siguiente se muestra cómo puede acceder a una propiedad .


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



En el ejemplo siguiente se muestra cómo se puede acceder a una propiedad cuando se tiene acceso directo.


```VB
VolumeName = MyDisk.VolumeName
```



El encadenamiento de objetos también es aceptable.

En el ejemplo siguiente se muestra cómo acceder a una propiedad de un objeto incrustado en otro objeto.


```VB
value = MyComputer.MyDisk.VolumeName
```



En el ejemplo siguiente se muestra cómo acceder a una propiedad con notación de subíndice de matriz.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



En el ejemplo de código de VBScript siguiente se muestra cómo generar una instancia de los parámetros de entrada para el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) en la clase Process de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) como [**SWbemObject,**](swbemobject.md)rellenar las propiedades de entrada y, a continuación, ejecutar el método **Create** mediante [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

La [**propiedad SWbemObject.Methods \_**](swbemobject-methods-.md) devuelve una colección [**SWbemMethodSet**](swbemmethodset.md) de los [**métodos Process \_ de Win32.**](/windows/desktop/CIMWin32Prov/win32-process) Los miembros del conjunto de métodos son [**objetos SWbemMethod**](swbemmethod.md) y [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) devuelve los parámetros de entrada para [**el método Create.**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) El parámetro *de entrada CommandLine* necesario se establece en "calc.exe". A continuación, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)ejecuta el método , lo que da lugar al inicio de un proceso calc.exe ejecución.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



En el ejemplo de código siguiente se muestra cómo realizar la operación anterior mediante el acceso directo.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Para obtener más información, vea [Llamar a un método de proveedor](calling-a-provider-method.md) y Scripting con [SWbemObject](scripting-with-swbemobject.md).

 

 
