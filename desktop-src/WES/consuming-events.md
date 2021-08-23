---
title: Consumo de eventos (Windows de eventos)
description: Puede consumir eventos de canales o de archivos de registro.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f131f0f3b02485c3c838e9180ea1daaebb4121b8846e5a124f36cfdb6bf377f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620385"
---
# <a name="consuming-events-windows-event-log"></a>Consumo de eventos (Windows de eventos)

Puede consumir eventos de canales o de archivos de registro. Para consumir eventos, puede consumir todos los eventos o puede especificar una expresión XPath que identifique los eventos que desea consumir. Para determinar los elementos y atributos de un evento que puede usar en la expresión XPath, vea [Esquema de eventos](eventschema-schema.md).

Windows El registro de eventos admite un subconjunto de XPath 1.0. Para más información sobre las limitaciones, consulte Limitaciones de [XPath 1.0.](#xpath-10-limitations)

En los ejemplos siguientes se muestran expresiones XPath simples.


```XML
// The following query selects all events from the channel or log file
XPath Query: *

// The following query selects all the LowOnMemory events from the channel or log file
XPath Query: *[UserData/LowOnMemory]

// The following query selects all events with a severity level of 1 (Critical) from the channel or log file
XPath Query: *[System/Level=1]

// The following query shows a compound expression that selects all events from the channel or log file
// where the printer's name is MyPrinter and severity level is 1.
XPath Query: *[UserData/*/PrinterName="MyPrinter" and System/Level=1]

// The following query selects all events from the channel or log file where the severity level is
// less than or equal to 3 and the event occurred in the last 24 hour period.
XPath Query: *[System[(Level <= 3) and TimeCreated[timediff(@SystemTime) <= 86400000]]]
```



Puede usar las expresiones XPath directamente al llamar a las funciones [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) o puede usar una consulta XML estructurada que contenga la expresión XPath. Para consultas simples que consultan eventos desde un único origen, el uso de una expresión XPath es perfecto. Si la expresión XPath es una expresión compuesta que contiene más de 20 expresiones o está consultando eventos de varios orígenes, debe usar una consulta XML estructurada. Para obtener más información sobre los elementos de una consulta XML estructurada, vea [Esquema de consulta](queryschema-schema.md).

Una consulta estructurada identifica el origen de los eventos y uno o varios selectores o supresores. Un selector contiene expresiones XPath que selecciona eventos del origen y un supresor contiene una expresión XPath que impide que se seleccionen eventos. Puede seleccionar eventos de más de un origen. Si un selector y un supresor identifican el mismo evento, el evento no se incluye en el resultado.

A continuación se muestra una consulta XML estructurada que especifica un conjunto de selectores y supresores.


```XML
<QueryList>
  <Query Id="0">
    <Select Path="Application">
        *[System[(Level <= 3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
    <Suppress Path="Application">
        *[System[(Level = 2)]]
    </Suppress>
    <Select Path="System">
        *[System[(Level=1  or Level=2 or Level=3) and 
        TimeCreated[timediff(@SystemTime) <= 86400000]]]
    </Select>
  </Query>
</QueryList>
```



El conjunto de resultados de la consulta no contiene una instantánea de los eventos en el momento de la consulta. En su lugar, el conjunto de resultados incluye los eventos en el momento de la consulta y también contendrá todos los nuevos eventos que se han producido que coinciden con los criterios de consulta mientras se enumeran los resultados.

> [!Note]  
> El orden de los eventos se conserva para los eventos escritos por el mismo subproceso. Sin embargo, es posible que los eventos escritos por subprocesos independientes en distintos procesadores de un equipo con varios procesadores aparezcan fuera de servicio.

 

Para más información sobre el consumo de eventos, consulte los temas siguientes:

-   [Consulta de eventos](querying-for-events.md)
-   [Suscripción a eventos](subscribing-to-events.md)
-   [Representación de eventos](rendering-events.md)
-   [Aplicar formato a los mensajes de eventos](formatting-event-messages.md)
-   [Eventos de marcador](bookmarking-events.md)

Las herramientas estándar del usuario final para consumir eventos son:

-   [Visor de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   El Windows PowerShell [cmdlet Get-WinEvent](/previous-versions//dd367894(v=technet.10))
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitaciones de XPath 1.0

Windows El registro de eventos admite un subconjunto de XPath 1.0. La restricción principal es que solo un selector de eventos puede seleccionar los elementos XML que representan eventos. Una consulta XPath que no selecciona un evento no es válida. Todas las rutas de acceso de selector válidas \* comienzan por o "Event". Todas las rutas de acceso de ubicación funcionan en los nodos de eventos y se componen de una serie de pasos. Cada paso es una estructura de tres partes: el eje, la prueba de nodo y el predicado. Para obtener más información sobre estas partes y sobre XPath 1.0, vea [Lenguaje de rutas XML (XPath).](https://www.w3.org/TR/xpath) Windows El registro de eventos coloca las restricciones siguientes en la expresión:

-   Eje: solo se admiten los ejes Secundario (valor predeterminado) y Atributo (y su eje "@") de forma abreviada.
-   Pruebas de nodo: solo se admiten los nombres de nodo y las pruebas NCName. Se admite \* el carácter "", que selecciona cualquier carácter.
-   Predicados: cualquier expresión XPath válida es aceptable si las rutas de acceso de ubicación se ajustan a las restricciones siguientes:
    -   Se **admiten** los operadores estándar OR , **AND**, =, !=, <=, <, >=, > y paréntesis.
    -   No se admite la generación de un valor de cadena para un nombre de nodo.
    -   No se admite la evaluación en orden inverso.
    -   No se admiten conjuntos de nodos.
    -   No se admite el ámbito del espacio de nombres.
    -   No se admiten los nodos de espacio de nombres, procesamiento y comentario.
    -   No se admite el tamaño del contexto.
    -   No se admiten enlaces de variables.
    -   Se admite la función position y su referencia de matriz abreviada (solo en nodos hoja).
    -   Se admite la función Band. La función realiza una operación AND bit a bit para dos argumentos de número entero. Si el resultado de AND bit a bit es distinto de cero, la función se evalúa como true; De lo contrario, la función se evalúa como false.
    -   Se admite la función timediff. La función calcula la diferencia entre el segundo argumento y el primer argumento. Uno de los argumentos debe ser un número literal. Los argumentos deben usar la representación FILETIME. El resultado es el número de milisegundos entre las dos veces. El resultado es positivo si el segundo argumento representa una hora posterior; de lo contrario, es negativo. Cuando no se proporciona el segundo argumento, se usa la hora actual del sistema.

 

 
