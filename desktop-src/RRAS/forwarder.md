---
title: Reenviador
description: El reenviador es el componente de modo kernel del enrutador responsable de reenviar datos de una interfaz de enrutador a los demás.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5011d340b444c9d0be5b26ee5449f041bb7419fd4a52f8a983ce2b85d9b106f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674025"
---
# <a name="forwarder"></a>Reenviador

El reenviador es el componente de modo kernel del enrutador responsable de reenviar datos de una interfaz de enrutador a los demás. El reenviador también decide si un paquete está destinado a la entrega local, si está destinado a reenviarse fuera de otra interfaz, o ambos.

Hay dos reenviadores de modo kernel: unidifusión y multidifusión.

El administrador de enrutadores obtiene las mejores rutas a todos los destinos del administrador de tablas de enrutamiento. Estas rutas se pasan al reenviador de unidifusión. El reenviador de unidifusión usa estas rutas para realizar el reenvío real de datos de unidifusión. De esta manera, el reenviador de unidifusión mantiene una caché de las mejores rutas en la vista de unidifusión de la tabla de enrutamiento.

El administrador de grupos de multidifusión usa información de la vista de multidifusión de la tabla de enrutamiento para agregar entradas de reenvío de multidifusión al reenviador de multidifusión.

 

 




