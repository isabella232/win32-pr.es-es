---
title: Escenario 1 ejemplo de tiempo de espera HTTP con seguimiento ETW y comandos Netsh
description: A través del seguimiento de ETW, el flujo de datos a través del componente API del servidor HTTP se puede inspeccionar para diagnosticar problemas.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa50f438aca664651b24db822f2b9e3a30da4682
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104556078"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Escenario 1: ejemplo de tiempo de espera de HTTP usando seguimiento ETW y comandos Netsh

A través del seguimiento de ETW, el flujo de datos a través del componente API del servidor HTTP se puede inspeccionar para diagnosticar problemas. Por ejemplo, los usuarios de una aplicación Web pueden ver mensajes de error en su explorador que no se pueden mostrar en una página web. En el servidor que hospeda la aplicación Web, el profesional de ti también ve una entrada de tiempo de espera de conexión en el registro de errores HTTP, como se muestra en la figura 1. El registro de errores HTTP se puede encontrar en el directorio siguiente:% WINDIR% \\ system32 \\ logfiles \\ HTTPERR \\ .

![Captura de pantalla que muestra la ventana de comandos Netsh H T T P mostrando un registro de errores H T t P para el tiempo de espera.](images/httperrorlog.png)

Figura 1: registro de errores de HTTP para el tiempo de espera

## <a name="generating-an-etw-trace-report"></a>Generar un informe de seguimiento de ETW

Para generar un informe de seguimiento de ETW para el componente de API del servidor HTTP, ejecute los pasos siguientes desde el símbolo del sistema. En este ejemplo, el seguimiento se ejecuta en el servidor desde que hospeda la aplicación Web.

En los pasos siguientes se genera un seguimiento denominado httptrace. ETL y, a continuación, se convierte el seguimiento en un archivo CSV denominado httptrace.csv. Como se muestra a continuación, el proveedor ETW de la API del servidor HTTP se denomina Microsoft-Windows-HttpService. La opción de línea de comandos 0xFFF indica que se deben capturar todos los eventos ETW para este proveedor.

**Generar un informe de seguimiento de ETW**

1.  Iniciar seguimiento de ETW para el componente de API de servidor HTTP: l **ogman.exe Start httptrace-p Microsoft-Windows-HTTPService 0xFFFF-o httptrace. ETL – ETS**
2.  Reproduzca el problema para que se pueda capturar en el seguimiento. En este ejemplo, se tiene acceso a la aplicación web desde un equipo cliente, lo que da lugar a que se muestre el mensaje "**no se puede mostrar la página**" en el cliente.
3.  Ahora que se ha reproducido el problema, detenga el seguimiento: **logman.exe STOP httptrace – ETS**
4.  Convierta el informe en formato CSV: **tracerpt.exe httptrace. ETL-de CSV-o httptrace.csv**
5.  Ver el informe de seguimiento. A continuación se muestra un extracto de un seguimiento de CSV en la tabla 1.

## <a name="viewing-the-trace-and-diagnosing"></a>Ver el seguimiento y el diagnóstico

