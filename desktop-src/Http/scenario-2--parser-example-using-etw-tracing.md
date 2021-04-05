---
title: Ejemplo de analizador de escenario 2 con seguimiento de ETW
description: Para generar un informe de seguimiento de ETW para el componente de la API del servidor HTTP, ejecute los pasos que se muestran en el paso \ 0034; Generar un informe de seguimiento de ETW \ 0034; sección del escenario 1 ejemplo de tiempo de espera HTTP que usa el seguimiento ETW y comandos Netsh, pero reproduce el error específico de este escenario.
ms.assetid: 2ccd2927-8a64-40a8-a29b-4b680a942f7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c566973b660e4e665226fbf9b4a266b086b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077764"
---
# <a name="scenario-2-parser-example-using-etw-tracing"></a>Escenario 2: ejemplo de analizador con seguimiento de ETW

Para generar un informe de seguimiento de ETW para el componente de API de servidor HTTP, ejecute los pasos que se muestran en la sección "generación de un informe de seguimiento de ETW" del [escenario 1: ejemplo de tiempo de espera de http mediante el seguimiento de ETW y comandos Netsh](scenario-1--http-timeout-example-using-etw-tracing-and-netsh-commands.md), pero reproduzca el error específico de este escenario. En este ejemplo, se tiene acceso a la aplicación web desde un equipo cliente, lo que da lugar a que se muestre el mensaje "400 Bad Request" en el cliente. Estos pasos se ejecutan en el servidor desde que se hospeda la aplicación Web.

## <a name="viewing-the-trace-and-diagnosing"></a>Ver el seguimiento y el diagnóstico

El archivo CSV resultante para seguimientos se puede ver en Excel o en cualquier herramienta que admita el formato CSV. En la tabla 2 siguiente se muestran fragmentos de un archivo de seguimiento de ejemplo (httptrace.csv). En el informe de seguimiento, la columna "nivel" muestra una entrada con un valor de "2", que representa un error. Como se indicó anteriormente, el componente de la API del servidor HTTP sigue los niveles de ETW definidos en el artículo [LevelType](../wes/eventmanifestschema-leveltype-complextype.md)tipo complejo tipo complejo.

Los niveles de ETW incluyen: 1 crítico; 2 error; 3 ADVERTENCIA; 4 información; 5 detallado.

Con este error, el tipo de evento (columna de tipo) notifica "ParseRequestFailed". En las columnas siguientes del evento ParseRequestFailed, vemos una entrada "InvalidHost". Esta entrada significa que el host identificado en la solicitud HTTP es incorrecto, según el protocolo HTTP. Tenga en cuenta que la columna con la entrada "InvalidHost" no se incluye en la tabla por razones de brevedad y para evitar el extracto de columnas no contiguas.

Para corregir este problema de análisis, el cliente web se debe corregir para que sea compatible con la RFC de HTTP. 

| Nombre del evento                    | Tipo               | Id. de evento | Versión | Canal | Nivel |
|-------------------------------|--------------------|----------|---------|---------|-------|
| Eventtracer                    | Encabezado             | 0        | 2       | 0       | 0     |
| Microsoft-Windows-HttpService | AddUrl             | 31       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnConnect        | 21       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ConnIdAssgn        | 22       | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | RecvReq            | 1        | 0       | 16      | 4     |
| Microsoft-Windows-HttpService | ParseRequestFailed | 52       | 0       | 16      | 2     |
| Microsoft-Windows-HttpService | LogFileWrite       | 51       | 0       | 16      | 4     |



 

Tabla 2: extractos de un informe de seguimiento de ejemplo para un problema de análisis

 

 