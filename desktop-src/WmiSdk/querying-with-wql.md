---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto de Lenguaje de consulta estructurado estándar de American National Standards Institute (ANSI SQL) con cambios semánticos menores para admitir WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Realizar consultas con WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8e2d3f68f4d7384781110958070b33b67a78405f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696806"
---
# <a name="querying-with-wql"></a>Realizar consultas con WQL

El lenguaje de consulta de WMI (WQL) es un subconjunto de Lenguaje de consulta estructurado estándar de American National Standards Institute (ANSI SQL) con cambios semánticos menores para admitir WMI.

Para obtener una lista completa de las palabras clave WQL admitidas, consulte [WQL (SQL para WMI)](wql-sql-for-wmi.md). El uso de palabras clave SQL para nombres de objeto o propiedad puede impedir que se analice una consulta. Las siguientes palabras clave de SQL están restringidas: **null**, **true** y **false**.

> [!Note]  
> Hay límites en el número de palabras clave AND y OR que se pueden usar en las consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error de **\_ \_ \_ infracción de la cuota de WBEM E** como un valor **HRESULT** . El límite de palabras clave de WQL depende de la complejidad de la consulta.

 

Las consultas pueden usar la cláusula **Where** para la extensión y la personalización, aunque no es necesario. La cláusula **Where** se compone de una propiedad o una palabra clave, un operador y una constante. Todas las cláusulas **Where** deben especificar uno de los operadores predefinidos que se incluyen en WQL. Para obtener más información sobre la sintaxis, vea [cláusula WHERE](where-clause.md). Para obtener más información sobre los operadores WQL válidos, vea [operadores WQL](wql-operators.md).

Como con otras cadenas de consulta de SQL, puede hacer que las consultas escapen.

> [!Note]  
> WQL no admite consultas ni asociaciones entre espacios de nombres. No se puede consultar todas las instancias de una clase especificada que residan en todos los espacios de nombres del equipo de destino.

 

WQL admite los siguientes tipos de consultas:

-   Consultas de datos

    Las consultas de datos se usan para recuperar instancias de clase y asociaciones de datos. Son el tipo de consulta que se usa con más frecuencia en scripts y aplicaciones de WMI. Para obtener más información sobre la sintaxis de las consultas de datos, vea [solicitar datos de instancia de clase](requesting-class-instance-data.md). Para obtener más información sobre las asociaciones, vea [declarar una clase de asociación](declaring-an-association-class.md).

    > [!Note]  
    > WQL no es compatible con las consultas de tipos de tipo de los tipos de tabla.

     

    El siguiente ejemplo de consulta de datos solicita el archivo de registro de eventos denominado "Application" de todas las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Consultas de eventos

    Los consumidores usan consultas de eventos para registrarse para recibir notificaciones de eventos. Los proveedores de eventos usan consultas de eventos para registrarse y admitir uno o varios eventos. Para obtener más información acerca de las consultas de eventos, consulte [recibir notificaciones de eventos](receiving-event-notifications.md).

    La siguiente consulta de eventos de ejemplo de un consumidor de eventos temporal solicita una notificación cuando se crea una nueva instancia de una clase derivada de [**\_ NTLogEvent de Win32**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) .

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set objEvents = objWMIService.ExecNotificationQuery _
    ("SELECT * FROM __InstanceModificationEvent WITHIN 10 WHERE " & _
        "TargetInstance ISA 'Win32_Service'" & _
        " AND TargetInstance._Class = 'win32_TerminalService'")

    i = TRUE
    Do While i = TRUE
        Set strReceivedEvent = objEvents.NextEvent

        'report an event
        Wscript.Echo "An event has occurred."
    Loop
    ```

    

-   Consultas de esquema

    Las consultas de esquema se utilizan para recuperar definiciones de clase (en lugar de instancias de clase) y asociaciones de esquema. Los proveedores de clases utilizan consultas de esquema para especificar las clases que admiten cuando se registran. Para obtener más información sobre las consultas de esquema, vea [recuperar definiciones de clase](retrieving-class-definitions.md).

    En la consulta de esquema de ejemplo siguiente se muestra la sintaxis especial.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de fecha y hora de WMI](date-and-time-format.md)
</dt> </dl>

 

 
