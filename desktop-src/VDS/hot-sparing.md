---
description: Hot Sparing
ms.assetid: 2faf2f3f-f459-4e41-9c8e-042c7b72281b
title: Hot Sparing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61b8df9bc27e303277c869901872a9b879cb2d7df32764589501b9d33a51c3fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125955"
---
# <a name="hot-sparing"></a>Hot Sparing

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se [reemplaza por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La moderación de acceso es la sustitución de un disco o unidad por un disco o unidad con errores o con errores. (Los proveedores de hardware actúan en las unidades; los proveedores de software actúan en los discos). Puede compartir una unidad de reserva en caliente entre todos los LUN del subsistema o asociarla a un LUN específico. Del mismo modo, puede asociar un disco de reserva en caliente con un único volumen, paquete y proveedor de software, o compartirlo entre todos los hosts de una SAN.

Si el volumen o LUN asociados son tolerantes a errores, puede sustituir una reserva en caliente por un disco o unidad con errores y recompilar cualquier RAID o reflejo de paridad afectado. Puede sustituir una reserva en caliente por un disco con errores aunque el volumen o LUN asociado no sea tolerante a errores. Suponiendo que puede determinar el error que se produce antes de una pérdida de datos grave, puede reflejar temporalmente la reserva en caliente en el disco o unidad con errores y, a continuación, quitar el disco o la unidad con errores.

La zona de acceso de acceso es automática o manual. Si un proveedor implementa una zona activa automática, realiza la sustitución dinámicamente. La moderación manual requiere la intervención del operador o de la aplicación. Una reserva en caliente puede contener datos parciales o formatos de un uso anterior. VDS sobrescribe la reserva en caliente cuando se produce la sustitución.

No se puede usar una reserva en caliente para las operaciones de enlace normales. Si la reserva de acceso rápido es mayor que el disco o la unidad con errores, cualquier exceso de espacio permanece sin usar hasta que se declara explícitamente disponible para el enlace. Una vez que se ha usado la reserva en caliente para la recuperación, el disco o la unidad ya no es una reserva en caliente. En otras palabras, un eje de 16 gigabytes no puede actuar como dos reservas de 8 gigabytes en caliente.

 

 
