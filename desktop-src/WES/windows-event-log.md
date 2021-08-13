---
title: Registro de sucesos de Windows
description: La WINDOWS Event Log API define el esquema que se usa para escribir un manifiesto de instrumentación.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4306ce9722aba5b06109265c71cf387af2b35f63aef1cec070936400fff61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587200"
---
# <a name="windows-event-log"></a>Registro de sucesos de Windows

## <a name="purpose"></a>Finalidad

La WINDOWS Event Log API define el esquema que se usa para escribir un manifiesto de instrumentación. Un manifiesto de instrumentación identifica el proveedor de eventos y los eventos que registra. La API también incluye las funciones que un consumidor de eventos, como el Visor de eventos [,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))usaría para leer y representar los eventos. Para escribir los eventos definidos en el manifiesto, use las funciones incluidas en la API [de seguimiento](/windows/desktop/ETW/event-tracing-portal) de eventos (ETW).

Windows El registro de eventos reemplaza la API [de registro](/windows/desktop/EventLog/event-logging) de eventos a partir del Windows operativo Vista.

## <a name="developer-audience"></a>Audiencia de desarrolladores

Windows El registro de eventos está diseñado para programadores de C/C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

Windows El registro de eventos se incluye en el sistema operativo a partir de Windows Vista y Windows Server 2008.

Para obtener información sobre los requisitos en tiempo de ejecución para un elemento de programación determinado, vea la sección Requisitos de la página de referencia de ese elemento.

Para obtener un historial de versiones completo, [vea Novedades.](what-s-new.md)

## <a name="in-this-section"></a>En esta sección


| Tema                                                        | Descripción                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Uso del Windows de eventos](using-windows-event-log.md)        | Guía de procedimientos que muestra cómo usar la API Windows Event Log API.                                 |
| [Windows Referencia del registro de eventos](windows-event-log-reference.md)| Tipos de datos, funciones, enumeraciones, estructuras, constantes y esquemas que incluye la API.|