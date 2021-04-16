---
description: Registro e informes de errores
ms.assetid: 162ce34b-cc82-40bb-8422-a639152aee25
title: Registro e informes de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cdc29d32ae26429f2fe23fe88762fabf82185c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677237"
---
# <a name="logging-and-error-reporting"></a>Registro e informes de errores

## <a name="log-file"></a>Archivo de registro

COMREPL genera un archivo de registro que contiene mensajes de estado y de error. Este archivo se almacena en el equipo en el que se inició COMREPL en% systemdir% \\ com \\ replicate \\ COMRepl. log.

Este archivo de registro se borra cuando se inicia una fase de copia. La instalación posterior en destinos se anexará al archivo.

## <a name="error-handling"></a>Control de errores

Los errores se indican en el archivo de registro que se ha descrito anteriormente. También se puede encontrar información detallada del error en el registro de eventos de los equipos de origen o de destino.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de archivos](file-management.md)
</dt> <dt>

[Fases de replicación](replication-phases.md)
</dt> <dt>

[Usar COMREPL](using-comrepl.md)
</dt> <dt>

[Lo que se replica](what-gets-replicated.md)
</dt> </dl>

 

 



