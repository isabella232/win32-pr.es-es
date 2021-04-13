---
title: Convenciones de nomenclatura de objetos de almacenamiento
description: Los nombres de los objetos de flujo y de almacenamiento se asignan según un conjunto de convenciones.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Strctd de almacenamiento estructurado STG, aspectos básicos y convenciones de nomenclatura de objetos de almacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418441"
---
# <a name="storage-object-naming-conventions"></a>Convenciones de nomenclatura de objetos de almacenamiento

Los nombres de los objetos de flujo y de almacenamiento se asignan según un conjunto de convenciones.

El nombre de un objeto de almacenamiento raíz es el nombre real del archivo en el sistema de archivos subyacente. Se ajusta a las convenciones y restricciones que impone el sistema de archivos. Las cadenas de nombre de archivo que se pasan a los métodos y funciones relacionados con el almacenamiento se pasan al sistema de archivos, no se interpretan y sin modificar.

El nombre de un elemento anidado contenido dentro de un objeto de almacenamiento se administra mediante la implementación del objeto de almacenamiento determinado. Todas las implementaciones de objetos de almacenamiento deben admitir nombres de elementos anidados 32 caracteres de longitud (incluido el terminador **null** ), aunque algunas implementaciones podrían admitir nombres más largos. Si el objeto de almacenamiento realiza una conversión de mayúsculas y minúsculas definida por la implementación. Como resultado, las aplicaciones que definen nombres de elementos deben elegir nombres que sean aceptables tanto si se realiza la conversión de mayúsculas o minúsculas como si no. La implementación COM de archivos compuestos admite nombres con una longitud máxima de 32 caracteres y no realiza ninguna conversión de mayúsculas y minúsculas.

 

 




