---
title: Reenviador
description: El reenviador es el componente de modo kernel del enrutador que es responsable de reenviar los datos de una interfaz de enrutador a los demás.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52885000a9f1fcc117cd1fefc207531b9b524e74
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075770"
---
# <a name="forwarder"></a>Reenviador

El reenviador es el componente de modo kernel del enrutador que es responsable de reenviar los datos de una interfaz de enrutador a los demás. El reenviador también decide si un paquete está destinado a la entrega local, si está destinado a reenviarse fuera de otra interfaz o a ambos.

Hay dos reenviadores de modo kernel: unidifusión y multidifusión.

El administrador de enrutadores obtiene las mejores rutas a todos los destinos del administrador de tablas de enrutamiento. Estas rutas se pasan al reenviador de unidifusión. El reenviador de unidifusión utiliza estas rutas para realizar el reenvío real de datos de unidifusión. De esta manera, el reenviador de unidifusión mantiene una memoria caché de las mejores rutas en la vista de unidifusión de la tabla de enrutamiento.

El administrador de grupos de multidifusión usa información de la vista multidifusión de la tabla de enrutamiento para agregar entradas de reenvío de multidifusión al reenviador de multidifusión.

 

 




