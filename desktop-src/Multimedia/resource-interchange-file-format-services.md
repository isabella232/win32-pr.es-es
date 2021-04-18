---
title: Servicios de formato de archivo de intercambio de recursos
description: Servicios de formato de archivo de intercambio de recursos
ms.assetid: 8526794b-7b40-470f-94f7-935d7dbf9151
keywords:
- e/s de archivos multimedia, formato de archivo de intercambio de recursos (RIFF)
- e/s de archivos, formato de archivo de intercambio de recursos (RIFF)
- entrada y salida (e/s), formato de archivo de intercambio de recursos (RIFF)
- E/s (entrada y salida), formato de archivo de intercambio de recursos (RIFF)
- mmioOpen función)
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
- Fragmento RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cca3792ccded248951065c7b69f2e50d27e0ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358822"
---
# <a name="resource-interchange-file-format-services"></a>Servicios de formato de archivo de intercambio de recursos

El formato preferido para los archivos multimedia es el formato de archivo de intercambio de recursos (RIFF). Las funciones de e/s de archivos RIFF funcionan con los servicios de e/s de archivos almacenados en búfer y no almacenados en búfer. Puede abrir, leer y escribir archivos RIFF de la misma manera que otros tipos de archivo. Para obtener información detallada sobre RIFF, vea [AVIFile Functions and macros](avifile-functions-and-macros.md).

Los archivos RIFF usan códigos de cuatro caracteres para identificar los elementos de archivo. Estos códigos son cantidades de 32 bits que representan una secuencia de uno a cuatro caracteres ASCII alfanuméricos, que se rellenan a la derecha con caracteres de espacio. El tipo de datos para códigos de cuatro caracteres es **FourCC**. Use la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) para convertir cuatro caracteres en un código de cuatro caracteres. Para convertir una cadena terminada en null en un código de cuatro caracteres, utilice la función [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) .

El bloque de creación básico de un archivo RIFF es un *fragmento*. Un fragmento es una unidad lógica de datos multimedia, como un solo fotograma en un clip de vídeo. Cada fragmento contiene los campos siguientes:

-   Un código de cuatro caracteres que especifica el identificador de fragmento
-   Un valor palabra que especifica el tamaño del miembro de datos del fragmento.
-   Un campo de datos

En la ilustración siguiente se muestra un fragmento "RIFF" que contiene dos subfragmentos.

![fragmento riff que contiene dos imágenes de subfragmentos](images/mmio1.gif)

Un fragmento contenido en otro fragmento es un *subfragmento*. Los únicos fragmentos que pueden contener subfragmentos son aquellos con un identificador de fragmento "RIFF" o "LIST". Un fragmento que contiene otro fragmento se denomina un *fragmento primario*. El primer fragmento de un archivo RIFF debe ser un fragmento "RIFF". Todos los demás fragmentos del archivo son subfragmentos del fragmento "RIFF".

Los fragmentos "RIFF" incluyen un campo adicional en los cuatro primeros bytes del campo de datos. Este campo adicional proporciona el *tipo de formulario* del campo. El tipo de formulario es un código de cuatro caracteres que identifica el formato de los datos almacenados en el archivo. Por ejemplo, los archivos de audio de forma de onda de Microsoft tienen un tipo de formulario "WAVE".

Los fragmentos de "lista" también incluyen un campo adicional en los cuatro primeros bytes del campo de datos. Este campo adicional contiene el *tipo de lista* del campo. El tipo de lista es un código de cuatro caracteres que identifica el contenido de la lista. Por ejemplo, un fragmento "LIST" con un tipo de lista "INFO" puede contener fragmentos "ICOP" y "ICRD" que proporcionan información sobre los derechos de autor y la fecha de creación. En la ilustración siguiente se muestra un fragmento "RIFF" que contiene un fragmento "LIST" y otro subfragmento (el fragmento "LIST" contiene dos subfragmentos).

![fragmento riff que contiene una imagen de fragmento de lista](images/mmio2.gif)

Los servicios de e/s de archivos multimedia incluyen dos funciones que puede usar para navegar entre fragmentos en un archivo RIFF: [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) y [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend). Puede usar estas funciones como funciones de búsqueda de alto nivel. Cuando desciende en un fragmento, la posición del archivo se establece en el campo de datos del fragmento (8 bytes desde el principio del fragmento). En el caso de los fragmentos "RIFF" y "LIST", la posición del archivo se establece en la ubicación que sigue al tipo de formulario o tipo de lista (12 bytes desde el principio del fragmento). Cuando se encuentra en orden ascendente de un fragmento, la posición del archivo se establece en la ubicación que sigue al final del fragmento.

Para crear un fragmento nuevo, utilice la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para escribir un encabezado de fragmentos en la posición actual de un archivo abierto. Las funciones **mmioAscend**, **mmioDescend** y **mmioCreateChunk** usan la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) para especificar y recuperar información sobre fragmentos "Riff".

 

 