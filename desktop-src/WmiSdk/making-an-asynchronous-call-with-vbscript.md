---
description: Realizar una llamada asincrónica a un método WMI o a un método de proveedor permite que un script continúe ejecutándose mientras los objetos vuelven a un objeto SWbemSink y se controlan mediante métodos como SWbemSink.OnObjectReady.
ms.assetid: 61f401d9-c874-472d-8dd3-7cf9d7f20a12
ms.tgt_platform: multiple
title: Realizar una llamada asincrónica con VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee8c4737ff7513441532275e24f2cfe20f8e30fa2932e854cc566eb032c49d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555154"
---
# <a name="making-an-asynchronous-call-with-vbscript"></a>Realizar una llamada asincrónica con VBScript

Realizar una llamada asincrónica a un método [*WMI*](gloss-w.md) o [*a*](gloss-p.md) un método de proveedor permite que un script continúe ejecutándose mientras los objetos vuelven a un objeto [**SWbemSink**](swbemsink.md) y se controlan mediante métodos como [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md). Sin embargo, no se recomiendan las llamadas asincrónicas porque es posible que los datos no se devuelvan en el mismo nivel de seguridad que se realiza la llamada.

Al usar llamadas de receptor asincrónicas como [**SWbemSink.OnObjectReady para**](swbemsink-onobjectready.md) obtener datos devueltos, puede establecer el siguiente valor del Registro.

**HKEY \_ SOFTWARE \_ DE MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault**

Establecer este valor del Registro garantiza la autenticación de los objetos de datos devueltos al receptor. Si **UnsecAppAccessControlDefault** se establece en uno (1), WMI realiza la comprobación de acceso de la devolución de datos. Las comprobaciones de acceso comprueban que los datos proceden del origen correcto. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md)

Los métodos asincrónicos con nombres que terminan en "Async" siempre devuelven inmediatamente después de llamarse para \_ que un programa pueda continuar ejecutándose. Por ejemplo, [**SWbemServices.ExecQuery es sincrónico**](swbemservices-execquery.md) y bloquea la ejecución hasta que se devuelven todos los objetos. El [**SWbemServices.Exemétodo cQueryAsync**](swbemservices-execqueryasync.md) es la versión asincrónica sin bloqueo. Una manera más segura de realizar la llamadaSWbemServices.Exeel bloqueo **de cQuery** es realizar la llamada de forma [*semisincronosa.*](gloss-s.md) Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md) y Realizar una llamada [semisincronosa con VBScript.](making-a-semisynchronous-call-with-vbscript.md)

El *parámetro iFlags* para las llamadas asincrónicas siempre tiene como valor predeterminado cero (0). Los métodos asincrónicos no suministran [**una colección SWbemObjectSet**](swbemobjectset.md) a la subrutina receptora. En su lugar, la subrutina de eventos [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) en el script o la aplicación recibe cada objeto tal como se proporciona.

Una vez completada la llamada asincrónica original, llama al evento [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) del receptor del objeto y ejecuta el código que se coloca allí para procesar el resultado de la llamada.

> [!Note]  
> Una Active Server page (ASP) como host de script no admite una llamada asincrónica.

 

En el procedimiento siguiente se describe cómo realizar una llamada asincrónica mediante VBScript.

**Para realizar una llamada asincrónica mediante VBScript**

1.  Conectar a WMI y obtener un [**objeto SWbemServices.**](swbemservices.md)

    ```VB
    Set Service = GetObject("Winmgmts:")
    ```

    

2.  Cree el receptor de objetos mediante [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) o (solo para Windows Script Host 2.0) la etiqueta OBJECT con un atributo events establecido en **TRUE.**

    ```VB
    Set sink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")
    ```

    

    O bien

    ```VB
    <OBJECT progid="WbemScripting.SWbemSink" ID="SINK" events="true"/>
    ```

    

