---
title: Ejemplo de tiempo de espera HTTP del escenario 1 mediante el seguimiento etw y los comandos Netsh
description: A través del seguimiento de ETW, se puede inspeccionar el flujo de datos a través del componente de API de servidor HTTP para diagnosticar problemas.
ms.assetid: b6b24161-c3da-4972-b49f-c545da2fc81e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bcb9ea328a77641e551f192b7aa89a56dd983251ade8aab45e68251a82458d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870474"
---
# <a name="scenario-1-http-timeout-example-using-etw-tracing-and-netsh-commands"></a>Escenario 1: Ejemplo de tiempo de espera http mediante el seguimiento etw y comandos Netsh

A través del seguimiento de ETW, se puede inspeccionar el flujo de datos a través del componente de API de servidor HTTP para diagnosticar problemas. Por ejemplo, los usuarios de una aplicación web pueden ver mensajes de error en su explorador que una página web no puede mostrar. En el servidor que hospeda la aplicación web, el profesional de IT también ve una entrada de tiempo de espera de conexión dentro del registro de errores HTTP, como se muestra en la figura 1 siguiente. El registro de errores HTTP se puede encontrar en el directorio siguiente: %windir% \\ System32 \\ LogFiles \\ HTTPERR \\ .

![Captura de pantalla que muestra la ventana de comandos netsh H T T P que muestra un registro de errores de H T T P para el tiempo de espera.](images/httperrorlog.png)

Figura 1: Registro de errores HTTP para el tiempo de espera

## <a name="generating-an-etw-trace-report"></a>Generación de un informe de seguimiento etw

Para generar un informe de seguimiento etw para el componente de API de servidor HTTP, ejecute los pasos siguientes desde el símbolo del sistema. En este ejemplo, el seguimiento se ejecuta en el servidor, ya que hospeda la aplicación web.

Los pasos siguientes generan un seguimiento denominado httptrace.etl y, a continuación, convierten el seguimiento en un archivo CSV denominado httptrace.csv. Como se muestra a continuación, el proveedor ETW para la API del servidor HTTP se denomina Microsoft-Windows-HttpService. La 0xFFF de línea de comandos indica que se deben capturar todos los eventos ETW para este proveedor.

**Generación de un informe de seguimiento etw**

1.  Iniciar seguimiento ETW para el componente de API de servidor HTTP: l **ogman.exe iniciar httptrace -p Microsoft-Windows-HttpService 0xFFFF -o httptrace.etl –ets**
2.  Reproduzca el problema para que se pueda capturar en el seguimiento. En este ejemplo, acceda a la aplicación web desde un equipo cliente, lo que da lugar a que la página **"** no se pueda mostrar " mensaje que se muestra en el cliente.
3.  Ahora que se ha reproducido el problema, detenga el seguimiento: **logman.exe httptrace –ets**
4.  Convertir el informe en formato CSV: **tracerpt.exe httptrace.etl -of CSV -o httptrace.csv**
5.  Vea el informe de seguimiento. A continuación se muestra un extracto de un seguimiento CSV en la tabla 1.

## <a name="viewing-the-trace-and-diagnosing"></a>Ver el seguimiento y diagnosticar

