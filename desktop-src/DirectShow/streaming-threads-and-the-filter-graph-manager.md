---
description: Subprocesos de streaming y filter Graph Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Subprocesos de streaming y filter Graph Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3501f984880fad22399cbda8710acaf2be1d6c4223e07a4c0f6e4c180d0699cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329775"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a>Subprocesos de streaming y filter Graph Manager

Cuando filter Graph Manager detiene el gráfico, espera a que se apaguen todos los subprocesos de streaming. Esto tiene las siguientes implicaciones para los filtros:

-   Un filtro nunca debe llamar a métodos en filter Graph Manager desde un subproceso de streaming.

    Filter Graph Manager usa una sección crítica para sincronizar sus propias operaciones. Si un subproceso de streaming intenta contener esta sección crítica, puede provocar un interbloqueo. Por ejemplo: supongamos que otro subproceso detiene el gráfico. Ese subproceso toma el bloqueo del gráfico de filtro y espera a que el filtro deje de entregar datos. Si el filtro está esperando el bloqueo, nunca se detendrá, lo que provocará un interbloqueo.

-   Un filtro nunca debe **agregar o** **queryinterface** el administrador Graph filtro de un subproceso de streaming.

    Si el filtro contiene un recuento de referencias en filter Graph Manager (a través de **AddRef** o **QueryInterface),** podría convertirse en el último objeto que contiene un recuento de referencias. Cuando el filtro llama **a Release**, filter Graph Manager se destruye a sí mismo. Dentro de su rutina de limpieza, filter Graph Manager intenta detener el gráfico, lo que hace que espere a que se cierre el subproceso de streaming. Sin embargo, está esperando dentro del subproceso de streaming, por lo que el subproceso de streaming no puede salir. El resultado es un interbloqueo.

 

 



