---
description: El lenguaje de consulta de WMI (WQL) es un subconjunto de American National Standards Institute Lenguaje de consulta estructurado estándar (ANSI SQL) con cambios semánticos menores para admitir WMI.
ms.assetid: 7e04ba37-c0e0-4304-b162-8b911f233f38
ms.tgt_platform: multiple
title: Consulta con WQL
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 737ae9505a0f775c26c5049eeb2f8500c9e3222d78181e18326ff53d39dfde01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554836"
---
# <a name="querying-with-wql"></a>Consulta con WQL

El lenguaje de consulta de WMI (WQL) es un subconjunto de American National Standards Institute Lenguaje de consulta estructurado estándar (ANSI SQL) con cambios semánticos menores para admitir WMI.

Para obtener una lista completa de las palabras clave WQL admitidas, vea [WQL (SQL para WMI).](wql-sql-for-wmi.md) El SQL palabras clave para nombres de objeto o propiedad puede impedir que se analice una consulta. Las siguientes SQL clave están restringidas: **NULL,** **TRUE** y **FALSE.**

> [!Note]  
> Hay límites en el número de palabras clave AND y OR que se pueden usar en consultas WQL. Un gran número de palabras clave WQL usadas en una consulta compleja puede hacer que WMI devuelva el código de error **WBEM \_ E QUOTA \_ \_ VIOLATION** como **un valor HRESULT.** El límite de palabras clave de WQL depende de lo compleja que sea la consulta.

 

Las consultas pueden usar la **cláusula WHERE** para la extensión y la personalización, aunque no es necesaria. La **cláusula WHERE** se forma de una propiedad o palabra clave, un operador y una constante. Todas **las cláusulas WHERE** deben especificar uno de los operadores predefinidos que se incluyen en WQL. Para obtener más información sobre la sintaxis, vea [CLÁUSULA WHERE](where-clause.md). Para obtener más información sobre los operadores WQL válidos, vea [Operadores WQL](wql-operators.md).

Al igual que con otras SQL cadenas de consulta, puede usar como escape las consultas.

> [!Note]  
> WQL no admite consultas o asociaciones entre espacios de nombres. No se pueden consultar todas las instancias de una clase especificada que resida en todos los espacios de nombres del equipo de destino.

 

WQL admite los siguientes tipos de consultas:

-   Consultas de datos

    Las consultas de datos se usan para recuperar instancias de clase y asociaciones de datos. Son el tipo de consulta que se usa con más frecuencia en scripts y aplicaciones WMI. Para obtener más información sobre la sintaxis de las consultas de datos, vea [Requesting Class Instance Data](requesting-class-instance-data.md). Para obtener más información sobre las asociaciones, vea [Declarar una clase de asociación](declaring-an-association-class.md).

    > [!Note]  
    > WQL no admite consultas de tipos de datos de matriz.

     

    En el ejemplo de consulta de datos siguiente se solicita el archivo de registro de eventos denominado "Application" de todas las instancias [**de Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent).

    ```VB
    strComputer = "." 
    Set objWMIService = GetObject("winmgmts:\\" _
        & strComputer & "\root\CIMV2") 
    Set colItems = objWMIService.ExecQuery( _
        "SELECT * FROM Win32_NTLogEvent " _
        & "WHERE Logfile = 'Application'",,48)
    ```

    

-   Consultas de eventos

    Los consumidores usan consultas de eventos para registrarse y recibir notificaciones de eventos. Los proveedores de eventos usan consultas de eventos para registrarse y admitir uno o varios eventos. Para obtener más información sobre las consultas de eventos, vea [Recepción de notificaciones de eventos.](receiving-event-notifications.md)

    La consulta de eventos de ejemplo siguiente realizada por un consumidor de eventos temporal solicita una notificación cuando se crea una nueva instancia de una clase derivada de [**Win32 \_ NTLogEvent.**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)

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

    Las consultas de esquema se usan para recuperar definiciones de clase (en lugar de instancias de clase) y asociaciones de esquema. Los proveedores de clases usan consultas de esquema para especificar las clases que admiten cuando se registran. Para obtener más información sobre las consultas de esquema, vea [Retrieving Class Definitions](retrieving-class-definitions.md).

    En la consulta de esquema de ejemplo siguiente se muestra la sintaxis especial.

    ```sql
    SELECT * FROM meta_class WHERE __this ISA "Win32_BaseService"
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de fecha y hora de WMI](date-and-time-format.md)
</dt> </dl>

 

 
