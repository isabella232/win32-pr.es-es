---
title: Espacios de color dependientes del dispositivo
description: La mayoría de los espacios de color dependen del dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Sistema de colores (WCS), espacios de color dependientes del dispositivo
- WCS (Windows de colores), espacios de color dependientes del dispositivo
- administración de colores de imagen, espacios de color dependientes del dispositivo
- administración de colores, espacios de color dependientes del dispositivo
- colors,device-dependent color spaces
- espacios de color, dependientes del dispositivo
- espacios de colores dependientes del dispositivo
- punto blanco
- Colorantes
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe10ad9d48e750f9869b113a45f1235d2aa692532702ea4443ec3629d32276ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593625"
---
# <a name="device-dependent-color-spaces"></a>Espacios de color dependientes del dispositivo

La mayoría [de los espacios de color](c.md) dependen del dispositivo. Aunque un dispositivo determinado, como una impresora, puede usar el espacio de colores SPACE, los colores que representa para valores SPACE específicos suelen ser ligeramente diferentes de todos los demás tipos de impresoras. Es precisamente por esta razón que el sistema de administración de colores WCS 1.0 es tan útil.

Todos los espacios de color tienen *un punto blanco*, que se define como el blanco más blanco que se puede generar en ese espacio de colores. Dado que los dispositivos pueden diferir entre sí, sus puntos en blanco también pueden diferir. Todos los colores que un dispositivo puede producir son relativos a su punto blanco. Por lo tanto, un sistema de administración de colores debe ser capaz de asignar el punto blanco de un espacio de color a otro y conservar las ubicaciones relativas de todos los colores. También debe ser capaz de asignar un color de un espacio de color a su coincidencia más cercana en otro espacio de colores, independientemente de las diferencias en los puntos en blanco. WCS 1.0 puede realizar ambas tareas.

El espacio de colores RGB se usa a menudo en monitores de equipo. Por lo tanto, depende del dispositivo. Normalmente, las impresoras usan [coloreantes](c.md)NTES. Cada impresora implementa su propia versión del espacio de colores SPACE. Es posible que las imágenes digitales no almacenen colores en ellas. Pueden almacenar números de índice en una paleta de colores. El resultado es que es muy difícil para los desarrolladores de aplicaciones individuales usar o proporcionar un método estandarizado para mover imágenes de color de un dispositivo a otro. Normalmente, los profesionales de la creación de imágenes experimentan la frustración de crear una imagen gráfica en una pantalla de equipo y de que se imprima de forma muy diferente. WCS 1.0 aborda estas necesidades de creación de imágenes.

 

 




