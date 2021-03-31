---
title: Registro de errores de Windows
description: La API del registro de eventos de Windows define el esquema que se utiliza para escribir un manifiesto de instrumentación.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904811"
---
# <a name="windows-event-log"></a>Registro de errores de Windows

## <a name="purpose"></a>Propósito

La API del registro de eventos de Windows define el esquema que se utiliza para escribir un manifiesto de instrumentación. Un manifiesto de instrumentación identifica el proveedor de eventos y los eventos que registra. La API también incluye las funciones que un consumidor de eventos, como el [visor de eventos](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), usaría para leer y representar los eventos. Para escribir los eventos definidos en el manifiesto, use las funciones incluidas en la API de [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) (ETW).

El registro de eventos de Windows sustituye a la API de [registro de eventos](/windows/desktop/EventLog/event-logging) a partir del sistema operativo Windows Vista.

## <a name="developer-audience"></a>Audiencia de desarrolladores

El registro de eventos de Windows está diseñado para programadores de C/C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

El registro de eventos de Windows se incluye en el sistema operativo a partir de Windows Vista y Windows Server 2008.

Para obtener información sobre los requisitos de tiempo de ejecución para un elemento de programación determinado, vea la sección de requisitos de la página de referencia de ese elemento.

Para ver el historial de versiones completo, vea [novedades](what-s-new.md).

## <a name="in-this-section"></a>En esta sección


| Tema                                                        | Descripción                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Uso del registro de eventos de Windows](using-windows-event-log.md)        | Guía de procedimientos que muestra cómo usar la API del registro de eventos de Windows.                                 |
| [Referencia del registro de eventos de Windows](windows-event-log-reference.md)| Los tipos de datos, las funciones, las enumeraciones, las estructuras, las constantes y los esquemas que incluye la API.|