El archivo CSV resultante para seguimientos se puede ver en Excel o en cualquier herramienta que admita el formato CSV. En la tabla 1 siguiente se muestran extractos de un archivo de seguimiento de ejemplo (httptrace.csv). En el informe de seguimiento, la columna "Level" muestra una entrada con un valor de "3", que corresponde a una advertencia en ETW. El componente de API de servidor HTTP sigue los niveles de ETW definidos en el siguiente artículo: ( https://msdn2.microsoft.com/library/aa382793.aspx) . Los niveles ETW incluyen:



| Nivel | Significado      |
|-------|--------------|
| 1     | Crítico     |
| 2     | Error        |
| 3     | Advertencia      |
| 4     | Infomaional |
| 5     | Verbose      |



 

Con esta advertencia, el tipo de evento (columna Tipo) notifica "ConnTimedOut". En las columnas posteriores para el evento ConnTimeOut, el temporizador específico que expiró se notifica como \_ "Timer ConnectionIdle". Tenga en cuenta que la columna con la entrada "Timer ConnectionIdle" no se incluye en la tabla por razones de brevedad y para evitar la salida de columnas no \_ contutas.



| Nombre del evento                    | Tipo            | Id. de evento | Versión | Canal | Nivel |
|-------------------------------|-----------------|----------|---------|---------|-------|
| EventTrace                    | Header          | 0        | 2       | 0       | 0     |
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



 

Tabla 1: Extractos de un informe de seguimiento de ejemplo para un problema de temporizador

En este ejemplo, la expiración (evento ConnTimeOut) del temporizador de encabezado (Timer ConnectionIdle) es la razón por la que los usuarios finales ven el mensaje "no se puede mostrar la página" en sus clientes \_ web. Una posible razón para el tiempo de espera puede ser que los clientes web se envían lentamente debido a conexiones lentas. Para solucionar este problema, el valor de tiempo de espera se puede ajustar mediante comandos netsh.

## <a name="adjusting-timeout-through-netsh-and-verifying-the-solution"></a>Ajustar el tiempo de espera mediante Netsh y comprobar la solución

Los comandos Netsh para HTTP que se enumeran a continuación permiten a un profesional de TI ver y configurar los valores de configuración en el componente de API del servidor HTTP. Los cambios a través de comandos HTTP de Netsh afectan a todas las aplicaciones de servidor hospedadas por el componente de API de servidor HTTP para esa máquina. Estos cambios persisten entre reinicios del componente y reinicios de la máquina. Los comandos HTTP de Netsh están disponibles en Windows Vista y Windows Server 2008 y reemplazan la herramienta HttpCfg.exe del Kit de recursos de Windows Server 2003 cuando se ejecutan en Windows Vista y Windows Server 2008. En este escenario, ajustaremos un valor de tiempo de espera y comprobaremos la solución. Existen temporizadores en el componente de API de servidor HTTP para garantizar la disponibilidad y protegerse contra el consumo en exceso por parte de un usuario mal configurado o malintencionado. El ajuste de temporizadores a partir de los valores predeterminados se debe evaluar cuidadosamente frente a un posible ataque DoS.

En este ejemplo, los clientes web están detrás de una conexión de red lenta, lo que genera el evento \_ ETW Timer ConnectionIdle. Después de considerar la causa de los tiempos de espera y equilibrar con el impacto en la carga del servidor, se toma la decisión de aumentar los valores de tiempo de espera a un valor de 240 segundos. Puede ver y configurar el temporizador con el procedimiento siguiente.

**Configuración del temporizador de conexión inactiva \_ (Timer ConnectionIdle) con Netsh**

1.  En el servidor, abra una ventana de comandos con privilegios elevados y ejecute los pasos siguientes para ver y configurar el valor de tiempo de espera. En la figura 2 siguiente se muestra una captura de pantalla del comando HTTP Netsh.
2.  Mostrar los valores de tiempo de espera actuales: **Netsh http show timeout**
3.  Configure el valor de \_ Tiempo de espera de ConnectionIdle del temporizador. En este ejemplo, el valor se cambia a 240 segundos: **Netsh http add timeout timeouttype=idleconnectiontimeout value=240**

![ventana de comandos http de netsh](images/netshhttpcommand.png)

Figura 2: Ventana de comandos HTTP de Netsh

Después de configurar el valor de tiempo de espera, vuelva a ejecutar los pasos de diagnóstico de ETW. Si se corrige la condición de error, el seguimiento ETW ya no debería mostrar un tiempo de espera con un nivel ETW de "3" para el temporizador de inactividad de conexión.

 

 




