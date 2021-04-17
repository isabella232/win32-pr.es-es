---
description: WMI proporciona métodos en la API de COM y la API de scripting para obtener información o manipular objetos en un sistema empresarial.
ms.assetid: 7a1eda93-014e-4067-b6d0-361a3d2fd1df
ms.tgt_platform: multiple
title: Llamar a un método WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c327bbf0c4c90ad05d1c5026e3308e5fd8447aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697844"
---
# <a name="calling-a-wmi-method"></a>Llamar a un método WMI

WMI proporciona métodos en la [API de com](com-api-for-wmi.md) y la [API de scripting](scripting-api-for-wmi.md) para obtener información o manipular objetos en un sistema empresarial. Por ejemplo, el método de scripting de WMI [**SWbemServices.ExecQuery**](swbemservices-execquery.md) consulta los datos. Los proveedores también tienen métodos definidos en las clases que registran. Algunos ejemplos son los métodos [**\_ lógicos Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) , [**CHKDSK**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk) y [**ScheduleAutoChk**](/windows/desktop/CIMWin32Prov/scheduleautochk-method-in-class-win32-logicaldisk) suministrados por el [proveedor de Win32](/windows/desktop/CIMWin32Prov/win32-provider).

En este tema se describen las siguientes secciones:

-   [Métodos de WMI en comparación con los métodos de proveedor](#wmi-methods-compared-to-provider-methods)
-   [Modos de llamada a métodos en WMI](#method-calling-modes-in-wmi)
    -   [Modo sincrónico](#synchronous-mode)
    -   [Modo asincrónico](#asynchronous-mode)
    -   [Modo semisincrónico](#semisynchronous-mode)
-   [Temas relacionados](#related-topics)

## <a name="wmi-methods-compared-to-provider-methods"></a>Métodos de WMI en comparación con los métodos de proveedor

Mediante el uso de llamadas a [*métodos WMI*](gloss-w.md) combinadas con llamadas a [*métodos de proveedor*](gloss-p.md) , puede recuperar y manipular información sobre su empresa. Para obtener más información, consulte [llamar a un método WMI](calling-a-wmi-method.md) y [llamar a un método de proveedor](calling-a-provider-method.md).

Los métodos del objeto de scripting de WMI [**SWbemObject**](swbemobject.md) tienen un estado especial, ya que se pueden aplicar a cualquier clase de datos de WMI. Para obtener más información, consulte [scripting con SWbemObject](scripting-with-swbemobject.md).

En el ejemplo de código siguiente se llama a los métodos de WMI y de proveedor.

Los siguientes métodos de WMI y proveedor se encuentran en la [API de scripting para WMI](scripting-api-for-wmi.md):

-   **objWMIService.ExecQuery** llama al método de scripting de WMI [ **SWbemServices.ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)
-   **objService. StopService ()** llama al método de proveedor [ **Win32 \_ Service. stopservice**](/windows/desktop/CIMWin32Prov/stopservice-method-in-class-win32-service)

Puede buscar el código que puede aparecer en "Return" en la sección códigos de retorno para [**el \_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service).


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





## <a name="method-calling-modes-in-wmi"></a>Modos de Method-Calling en WMI

Normalmente, el modo de llamada semisincrónico proporciona el mejor equilibrio entre seguridad y rendimiento.

Para obtener más información acerca de cada uno de los modos posibles, consulte lo siguiente:

-   [Sincrónica](#synchronous-mode)
-   [Asincrónica](#asynchronous-mode)
-   [Semisincrónico](#semisynchronous-mode)

### <a name="synchronous-mode"></a>Modo sincrónico

El modo sincrónico se produce cuando el programa o los scripts se pausan hasta que la llamada al método devuelve un objeto de colección [**SWbemObjectSet**](swbemobjectset.md) . WMI compila esta colección en memoria antes de devolver el objeto de colección al programa o script que realiza la llamada.

El modo sincrónico puede tener un efecto adverso en el rendimiento del programa o del script en el equipo que ejecuta el programa o el script. Por ejemplo, la recuperación sincrónica de miles de eventos del registro de eventos puede tardar mucho tiempo y usar una gran cantidad de memoria porque WMI crea un objeto a partir de cada evento y, a continuación, coloca esos objetos en una colección antes de pasar la colección al método.

Solo debe llamar a métodos que no devuelvan grandes conjuntos de datos en modo sincrónico. Se puede llamar a los siguientes métodos de [**SWbemServices**](swbemservices.md) de forma segura en modo sincrónico:

-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices. get**](swbemservices-get.md)

Se puede llamar a cualquier método de [**SWbemServices**](swbemservices.md) sin la palabra "Async" en el nombre en modo sincrónico estableciendo el valor de **wbemFlagReturnWhenComplete** en el parámetro *iFlags* .

### <a name="asynchronous-mode"></a>Modo asíncrono

El modo asincrónico se produce cuando el programa o el script continúan ejecutándose después de llamar al método. WMI devuelve todos los objetos del método a un objeto [**SWbemSink**](swbemsink.md) a medida que se crea cada objeto. El programa o script que realiza la llamada debe tener un objeto **SWbemSink** y un controlador de eventos [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) para procesar los objetos devueltos. Para obtener más información sobre cómo crear un controlador de eventos para el modo asincrónico, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

Aunque este modo no tiene la penalización de rendimiento y recursos del modo sincrónico, el modo asincrónico puede crear riesgos de seguridad graves, ya que los resultados almacenados en el objeto [**SWbemSink**](swbemsink.md) pueden no provienen del programa o script de llamada. WMI reduce el nivel de autenticación en el objeto **SWbemSink** hasta que el método se ejecuta correctamente. Para obtener más información sobre cómo mitigar estos riesgos de seguridad, consulte [configuración de la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md).

Los métodos anexados con la palabra Async son métodos para el modo asincrónico. Los métodos siguientes son llamadas asincrónicas:

-   [**SWbemServices. AssociatorsOfAsync**](swbemservices-associatorsofasync.md)
-   [**SWbemServices. DeleteAsync**](swbemservices-deleteasync.md)
-   [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
-   [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md)
-   [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md)
-   [**SWbemServices. InstancesOfAsync**](swbemservices-instancesofasync.md)
-   [**SWbemServices. ReferencesToAsync**](swbemservices-referencesto.md)
-   [**SWbemServices. SubclassesOfAsync**](swbemservices-subclassesofasync.md)

Para obtener más información sobre el modo asincrónico, vea:

-   [Realización de una llamada asincrónica con C++](making-an-asynchronous-call-with-c--.md)
-   [Realización de una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md)

### <a name="semisynchronous-mode"></a>Modo semisincrónico

El modo semisincrónico es similar al modo asincrónico en que el programa o script continúa ejecutándose después de llamar al método. En el modo semisincrónico, WMI recupera los objetos en segundo plano a medida que el script o programa continúa ejecutándose. WMI devuelve cada objeto devuelto al método de llamada justo después de que se cree el objeto.

Dado que WMI administra el objeto, el modo semisincrónico es más seguro que el modo asincrónico. Sin embargo, si utiliza el modo semisincrónico con más de 1.000 instancias, la recuperación de instancias puede monopolizar los recursos disponibles, lo que puede degradar el rendimiento del programa o el script y el equipo que usa el programa o el script. Cada objeto ocupa los recursos necesarios hasta que se libera la memoria.

Para solucionar esta situación, puede llamar al método con el parámetro *iFlags* establecido con las marcas **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** para indicar a WMI que devuelva un [**SWbemObjectSet**](swbemobjectset.md)de solo avance. Un **SWbemObjectSet** de solo avance elimina el problema de rendimiento causado por un conjunto de datos grande liberando la memoria después de que se haya enumerado el objeto.

Cualquier método [**SWbemServices**](swbemservices.md) al que no se pueda llamar en modo sincrónico o asincrónico se llama en modo semisincrónico.

Se llama a los métodos siguientes en modo semisincrónico:

-   [**SWbemServices. AssociatorsOf**](swbemservices-associatorsof.md)
-   [**SWbemServices. Delete**](swbemservices-delete.md)
-   [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
-   [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)
-   [**SWbemServices.ExecQuery**](swbemservices-execquery.md)
-   [**SWbemServices. get**](swbemservices-get.md)
-   [**SWbemServices. instances**](swbemservices-instancesof.md)
-   [**SWbemServices. References**](swbemservices-referencesto.md)
-   [**SWbemServices. subclasses**](swbemservices-subclassesof.md)
-   [**SWbemServices. put**](swbemservicesex-put.md)

Para obtener más información sobre el modo semisincrónico, vea [crear una llamada semisincrónica con C++](making-a-semisynchronous-call-with-c--.md) y [crear una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mejorar el rendimiento de la enumeración](improving-enumeration-performance.md)
</dt> <dt>

[Scripting con SWbemObject](scripting-with-swbemobject.md)
</dt> <dt>

[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> </dl>

 

 