El archivo CSV resultante para seguimientos se puede ver en Excel o en cualquier herramienta que admita el formato CSV. En la tabla 1 siguiente se muestran fragmentos de un archivo de seguimiento de ejemplo (httptrace.csv). En el informe de seguimiento, la columna "nivel" muestra una entrada con un valor de "3", que corresponde a una advertencia en ETW. El componente API del servidor HTTP sigue los niveles de ETW definidos en el artículo siguiente: ( https://msdn2.microsoft.com/library/aa382793.aspx) . Los niveles de ETW incluyen:



| Nivel | Significado      |
|-------|--------------|
| 1     | Crítico     |
| 2     | Error        |
| 3     | Advertencia      |
| 4     | Infomational |
| 5     | Verbose      |



 

Con esta advertencia, el tipo de evento (columna de tipo) notifica "ConnTimedOut". En las columnas subsiguientes del evento ConnTimeOut, el temporizador específico que expiró se muestra como "TIMER \_ ConnectionIdle". Tenga en cuenta que la columna con la entrada "TIMER \_ ConnectionIdle" no se incluye en la tabla por razones de brevedad y para evitar el extracto de columnas no contiguas.



| Nombre del evento                    | Tipo            | Id. de evento | Versión | Canal | Nivel |
|-------------------------------|-----------------|----------|---------|---------|-------|
| Eventtracer                    | Encabezado          | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | AddUrl          | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgReqQueueProp | 30       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgUrlGrpProp   | 28       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ChgSrvSesProp   | 29       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect     | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn     | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq         | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | Analizar           | 2        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | LogFileWrite    | 51       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnCleanup     | 24       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnTimedOut    | 53       | 0       | 16      | 3     |



 

Tabla 1: extractos de un informe de seguimiento de ejemplo para un problema de temporizador

En este ejemplo, la expiración (evento ConnTimeOut) del temporizador de encabezado (temporizador \_ ConnectionIdle) es el motivo por el que los usuarios finales ven el mensaje "no se puede mostrar la página" en sus clientes Web. Una posible razón para el tiempo de espera puede ser que los clientes web envíen lentamente debido a conexiones lentas. Para solucionar este problema, el valor de tiempo de espera se puede ajustar a través de los comandos Netsh.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Ajuste del tiempo de espera a través de Netsh y comprobación de la solución

Los comandos Netsh para HTTP que se enumeran a continuación permiten a los profesionales de ti ver y configurar los valores de configuración en el componente API del servidor HTTP. Los cambios a través de los comandos Netsh HTTP afectan a todas las aplicaciones de servidor hospedadas por el componente de API de servidor HTTP para ese equipo. Estos cambios se conservan a lo largo del reinicio del componente y se reinician de la máquina. Los comandos Netsh HTTP están disponibles en Windows Vista y Windows Server 2008 y reemplazan la herramienta HttpCfg.exe del kit de recursos de Windows Server 2003 cuando se ejecutan en Windows Vista y Windows Server 2008. En este escenario, se ajustará un valor de tiempo de espera y se comprobará la solución. Existen temporizadores en el componente API del servidor HTTP para garantizar la disponibilidad y protegerse frente al uso excesivo por parte de un usuario malintencionado o mal configurado. El ajuste de los temporizadores a partir de los valores predeterminados debe evaluarse detenidamente frente a posibles ataques de DoS.

En este ejemplo, los clientes web están detrás de una conexión de red lenta, lo que produce el \_ evento ETW ConnectionIdle de Timer. Después de considerar la causa de los tiempos de espera y el equilibrio con el impacto en la carga del servidor, se toma la decisión de aumentar los valores de tiempo de espera a un valor de 240 segundos. Puede ver y configurar el temporizador con el siguiente procedimiento.

**Configurar el temporizador de conexión inactiva (temporizador \_ ConnectionIdle) con netsh**

1.  En el servidor, abra una ventana de comandos con privilegios elevados y ejecute los pasos siguientes para ver y configurar el valor de tiempo de espera. En la figura 2 se muestra una captura de pantalla del comando netsh HTTP.
2.  Mostrar los valores de tiempo de espera actuales: **netsh http show timeout**
3.  Configure el \_ valor de tiempo de espera del temporizador ConnectionIdle. En este ejemplo, el valor se cambia a 240 segundos: **netsh http Add timeout timeouttype = idleconnectiontimeout, Value = 240**

![netsh http (ventana de comandos)](images/netshhttpcommand.png)

Figura 2: ventana de comandos Netsh HTTP

Después de configurar el valor de tiempo de espera, vuelva a ejecutar los pasos de diagnóstico de ETW. Si la condición de error se corrige, el seguimiento de ETW ya no debe mostrar un tiempo de espera con un nivel ETW de "3" para el temporizador de inactividad de la conexión.

 

 




