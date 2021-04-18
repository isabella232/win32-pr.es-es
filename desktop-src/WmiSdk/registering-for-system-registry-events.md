---
description: Para recibir notificaciones del proveedor del registro del sistema, una aplicación de administración debe registrarse como consumidor de eventos temporal.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registrar eventos del registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 886046f5ffef366cdba2efb86629019f2ee0b5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707276"
---
# <a name="registering-for-system-registry-events"></a>Registrar eventos del registro del sistema

Para recibir notificaciones del proveedor [del registro del sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) , una aplicación de administración debe registrarse como consumidor de eventos temporal. La mayoría de los requisitos para registrarse en el proveedor del registro del sistema son los mismos que cualquier otro registro de eventos, salvo que también debe realizar el procedimiento siguiente.

El proveedor del registro proporciona clases de eventos para los eventos en el registro del sistema. Para obtener más información sobre el registro de eventos generales, consulte [recibir un evento WMI](receiving-a-wmi-event.md).

En el procedimiento siguiente se describe cómo registrar eventos del registro del sistema.

**Para registrar eventos del registro del sistema**

1.  Llamar a un método de consulta de notificación.

    En script o C++, use una consulta de notificación como [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Cree una cadena de consulta para el parámetro *bstrQuery* de **IWbemServices:: ExecNotificationQueryAsync** o *strQuery* en el script.

2.  Determine el tipo de evento que desea recibir y cree la consulta.

    En la tabla siguiente se enumeran las clases de eventos del registro que se pueden usar.

    

    | Clase de evento                                                      | Ubicación de Hive        | Descripción                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/D<br/>       | Clase base abstracta para los cambios en el registro.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Supervisa los cambios en una jerarquía de claves.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | Rutas<br/>   | Supervisa los cambios en una sola clave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Supervisa los cambios en un único valor.<br/>              |

    

     

    Estas clases tienen una propiedad denominada **Hive** que identifica la jerarquía de claves que se va a supervisar para el cambio, como **HKEY \_ local \_ Machine**.

    Los cambios en **las \_ clases HKEY \_ root** y **HKEY del \_ \_ usuario actual** no son compatibles con [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ni con las clases derivadas de él, como [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent).

3.  Cree la cláusula WHERE para el registro de eventos.

    El proveedor del registro del sistema tiene reglas específicas para las cláusulas WHERE. Para obtener más información, vea [crear una cláusula WHERE adecuada para el proveedor del registro](creating-a-proper-where-clause-for-the-registry-provider.md). Para obtener más información general sobre la creación de una cláusula WHERE, vea [consultas con WQL](querying-with-wql.md).

4.  Determine si el consumidor está recibiendo eventos.

    El proveedor del registro del sistema no garantiza que se entreguen todos los eventos enviados. Para obtener más información, consulte [recibir eventos del registro](receiving-registry-events.md).

En el ejemplo de código de VBScript siguiente se muestra cómo detectar un cambio en el registro en el software del **\_ \_ equipo local HKEY** \\  \\ **Microsoft** Hive o subárbol. Se trata de un script de supervisión que, para fines de demostración, se ejecuta en un proceso denominado Wscript.exe hasta que se termina en el **Administrador de tareas**, se detiene WMI o se reinicia el sistema operativo. El script usa una llamada [*semisincrónica*](gloss-s.md) a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Para obtener más información sobre las llamadas semisincrónicas, vea [realizar una llamada semisincrónica con VBScript](making-a-semisynchronous-call-with-vbscript.md).


```VB
Set wmiServices = GetObject("winmgmts:root/default") 
Set colTreeChanges = wmiServices.ExecNotificationQuery _
    ("SELECT * FROM RegistryTreeChangeEvent " _
    & "WHERE Hive='HKEY_LOCAL_MACHINE' " _
    & "AND RootPath='SOFTWARE\\Microsoft'")

While (True)
   Set TreeChange = colTreeChanges.NextEvent
   TreeChange.GetObjectText_()
   Wscript.Echo  "Hive = " & TreeChange.Hive & VBNewLine _
      & "RootPath = "& TreeChange.RootPath _
      & TreeChange.GetObjectText_()      
Wend
```



En el ejemplo de código de VBScript siguiente se muestra cómo supervisar el cambio en los valores de una clave registrando el tipo de evento [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)del proveedor del registro. El script llama a un método asincrónico, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obtener más información sobre las llamadas asincrónicas y la seguridad, vea [realizar una llamada asincrónica con VBScript](making-an-asynchronous-call-with-vbscript.md).

El script siguiente se ejecuta indefinidamente hasta que se reinicia el equipo, se detiene WMI o se detiene el script. Para detener el script manualmente, use el administrador de tareas para detener el proceso. Para detenerlo mediante programación, use el método [**Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase de proceso de Win32 \_ .


```VB
strComputer = "."
Set objWMIServices = GetObject("winmgmts:root/default") 
Set wmiSink = WScript.CreateObject( _
    "WbemScripting.SWbemSink", "SINK_") 
Set ObjRegistry = GetObject("winmgmts:_
    {impersonationLevel = impersonate}!\\" _
    & strComputer & "\root\default:StdRegProv")

' Create a new key
strPath = "SOFTWARE\MyKey\MySubKey\"
Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

' Start listening for change in key
objWMIServices.ExecNotificationQueryAsync wmiSink, _ 
    "SELECT * FROM RegistryKeyChangeEvent " _ 
    & "WHERE Hive='HKEY_LOCAL_MACHINE' AND " _ 
    & "KeyPath='SOFTWARE\\MyKey\\MySubKey\\'" 
WScript.Echo "Listening for Registry Change Events..." 

While(True) 
    WScript.Sleep 1000
' You can use Regedit to make a change in the key 
' HKEY_LOCAL_MACHINE\SOFTWARE\MyKey\MySubKey\ 
'    to see an event generated.
Wend 

Sub SINK_OnObjectReady(EventObject, wmiAsyncContext) 
    WScript.Echo "Received Registry Change Event" & vbCrLf & _
      EventObject.GetObjectText_() 
End Sub
```



 

