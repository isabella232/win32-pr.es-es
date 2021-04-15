---
title: Localidad temporal
description: La localidad temporal es una estrategia de prevención que reduce la ventana para las actualizaciones parciales.
ms.assetid: 8f454087-46cb-4fa6-b83a-65b2393029c3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceecff05d031875178b6192e7c633f70e4c91c50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486579"
---
# <a name="temporal-locality"></a>Localidad temporal

La *localidad temporal* es una estrategia de prevención que reduce la ventana para las actualizaciones parciales. La replicación de los cambios de una réplica de origen determinada continúa en orden USN ascendente. Las escrituras que se producen juntas en el tiempo tendrán los USN "cercanos" entre sí y se propagarán cerca del tiempo. Las aplicaciones que crean o actualizan varios objetos relacionados deben escribir los objetos lo más cerca posible del tiempo. Por ejemplo, la aplicación podría recopilar toda la información necesaria del usuario y aplicarla al directorio cuando el usuario haga clic en un botón "aplicar".

La localidad temporal también reduce la probabilidad de que se produzca una resolución de colisiones introduciendo incoherencias dentro de los objetos.

 

 




