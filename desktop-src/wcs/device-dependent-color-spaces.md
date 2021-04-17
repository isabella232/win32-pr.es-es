---
title: Espacios de color dependientes del dispositivo
description: La mayoría de los espacios de colores dependen del dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Sistema de color de Windows (WCS), espacios de colores dependientes del dispositivo
- WCS (sistema de colores de Windows), espacios de colores dependientes del dispositivo
- Administración del color de imagen, espacios de colores dependientes del dispositivo
- Administración del color, espacios de colores dependientes del dispositivo
- colores, espacios de colores dependientes del dispositivo
- espacios de colores, dependientes del dispositivo
- espacios de colores dependientes del dispositivo
- punto blanco
- colorants
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/26/2021
ms.locfileid: "105721129"
---
# <a name="device-dependent-color-spaces"></a>Espacios de color dependientes del dispositivo

La mayoría de los [espacios de colores](c.md) dependen del dispositivo. Aunque un dispositivo determinado, como una impresora, puede usar el espacio de colores CMYK, los colores que representa para valores CMYK específicos suelen ser ligeramente diferentes de los demás tipos de impresoras. Por esta razón, el sistema de administración del color WCS 1,0 es tan útil.

Todos los espacios de colores tienen un *punto blanco*, que se define como el blanco más blanco que se puede producir en ese espacio de colores. Dado que los dispositivos pueden diferir entre sí, sus puntos blancos también pueden ser diferentes. Todos los colores que un dispositivo puede producir son relativos a su punto blanco. Por lo tanto, un sistema de administración del color debe ser capaz de asignar el punto blanco de un espacio de colores a otro y conservar las ubicaciones relativas de todos los colores. También debe poder asignar un color de un espacio de colores a la coincidencia más cercana en otro espacio de colores, independientemente de las diferencias en los puntos blancos. WCS 1,0 puede realizar ambas tareas.

El espacio de colores RGB se usa a menudo en monitores de equipos. Como tal, depende del dispositivo. Las impresoras suelen usar [COLORANTS](c.md)CMYK. Cada impresora implementa su propia versión del espacio de colores CMYK. Es posible que las imágenes digitales no almacenen realmente colores en ellas. Pueden almacenar números de índice en una paleta de colores. El resultado es que es muy difícil para los desarrolladores de aplicaciones individuales usar o proporcionar un método estandarizado para mover imágenes de color de un dispositivo a otro. Los profesionales de la creación de imágenes suelen experimentar la frustración de la creación de una imagen gráfica en la pantalla de un equipo y de que se convierta de forma muy diferente cuando se imprima. WCS 1,0 aborda estas necesidades de creación de imágenes.

 

 




