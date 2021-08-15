---
title: Servicios de formato de archivo de intercambio de recursos
description: Servicios de formato de archivo de intercambio de recursos
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- E/S de archivos multimedia, formato de archivo de intercambio de recursos (RIFF)
- E/S de archivo, formato de archivo de intercambio de recursos (RIFF)
- entrada y salida (E/S), formato de archivo de intercambio de recursos (RIFF)
- E/S (entrada y salida), formato de archivo de intercambio de recursos (RIFF)
- Función mmioOpen
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
- Fragmento de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5967165996b2a7fb9ed9b40c9a1f3c5608cd3bb4eb1e6cf05ae351f6ce6f2a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801937"
---
# <a name="resource-interchange-file-format-services"></a>Servicios de formato de archivo de intercambio de recursos

El formato preferido para los archivos multimedia es el formato de archivo de intercambio de recursos (RIFF). Las funciones de E/S de archivo RIFF funcionan con los servicios básicos de E/S de archivos almacenados en búfer y sin búfer. Puede abrir, leer y escribir archivos RIFF de la misma manera que otros tipos de archivo. Para obtener información detallada sobre RIFF, vea [Funciones y macros de AVIFile.](avifile-functions-and-macros.md)

Los archivos RIFF usan códigos de cuatro caracteres para identificar elementos de archivo. Estos códigos son cantidades de 32 bits que representan una secuencia de uno a cuatro caracteres alfanuméricos ASCII, que se agregan a la derecha con caracteres de espacio. El tipo de datos de los códigos de cuatro caracteres **es FOURCC.** Use la [**macro mmioFOURCC para**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) convertir cuatro caracteres en un código de cuatro caracteres. Para convertir una cadena terminada en NULL en un código de cuatro caracteres, use la [**función mmioStringToFOURCC.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

El bloque de creación básico de un archivo RIFF es un *fragmento*. Un fragmento es una unidad lógica de datos multimedia, como un único fotograma en un clip de vídeo. Cada fragmento contiene los siguientes campos:

-   Código de cuatro caracteres que especifica el identificador de fragmento
-   Valor doubleword que especifica el tamaño del miembro de datos en el fragmento
-   Un campo de datos

En la ilustración siguiente se muestra un fragmento "RIFF" que contiene dos subchunks.

![Fragmento de riff que contiene dos imágenes de subchunks](images/mmio1.gif)

Un fragmento contenido en otro fragmento es *un subchunk*. Los únicos fragmentos permitidos para contener subchunks son aquellos con un identificador de fragmento de "RIFF" o "LIST". Un fragmento que contiene otro fragmento se denomina *fragmento primario*. El primer fragmento de un archivo RIFF debe ser un fragmento "RIFF". Todos los demás fragmentos del archivo son subchunks del fragmento "RIFF".

Los fragmentos "RIFF" incluyen un campo adicional en los cuatro primeros bytes del campo de datos. Este campo adicional proporciona el *tipo de formulario* del campo. El tipo de formulario es un código de cuatro caracteres que identifica el formato de los datos almacenados en el archivo. Por ejemplo, los archivos de audio de forma de onda de Microsoft tienen un tipo de formulario "WAVE".

Los fragmentos "LIST" también incluyen un campo adicional en los cuatro primeros bytes del campo de datos. Este campo adicional contiene el *tipo de lista* del campo. El tipo de lista es un código de cuatro caracteres que identifica el contenido de la lista. Por ejemplo, un fragmento "LIST" con un tipo de lista de "INFO" puede contener fragmentos "ICOP" e "ICRD" que proporcionan información de fecha de creación y copyright. En la ilustración siguiente se muestra un fragmento "RIFF" que contiene un fragmento "LIST" y otro subchunk (el fragmento "LIST" contiene dos subchunks).

![Fragmento de riff que contiene una imagen de fragmento de lista](images/mmio2.gif)

Los servicios de E/S de archivos multimedia incluyen dos funciones que puede usar para navegar entre fragmentos en un archivo RIFF: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) y [**mmioDescend.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) Puede usar estas funciones como funciones de búsqueda de alto nivel. Cuando se baja a un fragmento, la posición del archivo se establece en el campo de datos del fragmento (8 bytes desde el principio del fragmento). Para los fragmentos "RIFF" y "LIST", la posición del archivo se establece en la ubicación que sigue al tipo de formulario o al tipo de lista (12 bytes desde el principio del fragmento). Cuando se sale de un fragmento, la posición del archivo se establece en la ubicación que sigue al final del fragmento.

Para crear un fragmento, use la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para escribir un encabezado de fragmento en la posición actual en un archivo abierto. Las **funciones mmioAscend,** **mmioDescend** y **mmioCreateChunk** usan la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) para especificar y recuperar información sobre los fragmentos "RIFF".

 

 