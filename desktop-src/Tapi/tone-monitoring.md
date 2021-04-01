---
description: La supervisión de tonos supervisa el flujo multimedia de una llamada para los tonos especificados.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Supervisión de tonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082762"
---
# <a name="tone-monitoring"></a>Supervisión de tonos

La supervisión de tonos supervisa el flujo multimedia de una llamada para los tonos especificados. Un tono se describe mediante sus frecuencias de componente y cadencia. Una implementación de la API puede permitir que se supervisen varios tonos diferentes simultáneamente. Una aplicación puede etiquetar cada tono para poder distinguir los distintos tonos para los que solicita detección.

Una aplicación puede habilitar o deshabilitar la supervisión de tono en una llamada especificada con [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones). Con esta función, la aplicación indica qué tonos detectar en una llamada especificada. Cuando está habilitada la supervisión de tonos, los dígitos detectados hacen que la aplicación reciba una notificación con el mensaje [**line \_ MONITORTONE**](line-monitortone.md) . Este mensaje proporciona el identificador de llamada en el que se detectó el tono, así como la etiqueta de la aplicación para el tono.

El ámbito de la supervisión de tonos está limitado por la duración de la llamada. La supervisión de tonos en una llamada finaliza en cuanto la llamada se *desconecta* o se queda *inactiva*.

> [!Note]  
> La supervisión de los tonos, los dígitos o los tipos de medios a menudo requiere el uso de recursos de los que el proveedor de servicios solo puede tener una cantidad finita. Si los recursos no están disponibles, se puede rechazar una solicitud de supervisión. Por la misma razón, una aplicación debe deshabilitar cualquier supervisión innecesaria.

 

 

 



