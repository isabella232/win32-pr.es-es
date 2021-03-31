---
title: Usar Netsh para administrar seguimientos
description: En Windows 7, se puede usar netsh.exe desde un símbolo del sistema para habilitar y configurar los seguimientos de red. En esta sección se describen algunos de los comandos de netsh.exe que pueden ayudar en la solución de problemas de seguimiento, incluida la nueva funcionalidad de seguimiento de Netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1978345da984ac90699b5355b36af18b9b285d5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418771"
---
# <a name="using-netsh-to-manage-traces"></a>Usar Netsh para administrar seguimientos

En Windows 7, se puede usar netsh.exe desde un símbolo del sistema para habilitar y configurar los seguimientos de red. En esta sección se describen algunos de los comandos de netsh.exe que pueden ayudar en la solución de problemas de seguimiento, incluida la nueva funcionalidad de **seguimiento de Netsh** . Tenga en cuenta que los comandos Netsh deben ejecutarse desde un símbolo del sistema con privilegios elevados.

## <a name="collecting-traces"></a>Recopilar seguimientos

Los escenarios son conjuntos predefinidos de proveedores de seguimiento que se pueden habilitar para solucionar problemas. Para ver la lista de escenarios relacionados con la red disponibles, escriba **netsh Trace show Scenarios** (**netsh Trace show Providers** lists cada uno de los proveedores disponibles, incluidos los que no son relevantes para las redes).

Cuando haya identificado un escenario que tenga un aspecto relevante para los problemas, puede ver una lista de todos los proveedores incluidos en ese escenario. Por ejemplo, para ver todos los proveedores habilitados en el escenario InternetClient, escriba **netsh Trace show Scenario InternetClient**.

Puede iniciar un seguimiento para todos los proveedores en un escenario o un conjunto de escenarios determinados. Por ejemplo, para iniciar un seguimiento de todos los proveedores habilitados en el escenario InternetClient, escriba **netsh Trace Start Scenario = InternetClient**. Para capturar proveedores para más de un escenario, puede especificar todos los escenarios adecuados, como **netsh Trace Start Scenario = FileSharing Scenario = DirectAccess**. Tenga en cuenta que solo se puede habilitar una sesión de seguimiento a la vez; no es posible capturar simultáneamente la información de seguimiento de distintos conjuntos de proveedores en archivos independientes.

También puede iniciar un seguimiento para proveedores adicionales no incluidos en ese escenario en particular. Por ejemplo, puede que desee iniciar seguimientos de todos los proveedores habilitados bajo el escenario WLAN y también el proveedor DHCP. Para ello, escriba **netsh Trace Start Scenario = WLAN Provider = Microsoft-Windows-DHCP-Client**.

También puede ver más detalles sobre un proveedor específico escribiendo **netsh Trace show Provider** seguido del nombre del proveedor.

Para ver todas las opciones y filtros disponibles, puede escribir **netsh Trace Start/?**.

Para detener el seguimiento, escriba **netsh Trace STOP**.

## <a name="using-the-output-files"></a>Usar los archivos de salida

Cuando se detiene el seguimiento, se generan dos archivos de forma predeterminada: un archivo de registro de seguimiento de eventos (ETL) y un archivo. cab.

Los eventos de seguimiento se recopilan en el archivo ETL, que se puede ver mediante herramientas como Monitor de red. El archivo ETL se denominará archivo NetTrace. ETL de forma predeterminada, o puede especificar otro nombre incluyendo el valor de seguimiento **= nombrearchivo. ETL** al iniciar el seguimiento.

El archivo. cab contiene información enriquecida sobre el software y el hardware del sistema, como la información del adaptador, la compilación, el sistema operativo y la configuración inalámbrica. El archivo. cab se denominará nettrace.cab de forma predeterminada, a menos que se especifique otro nombre, como se indicó anteriormente.

Este archivo. cab contendrá dos archivos, que siempre tendrán el mismo nombre. Report. ETL es otra copia de la misma información incluida en archivo NetTrace. ETL. El archivo report.html incluye información adicional sobre los eventos de seguimiento y la otra información recopilada. Para obtener la mayoría de los detalles disponibles, incluya el comando **Report = Yes** al iniciar un seguimiento.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Usar filtros para reducir la cantidad de datos en el archivo de seguimiento ETL

Cuando se producen capturas durante un largo período de tiempo, el archivo de seguimiento ETL puede llegar a ser muy grande. En escenarios en los que varios proveedores están habilitados, lo que da lugar a un tráfico elevado, las restricciones de búfer de ETW pueden hacer que se quiten algunos seguimientos. Aparte de esta consideración, reducir la cantidad de datos en el archivo de seguimiento ETL puede ayudar a facilitar la solución de problemas reduciendo la cantidad de datos que se van a revisar.

Los filtros de seguimiento de Netsh se pueden usar para reducir el tamaño del archivo de seguimiento ETL. Estos filtros de seguimiento son niveles ETW y palabras clave que se pueden aplicar a proveedores individuales.

Para ver una lista de filtros que se pueden aplicar, escriba **netsh Trace Start/?**

Un ejemplo de filtro es **netsh Trace Start InternetClient Provider = Microsoft-Windows-TCPIP LEVEL = 5 Keywords = UT: ReceivePath, UT: SendPath**.

En este ejemplo, el nivel se establece en 5, lo que significa que se mostrará el número máximo de eventos. En la tabla siguiente se muestra la configuración disponible:



|       |               |                                                                            |
|-------|---------------|----------------------------------------------------------------------------|
| Nivel | Configuración       | Descripción                                                                |
| 1     | Crítico      | Solo se mostrarán los eventos críticos.                                        |
| 2     | Errors        | Se mostrarán los eventos y los errores críticos.                                  |
| 3     | Advertencias      | Se mostrarán los eventos críticos, los errores y las advertencias.                       |
| 4     | Informativo | Se mostrarán los eventos críticos, los errores, las advertencias y los eventos informativos. |
| 5     | Verbose       | Se mostrarán todos los eventos.                                                  |



 

Las palabras clave **UT: ReceivePath** y **UT: SentPath** filtran los eventos para mostrar solo los eventos de los que se realiza el seguimiento en la ruta de acceso de recepción o de envío. Para encontrar una lista completa de las palabras clave de un proveedor específico, escriba **netsh Trace show Provider** seguido del nombre del proveedor. Por ejemplo, si escribe **netsh Trace show Provider Microsoft-Windows-TCPIP** , se mostrará información sobre el proveedor Microsoft-Windows-TCPIP, incluida una lista de palabras clave.

Netsh también admite la capacidad de filtrado de paquetes (similar a Monitor de red) cuando se activa la captura de paquetes (mediante la configuración de **Capture = Yes**). El filtrado de paquetes se puede usar para capturar un número limitado de paquetes en un archivo de seguimiento. Por ejemplo, **netsh Trace Start Capture = Yes IPv4. Address = = x.x.** x. x. x, donde x. x es la dirección IP, solo capturará los paquetes con tráfico IPv4 con esa dirección de origen o destino específica.

Para obtener información adicional sobre cómo usar el filtrado de paquetes, puede escribir **netsh Trace show capturefilterHelp**.

 

 




