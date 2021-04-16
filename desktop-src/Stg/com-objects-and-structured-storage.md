---
title: Objetos COM y almacenamiento estructurado
description: Uno de los usos actuales más comunes de las propiedades persistentes es utilizarlos para almacenar datos sobre un objeto del sistema, como un documento, con ese objeto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Objetos COM y almacenamiento estructurado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472a3d2fb9c145538bbd6b5e87dfcc9523feff78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418434"
---
# <a name="com-objects-and-structured-storage"></a>Objetos COM y almacenamiento estructurado

Uno de los usos actuales más comunes de las propiedades persistentes es utilizarlos para almacenar datos sobre un objeto del sistema, como un documento, con ese objeto. Por supuesto, existe la posibilidad de almacenar propiedades con cualquier objeto, como una impresora, por lo que solo sería necesario examinar sus propiedades para determinar su ubicación, su tipo, etc. Un objeto de usuario podría tener un conjunto de propiedades que incluye datos como el nombre, el apellido, la oficina y el teléfono. Las aplicaciones pueden escribirse para consultar un conjunto de objetos en todo el sistema en función de sus propiedades, por ejemplo, para mostrar todas las impresoras ubicadas en un determinado edificio. Los sistemas actuales, sin embargo, suelen usar las propiedades en los documentos.

El estándar del conjunto de propiedades principal definido por COM es [el conjunto de propiedades de información de Resumen](the-summary-information-property-set.md). Esta propiedad establecida es sencilla y se utiliza normalmente. La mayoría de los documentos creados por las aplicaciones tienen un conjunto común de atributos útiles para los usuarios de esos documentos. Estos atributos incluyen el nombre del autor del documento, el asunto del documento, Cuándo se creó, etc. Se han definido otros dos conjuntos de propiedades para Microsoft Office 95, Office 97 y versiones posteriores. Se trata del conjunto de propiedades de resumen del documento COM y del conjunto de propiedades User-Defined propiedades. Para obtener más información, consulte [formato del conjunto de propiedades serializado de almacenamiento estructurado](structured-storage-serialized-property-set-format.md).

En Windows 3,1, cada aplicación tenía una manera diferente de almacenar estos datos en sus documentos. Para examinar la información de Resumen de un documento determinado, el usuario tenía que ejecutar la aplicación que creó el documento, abrirlo e invocar el cuadro de diálogo información de Resumen de la aplicación, por lo que solo la aplicación podría mostrar su información de resumen.

Los conjuntos de propiedades COM y las interfaces de conjunto de propiedades permiten ver las propiedades del documento sin ejecutar la aplicación de creación. Por ejemplo, todas las versiones de Microsoft Word 6,0 o posterior, y muchas otras aplicaciones habilitadas para COM ahora guardan sus documentos mediante el almacenamiento estructurado COM y el estándar de conjunto de propiedades que se describe aquí. Por lo tanto, otras aplicaciones del conjunto de aplicaciones de Office pueden mostrar [el conjunto de propiedades de información de Resumen](the-summary-information-property-set.md) para este tipo de archivo, siempre que el archivo sea un archivo de almacenamiento estructurado com y la aplicación de creación guarde la información en el formato del conjunto de propiedades com. El shell de Windows 95 o Windows 98, por ejemplo, lo utiliza y permite al usuario final ver las propiedades de cualquier documento de Word 6,0 o posterior directamente desde el shell.

Para usar conjuntos de propiedades de otras aplicaciones, las demás aplicaciones deben reconocer cómo interpretar las propiedades dentro de un conjunto de propiedades, lo que implica un estándar. COM ha pionero en este enfoque definiendo un conjunto de propiedades estándar, el conjunto de propiedades de información de Resumen de COM. Cualquier aplicación que tenga la definición de este conjunto de propiedades puede tener acceso fácilmente a la información de Resumen contenida en cualquier documento creado por una aplicación COM que use esa especificación de conjunto de propiedades.

 

 




