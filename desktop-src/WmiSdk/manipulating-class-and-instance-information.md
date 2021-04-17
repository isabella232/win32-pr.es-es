---
description: WMI proporciona diversas técnicas para recuperar y manipular información de clase e instancia de WMI, mediante Microsoft PowerShell, visual&\# 160; Basic Scripting Edition (VBScript) y C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Manipular información de clase e instancia
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716865"
---
# <a name="manipulating-class-and-instance-information"></a>Manipular información de clase e instancia

WMI proporciona diversas técnicas para recuperar y manipular información de clase e instancia de WMI, mediante Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) y C++.

En la tabla siguiente se enumeran los temas en los que se describen las técnicas para recuperar y manipular información de clase e instancia de WMI.



| Tema                                                                                  | Descripción                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recuperación de datos de clase o instancia de WMI](retrieving-class-or-instance-data.md)         | Recuperar y establecer datos de y en el repositorio de información de WMI.                                                                                                                 |
| [Modificar una propiedad de instancia](modifying-an-instance-property.md)                   | Cambie la información de la instancia una vez recuperada.                                                                                                                     |
| [Cambiar la herencia de una instancia](changing-the-inheritance-of-an-instance.md) | Cambie la clase primaria de una instancia de.                                                                                                                                           |
| [Modificar un método](modifying-a-method.md)                                           | Modifique los parámetros de una instancia.                                                                                                                                             |
| [Enumerar WMI](enumerating-wmi.md)                                                 | Enumerar objetos WMI.                                                                                                                                                            |
| [Consultando WMI](querying-wmi.md)                                                       | Consultar objetos de WMI.                                                                                                                                                                |
| [Llamar a un método](calling-a-method.md)                                               | Use métodos asociados creados por Microsoft u otros desarrolladores de terceros para manipular más objetos WMI, o bien afectar directamente al objeto que representa el objeto WMI. |
| [Obtener acceso a una colección](accessing-a-collection.md)                                   | Enumerar colecciones en el script.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Manipular datos mediante VBScript

Puede usar el acceso directo para tener acceso a las propiedades de WMI de una clase o instancia de WMI directamente en un [**SWbemObject**](swbemobject.md), en lugar de a través de la [colección](accessing-a-collection.md) de propiedades de ese objeto. También puede ejecutar métodos en ese objeto en el estilo nativo del lenguaje de programación en lugar de usar la llamada [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) . Por ejemplo, el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) en [**el \_ proceso Win32**](/windows/desktop/CIMWin32Prov/win32-process) tenía tres parámetros en Windows 2000, pero tiene cuatro parámetros en Windows Server 2003.

Con el acceso directo, puede tratar las propiedades y los métodos de WMI como si fueran propiedades y métodos de automatización de [**SWbemObject**](swbemobject.md).

En el ejemplo siguiente se muestra cómo se puede tener acceso a una propiedad.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



En el ejemplo siguiente se muestra cómo puede tener acceso a una propiedad cuando tiene acceso directo.


```VB
VolumeName = MyDisk.VolumeName
```



También se admite el encadenamiento de objetos.

En el ejemplo siguiente se muestra cómo obtener acceso a una propiedad de un objeto que está incrustado en otro objeto.


```VB
value = MyComputer.MyDisk.VolumeName
```



En el ejemplo siguiente se muestra cómo obtener acceso a una propiedad con la notación de subíndice de matriz.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



En el ejemplo de código de VBScript siguiente se muestra cómo generar una instancia de los parámetros de entrada para el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) de la clase de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) como [**SWbemObject**](swbemobject.md), rellenar las propiedades de entrada y, a continuación, ejecutar el método **Create** con [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

La propiedad [**SWbemObject. \_ Methods**](swbemobject-methods-.md) devuelve una colección [**SWbemMethodSet**](swbemmethodset.md) de los métodos de [**\_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) . Los miembros del conjunto de métodos son objetos [**SWbemMethod**](swbemmethod.md) y [**SWbemMethod. Parameters**](swbemmethod-inparameters.md) devuelve los parámetros de entrada para el método [**Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . El parámetro de entrada de *línea de comandos* necesario se establece en "calc.exe". A continuación, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)ejecuta el método, lo que produce el inicio de un proceso de calc.exe.


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



Para obtener más información, consulte [llamar a un método de proveedor](calling-a-provider-method.md) y [scripting con SWbemObject](scripting-with-swbemobject.md).

 

 
