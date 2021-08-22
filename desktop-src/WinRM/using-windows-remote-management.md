---
title: Uso de Windows administración remota
description: Windows La administración remota está pensada para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan una variedad de sistemas operativos.
ms.assetid: 6ee2b238-5bc2-4274-b7ca-49dbc728d8f1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1c13359ad06e00b9228a1d2c5f425d46c04f7c3003cad3e3e0af658ae8c7191f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118823257"
---
# <a name="using-windows-remote-management"></a>Uso de Windows administración remota

Windows La administración remota está pensada para mejorar la administración de hardware en un entorno de red con varios dispositivos que ejecutan una variedad de sistemas operativos. Todo el diseño del servicio está orientado a la monitorización y la administración de equipos remotos implementando un protocolo estándar interoperable.

Dado que la API de scripting de WinRM y la API de [C++](winrm-c---api.md) de [WinRM](winrm-scripting-api.md) implementan y modela estrechamente las operaciones definidas para el protocolo WS-Management, los scripts y las aplicaciones reciben secuencias de XML en respuesta a las solicitudes. Los parámetros de entrada para las llamadas de método deben construirse en XML. Puede usar los métodos de la API [MSXML](/previous-versions/windows/desktop/ms763742(v=vs.85)) para mostrar o construir cadenas XML. Para obtener un ejemplo, vea [Mostrar la salida XML de scripts winRM.](displaying-xml-output-from-winrm-scripts.md)

En la lista siguiente se incluyen temas que describen cómo usar el scripting winRM:

-   [Detectar si un equipo remoto admite WS-Management protocolo](detecting-whether-a-remote-computer-supports-ws-management-protocol.md)
-   [Obtener datos del equipo local](obtaining-data-from-the-local-computer.md)
-   [Obtener datos de un equipo remoto](obtaining-data-from-a-remote-computer.md)
-   [Enumerar o enumerar todas las instancias de un recurso](enumerating-or-listing-all-instances-of-a-resource.md)
-   [Consulta de instancias específicas de un recurso](querying-for-specific-instances-of-a-resource.md)
-   [Mostrar la salida XML de scripts WinRM](displaying-xml-output-from-winrm-scripts.md)

## <a name="tracing-winrm-activity"></a>Seguimiento de la actividad winRM

Dado que WinRM obtiene datos a través [de Windows Management Instrumentation (WMI),](/windows/desktop/WmiSdk/wmi-start-page)puede realizar un seguimiento de la actividad WMI que resulta de los mensajes de WinRM. A partir Windows Vista, el servicio WMI ya no usa los [archivos de registro wmi](/windows/desktop/WmiSdk/wmi-log-files). En su lugar, usa [Seguimiento de](/windows/desktop/ETW/event-tracing-portal) eventos  (ETW) y los eventos están disponibles a través de la interfaz de usuario Visor de eventos o la herramienta de línea de comandos Evtutil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración remota de Windows](portal.md)
</dt> <dt>

[Acerca de Windows administración remota](about-windows-remote-management.md)
</dt> <dt>

[Windows Referencia de administración remota](windows-remote-management-reference.md)
</dt> <dt>

[Scripting en Windows administración remota](scripting-in-windows-remote-management.md)
</dt> </dl>

 

 