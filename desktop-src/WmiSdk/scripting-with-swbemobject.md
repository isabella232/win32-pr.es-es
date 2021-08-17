---
description: El objeto de scripting SWbemObject es el objeto WMI genérico, que define propiedades y métodos que se pueden usar independientemente del objeto WMI específico al que está enlazado el objeto SWbemObject.
ms.assetid: 33252b49-00d4-4c43-8abe-9368ed82f34b
ms.tgt_platform: multiple
title: Scripting con SWbemObject
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d6ba0cccca8fcd62af490aa91ab1cc965fdad4d3682d99a8fda52151135500ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739701"
---
# <a name="scripting-with-swbemobject"></a>Scripting con SWbemObject

El objeto de scripting [**SWbemObject**](swbemobject.md) es el objeto WMI genérico, que define propiedades y métodos que se pueden usar independientemente del objeto WMI específico al que está enlazado el objeto **SWbemObject.** Todos los objetos WMI, como una instancia de [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) o cualquier otra clase de datos WMI, se representan mediante [**SWbemObject**](swbemobject.md) y pueden usar las propiedades y métodos comunes **de SWbemObject** además de sus propias propiedades y métodos concretos.

Por ejemplo, use el siguiente script para obtener todas las instancias de un proceso [**win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) llamando al [**método SWbemObject.Instances. \_**](swbemobject-instances-.md) clsobjProcess representa la definición de clase Process de **Win32 \_** y [**un objeto SWbemObject.**](swbemobject.md)


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set clsobjProcess = objWMIServices.Get("Win32_Process")
Set colProcesses = clsobjProcess.Instances_()
For Each Process in colProcesses
    WScript.Echo Process.Name
Next
```



En el ejemplo siguiente se obtiene una instancia específica del servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) que representa el servicio Alerter y se almacena en objAlerter. A continuación, puede llamar a métodos [**SWbemObject,**](swbemobject.md) como WScript.Echo objAlerter.Path , o a métodos definidos por la clase de datos, como \_ WScript.Echo objAlerter.State. objAlerter, que representa una instancia del servicio Win32 \_ y **un objeto SWbemObject.**


```VB
strComputer = "." 
Set objWMIServices = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set objAlerter = objWMIServices.Get("Win32_Service.Name='Alerter'")
WScript.Echo objAlerter.Path_
objAlerter.StopService()
WScript.Echo objAlerter.State
```




```VB
For each Prop in myObject.Properties_
    Wscript.Echo Prop.Name
Next
```



La llamada a [**SWbemObject.Instances \_**](swbemobject-instances-.md) obtiene otro objeto de scripting WMI genérico, [**SWbemObjectSet**](swbemobjectset.md). Como se muestra, **el objeto SWbemObjectSet** se puede tratar como una [colección](accessing-a-collection.md).


```VB
Set clsobjProcess = objWMIServices.Get("Win32_Process")
```



Puede identificar los métodos [**SWbemObject**](swbemobject.md) porque todos terminan con un carácter de subrayado ( ), por \_ ejemplo, [**SWbemObject.Instances \_**](swbemobject-instances-.md).

[**SWbemObjectEx**](swbemobjectex.md) extiende las propiedades de [**SWbemObject**](swbemobject.md). Por ejemplo, ahora puede actualizar los datos de cualquier objeto WMI, como una instancia de [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process), mediante una llamada a [**SWbemObjectEx.Refresh \_**](swbemobjectex-refresh-.md).

En el ejemplo siguiente se muestra cómo se pueden actualizar los datos de error de la página de proceso del sistema cada cinco segundos.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'System'",,48) 
For Each Process in colProcesses
        i = 0
        Do Until i = 5
            i = i + 1
            Wscript.Echo "PageFaults = " & Process.PageFaults 
            Wscript.Sleep 10000
            Process.Refresh_
        Loop
Next
```



Para obtener más información sobre cómo actualizar datos mediante [**un objeto SWbemRefresher,**](swbemrefresher.md) vea [Actualizar datos WMI en scripts](refreshing-wmi-data-in-scripts.md).

[**SWbemObject.Put \_**](swbemobject-put-.md) y [**PutAsync \_**](swbemobject-putasync-.md) permiten volver a escribir los cambios en cualquier objeto WMI. Estos métodos solo confirman cambios en un objeto en el espacio de nombres donde se creó el objeto. Puede escribir el objeto en un espacio de nombres diferente mediante [**SWbemServicesEx.Put**](swbemservicesex-put.md) o [**SWbemServicesEx.PutAsync**](swbemservicesex-putasync.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de scripting para WMI](scripting-api-for-wmi.md)
</dt> <dt>

[Crear un script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Actualización de una instancia completa](updating-an-entire-instance.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
