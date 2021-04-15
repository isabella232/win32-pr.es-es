---
title: Consumir eventos (registro de eventos de Windows)
description: Puede consumir eventos de los canales o de los archivos de registro.
ms.assetid: 17204d3f-0875-42c5-9af4-caca6349a67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb3fb1b36a0cd4ecf836a8893bc1abc14e46451
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695832"
---
# <a name="consuming-events-windows-event-log"></a>Consumir eventos (registro de eventos de Windows)

Puede consumir eventos de los canales o de los archivos de registro. Para consumir eventos, puede consumir todos los eventos o especificar una expresión XPath que identifique los eventos que desea consumir. Para determinar los elementos y atributos de un evento que puede utilizar en la expresión XPath, vea [esquema de eventos](eventschema-schema.md).

El registro de eventos de Windows admite un subconjunto de XPath 1,0. Para obtener más información sobre las limitaciones, consulte [restricciones de XPath 1,0](#xpath-10-limitations).

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



Puede utilizar directamente las expresiones XPath al llamar a las funciones [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) , o puede usar una consulta XML estructurada que contenga la expresión XPath. En el caso de consultas simples que consultan eventos de un solo origen, el uso de una expresión XPath es correcto. Si la expresión XPath es una expresión compuesta que contiene más de 20 expresiones o está consultando eventos de varios orígenes, debe utilizar una consulta XML estructurada. Para obtener más información sobre los elementos de una consulta XML estructurada, vea [esquema de consulta](queryschema-schema.md).

Una consulta estructurada identifica el origen de los eventos y uno o más selectores o suprimidores. Un selector contiene una expresión XPath que selecciona los eventos del origen y un supresor contiene una expresión XPath que impide que se seleccionen los eventos. Puede seleccionar eventos de más de un origen. Si un selector e supresor identifican el mismo evento, el evento no se incluye en el resultado.

A continuación se muestra una consulta XML estructurada que especifica un conjunto de selectores y suprimidores.


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



El conjunto de resultados de la consulta no contiene una instantánea de los eventos en el momento de la consulta. En su lugar, el conjunto de resultados incluye los eventos en el momento de la consulta y también contendrá todos los eventos nuevos que se generan que coinciden con los criterios de consulta mientras se enumeran los resultados.

> [!Note]  
> El orden de los eventos se conserva para los eventos que se escriben en el mismo subproceso. Sin embargo, es posible que los eventos escritos por subprocesos independientes en diferentes procesadores de un equipo con varios procesadores parezcan desordenados.

 

Para obtener información detallada sobre el consumo de eventos, vea los temas siguientes:

-   [Consultar eventos](querying-for-events.md)
-   [Suscripción a eventos](subscribing-to-events.md)
-   [Representar eventos](rendering-events.md)
-   [Dar formato a mensajes de eventos](formatting-event-messages.md)
-   [Marcar eventos](bookmarking-events.md)

Las herramientas estándar de usuario final para el evento de consumo son:

-   [Visor de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))
-   El cmdlet [Get-WinEvent](/previous-versions//dd367894(v=technet.10)) de Windows PowerShell
-   [**WevtUtil**](windows-event-log-tools.md)

## <a name="xpath-10-limitations"></a>Limitaciones de XPath 1,0

El registro de eventos de Windows admite un subconjunto de XPath 1,0. La restricción principal es que solo los elementos XML que representan eventos se pueden seleccionar mediante un selector de eventos. Una consulta XPath que no selecciona un evento no es válida. Todas las rutas de acceso de selector válidas empiezan por \* o "Event". Todas las rutas de acceso de ubicación operan en los nodos de eventos y se componen de una serie de pasos. Cada paso es una estructura de tres partes: el eje, la prueba de nodo y el predicado. Para obtener más información acerca de estas partes y sobre XPath 1,0, consulte [lenguaje de rutas XML (XPath)](https://www.w3.org/TR/xpath). El registro de eventos de Windows impone las siguientes restricciones en la expresión:

-   AXIS: solo se admiten los valores secundarios (default) y Attribute (y su eje abreviado "@").
-   Pruebas de nodo: solo se admiten nombres de nodo y pruebas de NCName. \*Se admite el carácter "", que selecciona cualquier carácter.
-   Predicados: cualquier expresión XPath válida es aceptable si las rutas de acceso de ubicación cumplen las restricciones siguientes:
    -   Se admiten los operadores estándar **o**, **y**, =,! =, <=, <, >=, > y paréntesis.
    -   No se admite la generación de un valor de cadena para un nombre de nodo.
    -   No se admite la evaluación en orden inverso.
    -   No se admiten conjuntos de nodos.
    -   No se admite el ámbito de espacio de nombres.
    -   No se admiten los nodos de espacio de nombres, procesamiento y comentario.
    -   No se admite el tamaño del contexto.
    -   No se admiten los enlaces de variables.
    -   Se admite la función Position y su referencia de matriz abreviada (solo en los nodos hoja).
    -   Se admite la función de banda. La función realiza una operación and bit a bit para dos argumentos de número entero. Si el resultado de la operación and bit a bit es distinto de cero, la función se evalúa como true; de lo contrario, la función se evalúa como false.
    -   Se admite la función timediff. La función calcula la diferencia entre el segundo argumento y el primer argumento. Uno de los argumentos debe ser un número literal. Los argumentos deben usar la representación de FILETIME. El resultado es el número de milisegundos entre las dos horas. El resultado es positivo si el segundo argumento representa una hora posterior; de lo contrario, es negativo. Cuando no se proporciona el segundo argumento, se usa la hora actual del sistema.

 

 
