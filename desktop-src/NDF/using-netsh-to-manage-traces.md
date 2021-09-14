---
title: Uso de Netsh para administrar seguimientos
description: En Windows 7, netsh.exe se puede usar desde un símbolo del sistema para habilitar y configurar seguimientos de red. En esta sección se describen algunos de los netsh.exe que pueden ayudar a solucionar problemas de seguimiento, incluida la nueva funcionalidad de seguimiento de netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074190"
---
# <a name="using-netsh-to-manage-traces"></a>Uso de Netsh para administrar seguimientos

En Windows 7, netsh.exe se puede usar desde un símbolo del sistema para habilitar y configurar seguimientos de red. En esta sección se describen algunos de los netsh.exe que pueden ayudar a solucionar problemas de seguimiento, incluida la nueva funcionalidad **de seguimiento de netsh.** Tenga en cuenta que los comandos netsh deben ejecutarse desde un símbolo del sistema con privilegios elevados.

## <a name="collecting-traces"></a>Recopilación de seguimientos

Los escenarios son conjuntos predefinidos de proveedores de seguimiento que se pueden habilitar para solucionar problemas. Para mostrar la lista de escenarios relacionados con la red disponibles, escriba **netsh trace show scenarios** **(netsh trace show providers** lists every one of the available providers, including ones that are not relevant to networking).

Cuando haya identificado un escenario que parece relevante para sus problemas, puede ver una lista de todos los proveedores incluidos en ese escenario. Por ejemplo, para ver todos los proveedores habilitados en el escenario InternetClient, escriba **netsh trace show scenario internetclient**.

Puede iniciar un seguimiento de todos los proveedores en un escenario o conjunto de escenarios determinados. Por ejemplo, para iniciar un seguimiento de todos los proveedores habilitados en el escenario InternetClient, escriba **netsh trace start scenario=internetclient**. Para capturar proveedores para más de un escenario, puede especificar todos los escenarios adecuados, como **netsh trace start scenario=FileSharing scenario=DirectAccess**. Tenga en cuenta que solo se puede habilitar una sesión de seguimiento a la vez; no es posible capturar simultáneamente información de seguimiento de diferentes conjuntos de proveedores en archivos independientes.

También puede iniciar un seguimiento de proveedores adicionales no incluidos en ese escenario concreto. Por ejemplo, puede que desee iniciar seguimientos para todos los proveedores habilitados en el escenario WLAN y también para el proveedor DHCP. Para ello, escriba **netsh trace start scenario=wlan provider=Microsoft-Windows-Dhcp-Client**.

También puede ver más detalles sobre un proveedor específico escribiendo **netsh trace show provider** seguido del nombre del proveedor.

Para ver todas las opciones y filtros disponibles, puede escribir **netsh trace start /?**.

Para detener el seguimiento, escriba **netsh trace stop**.

## <a name="using-the-output-files"></a>Uso de los archivos de salida

Cuando se detiene el seguimiento, se generan dos archivos de forma predeterminada: un archivo de registro de seguimiento de eventos (ETL) y un archivo .cab eventos.

Los eventos de seguimiento se recopilan en el archivo ETL, que se puede ver mediante herramientas como Monitor de red. El archivo ETL se denominará nettrace.etl de forma predeterminada, o puede especificar un nombre diferente incluyendo **tracefile=filename.etl** al iniciar el seguimiento.

El .cab archivo contiene información completa sobre el software y el hardware del sistema, como la información del adaptador, la compilación, el sistema operativo y la configuración inalámbrica. El .cab se denominará nettrace.cab de forma predeterminada, a menos que se especifique otro nombre como se indicó anteriormente.

Este .cab archivo contendrá dos archivos, que siempre tendrán el mismo nombre. Report.etl es otra copia de la misma información incluida en nettrace.etl. El report.html archivo incluye información adicional sobre los eventos de seguimiento y la otra información recopilada. Para recibir la mayoría de los detalles disponibles, incluya el informe **de comandos = sí al** iniciar un seguimiento.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Uso de filtros para reducir la cantidad de datos en el archivo de seguimiento ETL

Cuando se suceden capturas durante un largo período de tiempo, el archivo de seguimiento ETL puede llegar a ser muy grande. En escenarios en los que se habilitan varios proveedores, lo que da lugar a un tráfico elevado, las restricciones de búfer ETW pueden provocar que se desasoyen algunos seguimientos. Aparte de esta consideración, reducir la cantidad de datos en el archivo de seguimiento ETL puede ayudar a facilitar la solución de problemas al reducir la cantidad de datos que se deben revisar.

Los filtros de seguimiento de Netsh se pueden usar para reducir el tamaño del archivo de seguimiento ETL. Estos filtros de seguimiento son niveles etw y palabras clave que se pueden aplicar a proveedores individuales.

Para ver una lista de filtros que se pueden aplicar, escriba **netsh trace start /?**

Un ejemplo de filtro es **netsh trace start InternetClient provider=Microsoft-Windows-TCPIP level=5 keywords=ut:ReceivePath,ut:SendPath**.

En este ejemplo, el nivel se establece en 5, lo que significa que se mostrará el número máximo de eventos. En la tabla siguiente se muestra la configuración disponible:



| Nivel      | Parámetro              | Descripción                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Crítico      | Solo se mostrarán los eventos críticos.                                        |
| 2     | Errors        | Se mostrarán los eventos y errores críticos.                                  |
| 3     | Advertencias      | Se mostrarán eventos críticos, errores y advertencias.                       |
| 4     | Informativo | Se mostrarán eventos críticos, errores, advertencias y eventos informativos. |
| 5     | Verbose       | Se mostrarán todos los eventos.                                                  |



 

Las palabras clave **ut:ReceivePath** y **ut:SentPath** filtran los eventos para mostrar solo los eventos de seguimiento en la ruta de acceso de recepción o envío. Para encontrar una lista completa de palabras clave para un proveedor específico, escriba **netsh trace show provider** seguido del nombre del proveedor. Por ejemplo, si escribe **netsh trace show provider Microsoft-Windows-TCPIP,** se mostrará información sobre el proveedor Microsoft-Windows-TCPIP, incluida una lista de palabras clave.

Netsh también admite la funcionalidad de filtrado de paquetes (similar a Monitor de red) cuando la captura de paquetes está activada (estableciendo **capture = yes**). El filtrado de paquetes se puede usar para capturar un número limitado de paquetes en un archivo de seguimiento. Por ejemplo, **netsh trace start capture = yes ipv4.address == x.x.x.x** , donde x.x.x.x es la dirección IP, solo capturará paquetes con tráfico ipv4 con esa dirección de origen o destino específica.

Para obtener información adicional sobre cómo usar el filtrado de paquetes, puede escribir **netsh trace show capturefilterHelp**.

 

 




