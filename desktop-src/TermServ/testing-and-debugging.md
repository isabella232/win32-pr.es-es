---
title: Pruebas y depuración
description: Hay un 0034; echo \ 0034; agente de escucha implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676118"
---
# <a name="testing-and-debugging"></a>Pruebas y depuración

Hay un agente de escucha de "Eco" implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y escuchando conexiones entrantes. Al escribir el lado del servidor de un módulo de canal virtual dinámico (DVC), como una prueba rápida, puede abrir un punto de conexión denominado "ECHO". Cualquier escritura en un canal del que se crean instancias desde este punto de conexión dará como resultado la recepción de los mismos datos.

Puede usar esta técnica para probar una implementación de entrada/salida (e/s) del módulo de servidor, para medir el tiempo de respuesta de un complemento de cliente Conexión a Escritorio remoto (RDC) o para medir el retraso de red para el cliente Conexión a Escritorio remoto (RDC). No hay ninguna limitación en la cantidad de datos que se pueden enviar a través de este canal.

 

 




