---
title: Creación de un fragmento de RIFF
description: Creación de un fragmento de RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- E/S de archivos multimedia, creación de fragmentos de RIFF
- E/S de archivo, crear fragmento de RIFF
- entrada y salida (E/S), creación de fragmentos de RIFF
- E/S (entrada y salida), creación de fragmentos de RIFF
- crear fragmento de RIFF
- Función mmioCreateChunk
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
- Fragmento de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01130a34759d8445913704a37406d93a1bbce0b8ad714f4467783e4b3a63b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144738"
---
# <a name="creating-a-riff-chunk"></a>Creación de un fragmento de RIFF

En el ejemplo siguiente se usa la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para crear un fragmento con un identificador de fragmento de "RIFF" y un tipo de formulario de "RDIB".


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Si va a crear un fragmento "RIFF" o "LIST", debe especificar el tipo de formulario o el tipo de lista en el miembro **fccType** de la [**estructura MMCKINFO.**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) En el ejemplo anterior, "RDIB" es el tipo de formulario.

Si conoce el tamaño del campo de datos en un nuevo fragmento, puede establecer el miembro **cksize** de la estructura **MMCKINFO** al crear el fragmento. Este valor se escribirá en el campo de tamaño de datos del nuevo fragmento. Si este valor no es correcto cuando se llama a [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) para marcar el final del fragmento, se reescribe automáticamente para reflejar el tamaño correcto del campo de datos.

Después de crear un fragmento mediante la función [**mmioCreateChunk,**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) la posición del archivo se establece en el campo de datos del fragmento (8 bytes desde el principio del fragmento). Si el fragmento es un fragmento "RIFF" o "LIST", la posición del archivo se establece en la ubicación siguiente al tipo de formulario o tipo de lista (12 bytes desde el principio del fragmento).

 

 