---
description: La región de actualización identifica la parte de una ventana que no está actualizada o no es válida y necesita volver a dibujarse.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717975"
---
# <a name="the-update-region"></a>Región de actualización

La *región de* actualización identifica la parte de una ventana que no está actualizada o no es válida y necesita volver a dibujarse. El sistema usa la región de actualización para generar mensajes [**WM \_ PAINT**](wm-paint.md) para las aplicaciones y para minimizar el tiempo que las aplicaciones dedican a actualizar el contenido de sus ventanas. El sistema agrega solo la parte no válida de la ventana a la región de actualización, lo que requiere que solo se retrase esa parte.

Cuando el sistema determina que una ventana necesita actualizarse, establece las dimensiones de la región de actualización en la parte no válida de la ventana. Establecer la región de actualización no hace que la aplicación se dibuje inmediatamente. En su lugar, la aplicación continúa recuperando mensajes de la cola de mensajes de la aplicación hasta que no queda ningún mensaje. A continuación, el sistema comprueba la región de actualización y, si la región no está vacía (no ES NULL), envía un mensaje [**WM \_ PAINT**](wm-paint.md) al procedimiento de ventana.

Una aplicación puede usar la región de actualización para generar sus [**mensajes \_ WM PAINT.**](wm-paint.md) Por ejemplo, una aplicación que carga datos de archivos abiertos normalmente establece la región de actualización durante la carga para que se dibujen nuevos datos durante el procesamiento del siguiente **mensaje \_ WM PAINT.** En general, una aplicación no debe dibujar en el momento en que cambian sus datos, sino enrutar todas las operaciones de dibujo a través del **mensaje \_ WM PAINT.**

 

 



