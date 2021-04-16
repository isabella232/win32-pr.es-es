---
description: Reserva activa
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Reserva activa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4d007e9219ea79ae3bda31be595c33b537661a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678448"
---
# <a name="hot-sparing"></a>Reserva activa

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La reserva activa es la sustitución de un disco o unidad para un disco o una unidad con errores. (Los proveedores de hardware actúan en unidades; los proveedores de software actúan en discos). Puede compartir una unidad de reserva activa entre todos los LUN del subsistema o asociarla a un LUN específico. Del mismo modo, puede asociar un disco de reserva activa con un solo volumen, un paquete y un proveedor de software, o bien compartirlo entre todos los hosts de una red SAN.

Si el volumen o LUN asociado es tolerante a errores, puede sustituir una reserva activa por un disco o unidad con errores y volver a generar los reflejos o RAID de paridad afectados. Puede sustituir una reserva activa para un disco con errores aunque el volumen o LUN asociado no sea tolerante a errores. Suponiendo que pueda determinar el error inminente antes de que se produzca una pérdida de datos catastrófica, puede reflejar temporalmente la reserva activa en el disco o unidad con errores y, a continuación, quitar el disco o la unidad con errores.

La reserva activa puede ser automática o manual. Si un proveedor implementa el reemplazo en caliente automático, realiza la sustitución dinámicamente. El sparing activo manual requiere la intervención del operador o de la aplicación. Una reserva activa puede contener datos parciales o formato de un uso anterior. VDS sobrescribe la reserva activa cuando se produce la sustitución.

No se puede usar una reserva activa para las operaciones de enlace normales. Si la reserva activa es mayor que el disco o la unidad con errores, cualquier espacio sobrante permanece sin usar hasta que se declare explícitamente disponible para el enlace. Una vez que la reserva activa se ha usado para la recuperación, el disco o la unidad ya no es una reserva activa. En otras palabras, el eje 1 16-Gigabyte no puede actuar como reservas activas de 2 8 gigabytes.

 

 
