---
title: Storage Convenciones de nomenclatura de objetos
description: Storage y los objetos de flujo se denominan según un conjunto de convenciones.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Convenciones Storage de nomenclatura de objetos de almacenamiento, fundamentales y Stg Strctd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acebeabfbd5ba41a66ee102d2939498064fc3d852d29db4ce54cfd18878eda94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960204"
---
# <a name="storage-object-naming-conventions"></a>Storage Convenciones de nomenclatura de objetos

Storage y los objetos de flujo se denominan según un conjunto de convenciones.

El nombre de un objeto de almacenamiento raíz es el nombre real del archivo en el sistema de archivos subyacente. Se ajusta a las convenciones y restricciones que impone el sistema de archivos. Las cadenas de nombre de archivo que se pasan a funciones y métodos relacionados con el almacenamiento se pasan, sin interpretar y sin modificar, al sistema de archivos.

El nombre de un elemento anidado contenido en un objeto de almacenamiento se administra mediante la implementación del objeto de almacenamiento concreto. Todas las implementaciones de objetos de almacenamiento deben admitir nombres de elementos anidados de 32 caracteres de longitud (incluido el terminador **NULL),** aunque algunas implementaciones pueden admitir nombres más largos. Si el objeto de almacenamiento realiza alguna conversión de mayúsculas y minúsculas está definido por la implementación. Como resultado, las aplicaciones que definen nombres de elementos deben elegir nombres que sean aceptables independientemente de si se realiza o no la conversión de mayúsculas y minúsculas. La implementación COM de archivos compuestos admite nombres con una longitud máxima de 32 caracteres y no realiza ninguna conversión de mayúsculas y minúsculas.

 

 




