---
description: Use SWbemServices.ExecQuery para solicitar todos los eventos existentes.
ms.assetid: bc99719a-7e33-4e2d-8355-f8fc97c66f71
ms.tgt_platform: multiple
title: Recepción de notificaciones de eventos sincrónicas y semisincronosas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8657767150012124c3ccb0df8d95896f51b36ef47fa00998cf786df9beddf977
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817264"
---
# <a name="receiving-synchronous-and-semisynchronous-event-notifications"></a>Recepción de notificaciones de eventos sincrónicas y semisincronosas

Use [**SWbemServices.ExecQuery para**](swbemservices-execquery.md) solicitar todos los eventos existentes.

En el ejemplo de código siguiente se muestra cómo consultar los eventos de un registro.

`Select * from Win32_NTLogEvent`

Para obtener más información, vea [Determinar](determining-the-type-of-event-to-receive.md)el tipo de evento que se recibirá , Recibir notificaciones [de](receiving-event-notifications.md)eventos y [WQL (SQL para WMI).](wql-sql-for-wmi.md)

La llamada predeterminada a [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) usa la comunicación semisincronosa. El *parámetro iflags* tiene las marcas **wbemFlagForwardOnly** y **wbemFlagReturnImmediately** establecidas de forma predeterminada. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

En el procedimiento siguiente se describe cómo recibir notificaciones de eventos semisincronosos mediante VBScript.

**Para recibir notificaciones de eventos semisincronosos en VBScript**

1.  Cree una consulta para el tipo de evento que desea recibir. Para obtener más información, vea [Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

2.  Si solicita un tipo de instancia de evento como [**\_ \_ InstanceCreationEvent**](--instancecreationevent.md), indique en la consulta un tipo de instancia de destino, por ejemplo, [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).

3.  Si es necesario, especifique una instancia, por ejemplo, el nombre de un espacio de nombres al solicitar futuras instancias [**\_ \_ de NamespaceModificationEvent**](--namespacemodificationevent.md) para un espacio de nombres específico.

4.  Especifique un intervalo de sondeo para Windows Management Instrumentation (WMI) en una consulta, como "WITHIN 10", para sondear cada 10 segundos. Para obtener más información, vea [CLÁUSULA WITHIN](within-clause.md).

5.  Llame [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) mediante la consulta .

6.  Recorrer en bucle la colección que recibe.

En el ejemplo siguiente se muestra cómo supervisar la inserción y eliminación de discos de una unidad de disquete en una máquina local. El script solicita instancias \_ [**\_ \_ instanceModificationEvent**](--instancemodificationevent.md) para la instancia [**\_ de LogicalDisk win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de la unidad de disquete y sondea cada 10 segundos las nuevas instancias. Este script es un ejemplo de un consumidor de eventos temporal y continúa ejecutándose hasta que se detiene en Administrador de tareas o se reinicia el sistema. Para obtener más información, vea [Recepción de eventos durante la duración de la aplicación.](receiving-events-for-the-duration-of-your-application.md)


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



En el procedimiento siguiente se describe cómo recibir notificaciones de eventos semisincronosas mediante C++.

**Para recibir notificaciones de eventos semisincronosos en C++**

1.  Configure la aplicación con llamadas a las [**funciones CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

    Dado que WMI está basado en COM, llamar a [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) es un paso necesario para una aplicación WMI. Para obtener más información, vea [Crear una aplicación WMI o script](creating-a-wmi-application-or-script.md).

2.  Determine el tipo de eventos que desea recibir.

    WMI admite eventos intrínsecos y extrínsecos. Un evento intrínseco es un evento predefinido por WMI. Un evento extrínsico es un evento definido por un proveedor de terceros. Para obtener más información, vea [Determinar el tipo de evento que se recibirá.](determining-the-type-of-event-to-receive.md)

3.  Regístrese para recibir una clase específica de eventos con una llamada al método [**IWbemServices::ExecNotificationQuery.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery)

    Haga que cada consulta sea muy específica. El objetivo del registro es registrarse para recibir solo las notificaciones necesarias. Notificaciones que no son necesarias para el procesamiento de residuos y el tiempo de entrega.

    Puede diseñar un consumidor de eventos para recibir varios eventos. Por ejemplo, un consumidor podría requerir la notificación de eventos de modificación de instancia para una clase específica de eventos de infracción de seguridad y dispositivo. En este caso, las tareas que realiza un consumidor al recibir un evento de modificación de instancia son diferentes para los dos eventos. Por lo tanto, el consumidor debe realizar una llamada a [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) para registrarse para eventos de modificación de instancia y otra llamada a **ExecNotificationQuery** para registrarse para eventos de infracción de seguridad.

    En la llamada a [**ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery), establezca el parámetro *lFlags* en **WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** y **WBEM FLAG FORWARD \_ \_ \_ ONLY**. La **marca WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** solicita un procesamiento semisincronizado y la marca **WBEM FLAG FORWARD \_ \_ \_ ONLY** solicita un enumerador de solo avance. Para obtener más información, vea [Llamar a un método](calling-a-method.md). La **función ExecNotificationQuery** devuelve un puntero a una [**interfaz IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)

4.  Sondee las notificaciones de eventos registrados mediante llamadas repetidas [**al método IEnumWbemClassObject::Next.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next)
5.  Cuando termine, libere el enumerador que apunta al [**objeto IEnumWbemClassObject.**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)

    Puede liberar el [**puntero IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) asociado al registro. Al liberar el **puntero IWbemServices,** WMI deja de entregar eventos a todos los consumidores temporales asociados.

 

 
