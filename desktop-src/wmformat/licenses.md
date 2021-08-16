---
title: Licencias
description: Licencias
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- Windows SDK de formato multimedia, administración de derechos digitales (DRM)
- Windows SDK de formato multimedia, licencias DRM
- Windows SDK de formato multimedia, licencias para DRM
- administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b899e44ffdff5d2a7f3c5fb3237b477ae0143327a331f63bd9717e3ae4320483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118700839"
---
# <a name="licenses"></a>Licencias

Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos. Cada licencia se aplica a un identificador de clave, que normalmente se asigna a un único archivo multimedia. Este identificador es lo que se usa para identificar el contenido protegido en la licencia.

Cada licencia especifica una o varias acciones que se pueden realizar con el contenido protegido. Estas acciones, también denominadas derechos, se pueden limitar de varias maneras. Al combinar las fechas de inicio, las fechas de finalización, los recuentos y los límites de tiempo, el emisor de la licencia puede crear casi cualquier limitación general sobre un derecho.

Las licencias las emite un servicio web. Cuando se adquiere una licencia, se almacena en el equipo cliente en el almacén de licencias local, que es un archivo protegido que contiene licencias y otros datos DRM. Cuando una aplicación tiene acceso al contenido protegido, el subsistema DRM busca en el almacén de licencias local una licencia que conceda el derecho adecuado. Si no se encuentra ninguna licencia, la aplicación puede adquirir una según la información almacenada en el encabezado DRM del archivo.

Se pueden emitir varias licencias para el mismo archivo protegido. Cuando el subsistema DRM determina si se permite una acción, agrega los derechos de todas las licencias que se aplican. A cada licencia se le puede asignar una prioridad. Si se aplica más de una licencia a una acción, se comprueba la licencia de prioridad más alta para determinar si es necesario disminuir los recuentos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




