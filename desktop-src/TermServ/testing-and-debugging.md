---
title: Pruebas y depuración
description: Hay un \ 0034;echo \ 0034; agente de escucha implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y que escucha las conexiones entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170622"
---
# <a name="testing-and-debugging"></a>Pruebas y depuración

Hay un agente de escucha de "eco" implementado por el cliente de Conexión a Escritorio remoto (RDC), que siempre está presente y que escucha las conexiones entrantes. Al escribir el lado servidor de un módulo de canal virtual dinámico (DVC), como prueba rápida, puede abrir un punto de conexión denominado "ECHO". Cualquier escritura en un canal del que se crea una instancia desde este punto de conexión dará como resultado la recepción de los mismos datos.

Puede usar esta técnica para probar una implementación de entrada/salida (E/S) del módulo del lado servidor, medir el tiempo de respuesta de un complemento de cliente de Conexión a Escritorio remoto (RDC) o medir el retraso de red para el cliente de Conexión a Escritorio remoto (RDC). No hay ninguna limitación en la cantidad de datos que se pueden enviar a través de este canal.

 

 