3.  Cree una subrutina para cada evento que un evento asincrónico pueda desencadenar. Estos eventos se definen como métodos en [**SWbemObject**](swbemobject.md). Por ejemplo, WMI realiza una devolución de llamada a [**SWbemSink.OnObjectReady a**](swbemsink-onobjectready.md) medida que se devuelve cada instancia.

    Cuando cree la subrutina, coloque el código en la subrutina para controlar cada evento cuando se reciba.

    ```VB
    Sub SINK_OnCompleted(
          iHResult, 
          objErrorObject, 
          objAsyncContext
          )
        WScript.Echo "Asynchronous operation is done."
    End Sub

    Sub SINK_OnObjectReady(objObject, objAsyncContext)
        WScript.Echo (objObject.Name)
    End Sub
    ```

    

    Examine el *parámetro iHresult* devuelto por el evento [**OnCompleted**](swbemsink-oncompleted.md) para determinar si la llamada asincrónica es correcta o no, o si se produjo un error. Si se realiza correctamente, el valor pasado en el *parámetro iHresult* es igual a cero (0). Cualquier otro valor puede indicar un error y debe comprobar los valores del objeto de error que se devuelve en el *parámetro objErrorObject.*

4.  Realice una llamada asincrónica y pase el nombre del receptor en el *parámetro objWbemSink.*

    ```VB
    Service.InstancesOfAsync sink, "Win32_process"
    ```

    

5.  Realice una llamada que impida que el script termine antes de que se reciban todos los eventos. Si el script se puede ejecutar con una interfaz de pantalla, una manera sencilla de hacerlo es usar un comando Windows Script Host (WSH), que se muestra en el `Echo` ejemplo siguiente.

    ```VB
    WScript.Echo "Waiting for instances."
    ```

    

    Al ejecutar este script, es posible que vea que la primera instancia vuelve antes del mensaje **Waiting for instances** (Esperando instancias) o puede verlo después. Esta es la naturaleza del procesamiento asincrónico. Si cierra el cuadro **de mensaje Esperando instancias** demasiado pronto, es posible que no vea todas las instancias.

6.  Si tiene resultados de varias llamadas asincrónicas diferentes que vuelven al mismo receptor, almacene los datos distintivos necesarios en el parámetro de contexto *objWbemAsyncContext.*

7.  Cuando termine con el receptor, cancele la llamada asincrónica con el [**método Cancel.**](swbemsink-cancel.md)

    ```VB
    objwbemsink.Cancel()
    ```

    

    El [**método Cancel**](swbemsink-cancel.md) indica a WSH que cancele todas las llamadas asincrónicas asociadas a un objeto receptor determinado. Por lo tanto, puede que desee usar receptores independientes para las operaciones asincrónicas que deben ser independientes.

8.  Libere el objeto receptor asignando el objeto receptor a `Nothing` .

    ```VB
    set objwbemsink= Nothing
    ```

    

En el ejemplo de código siguiente se muestra una consulta asincrónica para todas las instancias de [**Proceso de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) en el equipo local. Para obtener una versión semisincronosa del mismo método, vea [Llamar a un método](calling-a-method.md).


```VB
' Create an object sink
set oSink = WScript.CreateObject("wbemscripting.swbemsink","sink_")
' Connect to WMI and the cimv2 namespace, and obtain
' an SWbemServices object
set oSvc = GetObject("winmgmts:root\cimv2")

bdone = false
' Query for all Win32_Process objects
osvc.ExecQueryAsync oSink, "SELECT Name FROM Win32_Process"
' Wait until all instances are returned. 
' The bdone flag prevents the script from exiting until
' the sink.OnCompleted subroutine is executed when
' all the objects are returned.
while not bdone    
    wscript.sleep 1000
wend

' The sink subroutine to handle the OnObjectReady 
' event. This is called as each object returns.
sub sink_OnObjectReady(oInst, octx)
    WScript.Echo "Got Instance: " & oInst.Name
end sub
' The sink subroutine to handle the OnCompleted event.
' This is called when all the objects are returned. 
' The oErr parameter obtains an SWbemLastError object,
' if available from the provider.
sub sink_OnCompleted(HResult, oErr, oCtx)
    WScript.Echo "ExecQueryAsync completed"
    bdone = true
end sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

 
