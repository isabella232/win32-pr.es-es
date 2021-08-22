---
title: Objetos COM y estructura Storage
description: Uno de los usos actuales más comunes de las propiedades persistentes es usarlos para almacenar datos sobre un objeto del sistema, como un documento, con ese objeto.
ms.assetid: 95136e9a-4c80-4704-ae65-9759487cf8f8
keywords:
- Objetos COM y estructura Storage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4c1405ddfaa060aa249090fc58b25b294a8c9aecc5f7b885d21b55bc162198
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663595"
---
# <a name="com-objects-and-structured-storage"></a>Objetos COM y estructura Storage

Uno de los usos actuales más comunes de las propiedades persistentes es usarlos para almacenar datos sobre un objeto del sistema, como un documento, con ese objeto. Por supuesto, existe la posibilidad de almacenar propiedades con cualquier objeto, como una impresora, por lo que solo sería necesario mirar sus propiedades para determinar su ubicación, su tipo, y así sucesivamente. Un objeto de usuario podría tener un conjunto de propiedades que incluye datos como nombre, apellidos, Office y Teléfono. Las aplicaciones se pueden escribir para consultar un conjunto de objetos de todo el sistema en función de sus propiedades, por ejemplo, mostrando todas las impresoras ubicadas en un determinado edificio. Sin embargo, los sistemas actuales usan con más frecuencia propiedades en documentos.

El estándar del conjunto de propiedades principal definido por COM es [El conjunto de propiedades de información de resumen](the-summary-information-property-set.md). Este conjunto de propiedades es simple y se usa con frecuencia. La mayoría de los documentos creados por aplicaciones tienen un conjunto común de atributos útiles para los usuarios de esos documentos. Estos atributos incluyen el nombre del autor del documento, el asunto del documento, cuándo se creó, y así sucesivamente. Se definen otros dos conjuntos de propiedades para Microsoft Office 95, Office 97 y versiones posteriores. Estos son el conjunto de propiedades Resumen del documento COM y el conjunto de User-Defined propiedades. Para obtener más información, vea [Structured Storage Serialized Property Set Format](structured-storage-serialized-property-set-format.md).

En Windows 3.1, cada aplicación tenía una manera diferente de almacenar estos datos en sus documentos. Para examinar la información de resumen de un documento determinado, el usuario tenía que ejecutar la aplicación que creó el documento, abrirlo e invocar el cuadro de diálogo Información de resumen de la aplicación, por lo que solo la aplicación podía mostrar su información de resumen.

Los conjuntos de propiedades COM y las interfaces del conjunto de propiedades hacen posible ver las propiedades del documento sin ejecutar la aplicación de creación. Por ejemplo, todas las versiones de Microsoft Word 6.0 o posterior, y muchas otras aplicaciones habilitadas para COM ahora guardarán sus documentos mediante el almacenamiento estructurado COM y el estándar del conjunto de propiedades descrito aquí. Por lo tanto, otras aplicaciones de [](the-summary-information-property-set.md) Office Suite pueden mostrar el conjunto de propiedades de información de resumen para este tipo de archivo, siempre que ese archivo sea un archivo de almacenamiento estructurado COM y la aplicación de creación guarde la información en el formato de conjunto de propiedades COM. El shell Windows 95 o Windows 98, por ejemplo, lo usa y permite al usuario final ver las propiedades de cualquier documento de Word 6.0 o posterior directamente desde el shell.

Para usar conjuntos de propiedades de otras aplicaciones, las demás aplicaciones deben reconocer cómo interpretar las propiedades dentro de un conjunto de propiedades, lo que implica un estándar. COM ha abordado este enfoque mediante la definición de un conjunto de propiedades estándar, el conjunto de propiedades de información de resumen COM. Cualquier aplicación que tenga la definición de este conjunto de propiedades puede acceder fácilmente a la información de resumen contenida en cualquier documento creado por una aplicación COM que use esa especificación de conjunto de propiedades.

 

 




