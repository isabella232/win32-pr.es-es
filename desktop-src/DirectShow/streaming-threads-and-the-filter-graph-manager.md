---
description: Streaming de subprocesos y Filter Graph Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streaming de subprocesos y Filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678151"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Streaming de subprocesos y Filter Graph Manager

Cuando el administrador de gráficos de filtro detiene el gráfico, espera a que se cierren todos los subprocesos de streaming. Esto tiene las implicaciones siguientes para los filtros:

-   Un filtro no debe llamar nunca a los métodos del administrador de gráficos de filtro desde un subproceso de streaming.

    Filter Graph Manager usa una sección crítica para sincronizar sus propias operaciones. Si un subproceso de streaming intenta contener esta sección crítica, puede producirse un interbloqueo. Por ejemplo: Supongamos que otro subproceso detiene el gráfico. Ese subproceso toma el bloqueo del gráfico de filtro y espera a que el filtro deje de entregar los datos. Si el filtro está esperando el bloqueo, nunca se detendrá, lo que provocará un interbloqueo.

-   Un filtro nunca debe **AddRef** o **QueryInterface** para filtrar el administrador de gráficos de un subproceso de streaming.

    Si el filtro contiene un recuento de referencias en el administrador de gráficos de filtro (a través de **AddRef** o **QueryInterface**), es posible que se convierta en el último objeto que contiene un recuento de referencias. Cuando el filtro llama a **Release**, el administrador de gráficos de filtro se destruye a sí mismo. Dentro de su rutina de limpieza, el administrador de gráficos de filtro intenta detener el gráfico, lo que espera a que se cierre el subproceso de streaming. Sin embargo, está esperando en el subproceso de streaming, por lo que el subproceso de streaming no puede salir. El resultado es un interbloqueo.

 

 



