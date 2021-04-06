---
title: Crear un fragmento RIFF
description: Crear un fragmento RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- e/s de archivos multimedia, crear un fragmento RIFF
- e/s de archivos, crear un fragmento RIFF
- entrada y salida (e/s), crear un fragmento RIFF
- E/s (entrada y salida), crear un fragmento RIFF
- crear un fragmento RIFF
- mmioCreateChunk función)
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
- Fragmento RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904555"
---
# <a name="creating-a-riff-chunk"></a>Crear un fragmento RIFF

En el ejemplo siguiente se usa la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) para crear un fragmento con un identificador de fragmento "Riff" y un tipo de formulario "RDIB".


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Si va a crear un fragmento "RIFF" o "LIST", debe especificar el tipo de formulario o de lista en el miembro **fccType** de la estructura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) . En el ejemplo anterior, "RDIB" es el tipo de formulario.

Si conoce el tamaño del campo de datos en un nuevo fragmento, puede establecer el miembro **cksize** de la estructura **MMCKINFO** al crear el fragmento. Este valor se escribirá en el campo tamaño de los datos del nuevo fragmento. Si este valor no es correcto cuando se llama a [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) para marcar el final del fragmento, se reescribirá automáticamente para reflejar el tamaño correcto del campo de datos.

Después de crear un fragmento mediante la función [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la posición del archivo se establece en el campo de datos del fragmento (8 bytes desde el principio del fragmento). Si el fragmento es un fragmento "RIFF" o "LIST", la posición del archivo se establece en la ubicación que sigue al tipo de formulario o tipo de lista (12 bytes desde el principio del fragmento).

 

 