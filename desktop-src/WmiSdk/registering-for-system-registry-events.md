---
description: Para recibir notificaciones del proveedor del Registro del sistema, una aplicación de administración debe registrarse como consumidor de eventos temporal.
ms.assetid: 4cac5fdd-c842-4d7e-a56e-2e1312df68b4
ms.tgt_platform: multiple
title: Registro de eventos del Registro del sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c6f60b21dee729a879aaeab676da67b06ca0a822bcfd6509bc0f406f96fecec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554250"
---
# <a name="registering-for-system-registry-events"></a>Registro de eventos del Registro del sistema

Para recibir notificaciones del proveedor del [Registro del](/previous-versions/windows/desktop/regprov/system-registry-provider) sistema, una aplicación de administración debe registrarse como consumidor de eventos temporal. La mayoría de los requisitos para registrarse para el proveedor del Registro del sistema son los mismos que cualquier otro registro de eventos, excepto que también debe realizar el procedimiento siguiente.

El proveedor del Registro proporciona clases de eventos para los eventos del registro del sistema. Para obtener más información sobre el registro de eventos generales, vea [Recepción de un evento WMI](receiving-a-wmi-event.md).

En el procedimiento siguiente se describe cómo registrarse para eventos del registro del sistema.

**Para registrarse para eventos del registro del sistema**

1.  Llame a un método de consulta de notificación.

    En script o C++, use una consulta de notificación [**comoSWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) o [**IWbemServices::ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync). Cree una cadena de consulta para el *parámetro bstrQuery* de **IWbemServices::ExecNotificationQueryAsync** o *strQuery* en el script.

2.  Determine qué tipo de evento desea recibir y cree la consulta.

    En la tabla siguiente se enumeran las clases de eventos del Registro que puede usar.

    

    | Clase de evento                                                      | Ubicación de Hive        | Descripción                                                 |
    |------------------------------------------------------------------|----------------------|-------------------------------------------------------------|
    | [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent)                       | N/D<br/>       | Clase base abstracta para los cambios en el Registro.<br/> |
    | [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)   | RootPath<br/>  | Supervisa los cambios en una jerarquía de claves.<br/>         |
    | [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent)     | KeyPath<br/>   | Supervisa los cambios en una sola clave.<br/>                |
    | [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent) | ValueName<br/> | Supervisa los cambios en un solo valor.<br/>              |

    

     

    Estas clases tienen una propiedad denominada **Hive** que identifica la jerarquía de claves que se va a supervisar para el cambio, como **HKEY \_ LOCAL \_ MACHINE.**

    Los cambios en los subárboles **HKEY \_ CLASSES \_ ROOT** y **HKEY \_ CURRENT \_ USER** no son compatibles con [**RegistryEvent**](/previous-versions/windows/desktop/regprov/registryevent) ni con las clases derivadas de él, como [**RegistryTreeChangeEvent.**](/previous-versions/windows/desktop/regprov/registrytreechangeevent)

3.  Cree la cláusula WHERE para el registro de eventos.

    El proveedor del Registro del sistema tiene reglas específicas para las cláusulas WHERE. Para obtener más información, vea [Creating a Proper WHERE Clause for the Registry Provider](creating-a-proper-where-clause-for-the-registry-provider.md). Para obtener más información general sobre cómo crear una cláusula WHERE, vea [Consulta con WQL.](querying-with-wql.md)

4.  Determine si el consumidor recibe eventos.

    El proveedor del Registro del sistema no garantiza que se entreguen todos los eventos enviados. Para obtener más información, vea [Recepción de eventos del Registro.](receiving-registry-events.md)

En el ejemplo de código de VBScript siguiente se muestra cómo detectar un cambio del Registro en el subárbol o subárbol de Microsoft **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE.** \\  Se trata de un script de supervisión que, con fines de demostración, se ejecuta en un proceso denominado Wscript.exe hasta que finaliza en **Administrador de tareas**, WMI se detiene o se reinicia el sistema operativo. El script usa una [*llamada semisincronosa*](gloss-s.md) [**paraSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md). Para obtener más información sobre las llamadas semisincronosas, vea Realizar una llamada [semisincronosa con VBScript.](making-a-semisynchronous-call-with-vbscript.md)


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



En el ejemplo de código de VBScript siguiente se muestra cómo supervisar el cambio en los valores de una clave mediante el registro para el tipo de evento del proveedor del Registro [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent). El script llama a un método asincrónico, [**SWbemServices.ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md). Para obtener más información sobre las llamadas asincrónicas y la seguridad, vea [Realizar una llamada asincrónica con VBScript.](making-an-asynchronous-call-with-vbscript.md)

El siguiente script se ejecuta indefinidamente hasta que se reinicia el equipo, wmi se detiene o se detiene el script. Para detener el script manualmente, use Administrador de tareas para detener el proceso. Para detenerla mediante programación, use el [**método Terminate**](/windows/desktop/CIMWin32Prov/terminate-method-in-class-win32-process) en la clase Win32 \_ Process.


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



 

