---
description: Registro e informes de errores
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registro e informes de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d974b4043b4365839aec6a4fae392ae1d84900e8b8347949147b8df13326bd1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990765"
---
# <a name="logging-and-error-reporting"></a>Registro e informes de errores

## <a name="log-file"></a>Archivo de registro

COMREPL genera un archivo de registro que contiene mensajes de estado y de error. Este archivo se almacena en el equipo donde comREPL se inició en la replicación %systemdir% \\ com \\ \\ ComRepl.log.

Este archivo de registro se borra cuando se inicia una fase de copia. La instalación posterior en destinos se anexará al archivo.

## <a name="error-handling"></a>Control de errores

Los errores se anotan en el archivo de registro descrito anteriormente. También se puede encontrar información de error detallada en el registro de eventos de los equipos de origen o de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Uso de COMREPL](using-comrepl.md)
</dt> <dt>

[Qué se replica](what-gets-replicated.md)
</dt> </dl>

 

 



