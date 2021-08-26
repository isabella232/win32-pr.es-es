---
description: La supervisión del tono supervisa el flujo multimedia de una llamada para los tono especificados.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Supervisión del tono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb811d91a70f439ae17123b35967800914bd6a04f1a30168754f602231f038e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034185"
---
# <a name="tone-monitoring"></a>Supervisión del tono

La supervisión del tono supervisa el flujo multimedia de una llamada para los tono especificados. Un tono se describe por sus frecuencias de componentes y cadencia. Una implementación de la API puede permitir la supervisión simultánea de varios tonos diferentes. Una aplicación puede etiquetar cada tono para poder distinguir los distintos tonos para los que solicita la detección.

Una aplicación puede habilitar o deshabilitar la supervisión del tono en una llamada especificada con [**lineMonitorMonitorMonitor .**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones) Con esta función, la aplicación indica qué tonos se detectarán en una llamada especificada. Cuando la supervisión de tono está habilitada, los dígitos detectados hacen que la aplicación se notifique con el [**mensaje LINE \_ MONITORTONE.**](line-monitortone.md) Este mensaje proporciona el identificador de llamada en el que se detectó el tono, así como la etiqueta de la aplicación para el tono.

El ámbito de la supervisión del tono está enlazado por la duración de la llamada. La supervisión del tono en una llamada finaliza en cuanto la llamada *se desconecta* o se queda *inactiva.*

> [!Note]  
> La supervisión de los tonos, dígitos o tipos de medios a menudo requiere el uso de recursos de los que el proveedor de servicios solo puede tener una cantidad finita. Se puede rechazar una solicitud de supervisión si los recursos no están disponibles. Por el mismo motivo, una aplicación debe deshabilitar cualquier supervisión innecesaria.

 

 

 



