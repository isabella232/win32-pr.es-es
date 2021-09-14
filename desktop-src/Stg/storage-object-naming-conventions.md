---
title: Storage Convenciones de nomenclatura de objetos
description: Storage y los objetos de secuencia se denominan según un conjunto de convenciones.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Structured Storage Strctd Stg ,fundamentals,storage object naming conventions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073538"
---
# <a name="storage-object-naming-conventions"></a>Storage Convenciones de nomenclatura de objetos

Storage y los objetos de secuencia se denominan según un conjunto de convenciones.

El nombre de un objeto de almacenamiento raíz es el nombre real del archivo en el sistema de archivos subyacente. Se ajusta a las convenciones y restricciones que impone el sistema de archivos. Las cadenas de nombre de archivo que se pasan a funciones y métodos relacionados con el almacenamiento se pasan, sin interpretar y sin modificar, al sistema de archivos.

El nombre de un elemento anidado incluido dentro de un objeto de almacenamiento se administra mediante la implementación del objeto de almacenamiento determinado. Todas las implementaciones de objetos de almacenamiento deben admitir nombres de elementos anidados de 32 caracteres de longitud (incluido el terminador **NULL),** aunque algunas implementaciones pueden admitir nombres más largos. Si el objeto de almacenamiento realiza alguna conversión de mayúsculas y minúsculas está definido por la implementación. Como resultado, las aplicaciones que definen nombres de elementos deben elegir nombres que sean aceptables independientemente de si se realiza o no la conversión de mayúsculas y minúsculas. La implementación COM de archivos compuestos admite nombres con una longitud máxima de 32 caracteres y no realiza ninguna conversión de mayúsculas y minúsculas.

 

 




