---
description: Use SWbemServices.ExecQuery para solicitar todos los eventos existentes.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos sincrónicos y semisincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15327c66f7ba3e59824c94d54a206ec348c85952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697364"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Recibir notificaciones de eventos sincrónicos y semisincrónicos

Use [**SWbemServices.ExecQuery**](swbemservices-execquery.md) para solicitar todos los eventos existentes.

En el ejemplo de código siguiente se muestra cómo consultar los eventos en un registro.

`Select * from Win32_NTLogEvent`

Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md), [recibir notificaciones de eventos](receiving-event-notifications.md)y [WQL (SQL para WMI)](wql-sql-for-wmi.md).

La llamada predeterminada a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) utiliza la comunicación semisincrónica. El parámetro *iflags* tiene los marcadores **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** establecidos de forma predeterminada. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

En el procedimiento siguiente se describe cómo recibir una notificación de eventos semisincrónica mediante VBScript.

**Para recibir la notificación de eventos semisincrónicos en VBScript**

1.  Cree una consulta para el tipo de evento que desea recibir. Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

2.  Si solicita un tipo de instancia de evento como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indique en la consulta un tipo de instancia de destino, por ejemplo, [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Si es necesario, especifique una instancia, por ejemplo, el nombre de un espacio de nombres al solicitar futuras instancias de [**\_ \_ NamespaceModificationEvent**](--namespacemodificationevent.md) para un espacio de nombres concreto.

4.  Especifique un intervalo de sondeo para Instrumental de administración de Windows (WMI) en una consulta, como "dentro de 10", para sondear cada 10 segundos. Para obtener más información, vea [dentro de la cláusula](within-clause.md).

5.  Llame a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) con la consulta.

6.  Recorra en bucle la colección que recibe.

En el ejemplo siguiente se muestra cómo supervisar la inserción y la eliminación de discos desde una unidad de disquete en un equipo local. El script solicita \_ instancias de [**\_ \_ InstanceModificationEvent**](--instancemodificationevent.md) para la instancia de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de la unidad de disquete y sondea cada 10 segundos para las nuevas instancias. Este script es un ejemplo de consumidor de eventos temporal y continúa ejecutándose hasta que se detiene en el administrador de tareas o cuando se reinicia el sistema. Para obtener más información, consulte [recepción de eventos para la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md).


```VB
Const FLOPPY_DISK = 2
Set colMonitoredDisks = GetObject("Winmgmts:").ExecNotificationQuery _
    ("Select * from __InstanceModificationEvent within 10 WHERE " _
        & "TargetInstance ISA 'Win32_LogicalDisk'")
i = 0
Do While i = 0
    Set strDiskChange = colMonitoredDisks.NextEvent
    If strDiskChange.TargetInstance.DriveType = FLOPPY_DISK Then
        If strDiskChange.TargetInstance.Size > 0 Then
            Wscript.Echo "A disk has been inserted" & _
                " into the floppy drive."
    Else
            Wscript.Echo "A disk has been removed" & _
                " from the floppy drive."
        End If
    End If
Loop
```



En el procedimiento siguiente se describe cómo recibir una notificación de eventos semisincrónica mediante C++.

**Para recibir la notificación de eventos semisincrónicos en C++**

1.  Configure la aplicación con llamadas a las funciones [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

    Dado que WMI está basado en COM, llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) es un paso necesario para una aplicación WMI. Para obtener más información, vea [crear una aplicación o un script WMI](creating-a-wmi-application-or-script.md).

2.  Determine el tipo de eventos que desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI. Un evento extrínseco es un evento definido por un proveedor de terceros. Para obtener más información, vea [determinar el tipo de evento que se va a recibir](determining-the-type-of-event-to-receive.md).

3.  Regístrese para recibir una clase específica de eventos con una llamada al método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) .

    Haga que cada consulta sea muy específica. El objetivo del registro es registrarse para recibir solo las notificaciones necesarias. Notificaciones que no son necesarias para el procesamiento de residuos y el tiempo de entrega.

    Puede diseñar un consumidor de eventos para recibir varios eventos. Por ejemplo, un consumidor podría requerir la notificación de eventos de modificación de instancia para una clase específica de eventos de dispositivo y de infracción de seguridad. En este caso, las tareas que realiza un consumidor al recibir un evento de modificación de instancia son diferentes para los dos eventos. Por lo tanto, el consumidor debe realizar una llamada a [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) para registrar los eventos de modificación de instancias y otra llamada a **ExecNotificationQuery** para registrar los eventos de infracción de seguridad.

    En la llamada a [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), establezca el parámetro *lFlags* en **la \_ marca WBEM \_ Return \_ inmediatamente** y **WBEM \_ Flag \_ Forward \_ Only**. La **\_ marca WBEM \_ devolverá \_ inmediatamente** el procesamiento semisincrónico de las solicitudes y el marcador **WBEM \_ Flag \_ Forward \_ Only** solicita un enumerador de solo avance. Para obtener más información, consulte [llamar a un método](calling-a-method.md). La función **ExecNotificationQuery** devuelve un puntero a una interfaz [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

4.  Sondear las notificaciones de eventos registradas realizando llamadas repetidas al método [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) .
5.  Cuando termine, libere el enumerador que señala al objeto [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject) .

    Puede liberar el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) asociado al registro. Al liberar el puntero **IWbemServices** , WMI deja de entregar eventos a todos los consumidores temporales asociados.

 

 
