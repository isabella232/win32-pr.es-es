---
title: Pruebas y depuración
description: Hay un \ 0034;echo \ 0034; agente de escucha implementado por el cliente Conexión a Escritorio remoto (RDC), que siempre está presente y que escucha las conexiones entrantes.
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cacabf8f30772fa654a1fefc24ff8059ff5e002cde8f633537ce8f2f07f068
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987045"
---
# <a name="testing-and-debugging"></a>Pruebas y depuración

Hay un agente de escucha de "eco" que implementa el cliente de Conexión a Escritorio remoto (RDC), que siempre está presente y que escucha las conexiones entrantes. Al escribir el lado servidor de un módulo de canal virtual dinámico (DVC), como prueba rápida, puede abrir un punto de conexión denominado "ECHO". Cualquier escritura en un canal del que se crea una instancia desde este punto de conexión dará como resultado la recepción de los mismos datos.

Puede usar esta técnica para probar una implementación de entrada/salida (E/S) del módulo del lado servidor, medir el tiempo de respuesta de un complemento de cliente de Conexión a Escritorio remoto (RDC) o medir el retraso de red para el cliente de Conexión a Escritorio remoto (RDC). No hay ninguna limitación en la cantidad de datos que se pueden enviar a través de este canal.

 

 




