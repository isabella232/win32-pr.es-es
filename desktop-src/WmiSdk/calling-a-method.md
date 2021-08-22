---
description: WMI proporciona métodos en la API COM y la API de scripting para obtener información o manipular objetos en un sistema empresarial.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Llamar a un método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1db6c8a74c8125e0bb1727839b8f59f4b486161d5ae629a0c7351481ade016ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820119"
---
# <a name="calling-a-wmi-method"></a>Llamar a un método WMI

WMI proporciona métodos en la [API COM y](com-api-for-wmi.md) la [API de scripting](scripting-api-for-wmi.md) para obtener información o manipular objetos en un sistema empresarial. Por ejemplo, el método de scripting wmi [**SWbemServices.Execonsultas cQuery**](swbemservices-execquery.md) para los datos. Los proveedores también tienen métodos definidos en las clases que registran. Algunos ejemplos son [**los métodos \_ Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) [**Chkdsk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) y [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) proporcionados por el [proveedor de Win32.](/windows/desktop/CIMWin32Prov/win32-provider)

En este tema se de abordan las siguientes secciones:

-   [Métodos WMI en comparación con métodos de proveedor](#wmi-methods-compared-to-provider-methods)
-   [Modos de llamada a métodos en WMI](#method-calling-modes-in-wmi)
    -   [Modo sincrónico](#synchronous-mode)
    -   [Modo asincrónico](#asynchronous-mode)
    -   [Modo semisincronoso](#semisynchronous-mode)
-   [Temas relacionados](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Métodos WMI en comparación con métodos de proveedor

Mediante el uso [*de llamadas a métodos WMI*](gloss-w.md) combinadas con llamadas a [*métodos*](gloss-p.md) de proveedor, puede recuperar y manipular información sobre su empresa. Para obtener más información, vea [Llamar a un método WMI y](calling-a-wmi-method.md) Llamar a un método de [proveedor](calling-a-provider-method.md).

Los métodos del objeto de scripting wmi [**SWbemObject**](swbemobject.md) tienen un estado especial porque se pueden aplicar a cualquier clase de datos WMI. Para obtener más información, vea [Scripting con SWbemObject](scripting-with-swbemobject.md).

En el ejemplo de código siguiente se llama a WMI y a los métodos de proveedor.

Los siguientes métodos wmi y de proveedor se encuentran en [scripting API para WMI](scripting-api-for-wmi.md):

-   **objWMIService.ExecQuery llama** al método de scripting wmi [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService.StopService()** llama al método de proveedor [ **Win32 \_ Service.StopService**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Puede buscar el código que puede aparecer en "Devolución" en la sección Códigos de retorno del [**servicio Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```


```PowerShell

$colServices= Get-WmiObject -Class Win32_Service -Filter 'Name = &quot;Alerter&quot;'
foreach ($objService in $colServices)
{
    $objService.StopService()
}
```





## <a name="method-calling-modes-in-wmi"></a>Method-Calling en WMI

El modo de llamada semisincronosa normalmente proporciona el mejor equilibrio entre seguridad y rendimiento.

Para obtener más información sobre cada uno de los modos posibles, vea lo siguiente:

-   [Sincrónica](#synchronous-mode)
-   [Asincrónica](#asynchronous-mode)
-   [Semisynchronous](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Modo sincrónico

El modo sincrónico se produce cuando el programa o los scripts se detienen hasta que la llamada al método devuelve un objeto de colección [**SWbemObjectSet.**](swbemobjectset.md) WMI compila esta colección en memoria antes de devolver el objeto de colección al programa o script que realiza la llamada.

El modo sincrónico puede tener un efecto adverso del rendimiento del programa o script en el equipo que ejecuta el programa o script. Por ejemplo, recuperar sincrónicamente miles de eventos del registro de eventos puede tardar mucho tiempo y usar mucha memoria porque WMI crea un objeto a partir de cada evento y, a continuación, coloca esos objetos en una colección antes de pasar la colección al método .

Solo debe llamar a métodos que no devuelvan grandes conjuntos de datos en modo sincrónico. Los [**métodos SWbemServices siguientes**](swbemservices.md) se pueden llamar de forma segura en modo sincrónico:

-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.Get**](swbemservices-get.md)

Cualquier [**método SWbemServices**](swbemservices.md) sin la palabra "Async" en el nombre se puede llamar en modo sincrónico estableciendo el valor **wbemFlagReturnWhenComplete** en el *parámetro iFlags.*

### <a name="asynchronous-mode"></a>Modo asíncrono

El modo asincrónico se produce cuando el programa o script continúa en ejecución después de llamar al método . WMI devuelve todos los objetos del método a [**un objeto SWbemSink**](swbemsink.md) a medida que se crea cada objeto. El programa o script que realiza la llamada debe tener un objeto **SWbemSink** y un controlador de eventos [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) para procesar los objetos devueltos. Para obtener más información sobre cómo crear un controlador de eventos para el modo asincrónico, vea [Recibir un evento WMI](receiving-a-wmi-event.md).

Aunque este modo no tiene el rendimiento y la penalización de recursos del modo sincrónico, el modo asincrónico puede crear riesgos de seguridad graves porque es posible que los resultados almacenados en el objeto [**SWbemSink**](swbemsink.md) no proceden del programa o script de llamada. WMI reduce el nivel de autenticación en el **objeto SWbemSink** hasta que el método se realiza correctamente. Para obtener más información sobre cómo mitigar estos riesgos de seguridad, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

Los métodos anexados con la palabra Async son métodos para el modo asincrónico. Los métodos siguientes son llamadas asincrónicas:

-   [**SWbemServices.AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices.DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices.InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices.ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Para obtener más información sobre el modo asincrónico, vea:

-   [Realizar una llamada asincrónica con C++](making-an-asynchronous-call-with-c--.md)
-   [Realizar una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Modo semisincronoso

El modo semisincronoso es similar al modo asincrónico, ya que el programa o script continúa en ejecución después de llamar al método . En modo semisincronoso, WMI recupera los objetos en segundo plano a medida que el script o programa continúa en ejecución. WMI devuelve cada objeto devuelto al método de llamada justo después de crear el objeto.

Dado que WMI administra el objeto, el modo semisincronoso es más seguro que el modo asincrónico. Sin embargo, si usa el modo semisincronoso con más de 1000 instancias, la recuperación de instancias puede penalizar los recursos disponibles, lo que puede degradar el rendimiento del programa o script y del equipo mediante el programa o script. Cada objeto toma los recursos necesarios hasta que se libera la memoria.

Para evitar esta condición, puede llamar al método con el parámetro *iFlags* establecido con las marcas **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** para indicar a WMI que devuelva un [**SWbemObjectSet**](swbemobjectset.md)de solo avance. Un **SWbemObjectSet** de solo avance elimina el problema de rendimiento causado por un conjunto de datos grande al liberar la memoria después de enumerar el objeto.

Cualquier [**método SWbemServices**](swbemservices.md) al que no se pueda llamar en modo sincrónico o asincrónico se llama en modo semisincronoso.

Se llama a los métodos siguientes en modo semisincronoso:

-   [**SWbemServices.AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices.Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices.Get**](swbemservices-get.md)
-   [**SWbemServices.InstancesOf**](swbemservices-instancesof.md)
-   [**SWbemServices.ReferencesTo**](swbemservices-referencesto.md)
-   [**SWbemServices.SubclassesOf**](swbemservices-subclassesof.md)
-   [**SWbemServices.Put**](swbemservicesex-put.md)

Para obtener más información sobre el modo semisincrónico, vea Realizar una llamada semisincronosa con [C++](making-a-semisynchronous-call-with-c--.md) y Realizar una llamada [semisincronosa con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejora del rendimiento de enumeración](improving-enumeration-performance.md)
</dt> <dt>

[Scripting con SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
