---
title: Licencias
description: Licencias
ms.assetid: 74717519-bfd5-4a64-88eb-680d4bdfe74a
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0fbf2d7c0a25b2b19241d90743f43f46a71d7e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357680"
---
# <a name="licenses"></a>Licencias

Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos. Cada licencia se aplica a un identificador de clave, que normalmente se asigna a un solo archivo multimedia. Este identificador es lo que se usa para identificar el contenido protegido en la licencia.

Cada licencia especifica una o varias acciones que se pueden realizar con el contenido protegido. Estas acciones, también denominadas derechos, se pueden limitar de varias maneras. Mediante la combinación de fechas de inicio, fechas de finalización, recuentos y límites de tiempo, el emisor de la licencia puede crear casi cualquier límite imaginable a la derecha.

Las licencias las emite un servicio Web. Cuando se adquiere una licencia, se almacena en el equipo cliente en el almacén de licencias local, que es un archivo protegido que contiene licencias y otros datos DRM. Cuando una aplicación tiene acceso a contenido protegido, el subsistema DRM busca en el almacén de licencias local una licencia que conceda el derecho adecuado. Si no se encuentra ninguna licencia, la aplicación puede adquirir una basada en la información almacenada en el encabezado DRM del archivo.

Se pueden emitir varias licencias para el mismo archivo protegido. Cuando el subsistema DRM determina si se permite una acción, agrega los derechos de todas las licencias que se aplican. Se puede asignar una prioridad a cada licencia. Si se aplica más de una licencia a una acción, se comprueba la licencia de prioridad más alta para determinar si es necesario disminuir el número de recuentos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Conceptos**](drmconcepts.md)
</dt> </dl>

 

 




