---
title: Búsqueda de un fragmento de RIFF
description: Búsqueda de un fragmento de RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- E/S de archivos multimedia, buscar fragmento de RIFF
- E/S de archivo, buscar fragmento de RIFF
- entrada y salida (E/S), buscar fragmento de RIFF
- E/S (entrada y salida), buscar fragmento de RIFF
- buscar fragmento de RIFF
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- E/S de RIFF
- Fragmento de RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbb09c7777cf675ceb0f11ae84fb50a3b9deaa73910ca9e15280c3fb88c42cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782095"
---
# <a name="searching-for-a-riff-chunk"></a>Búsqueda de un fragmento de RIFF

En el ejemplo siguiente se usa la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para buscar un fragmento "RIFF" con un tipo de formulario "WAVE" para comprobar que el archivo que se acaba de abrir es un archivo de audio de forma de onda.


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfoParent; 
MMCKINFO mmckinfoSubchunk; 
. 
. 
. 
// Locate a "RIFF" chunk with a "WAVE" form type to make 
// sure the file is a waveform-audio file. 
mmckinfoParent.fccType = mmioFOURCC('W', 'A', 'V', 'E'); 
if (mmioDescend(hmmio, (LPMMCKINFO) &mmckinfoParent, NULL, 
    MMIO_FINDRIFF)) 
    // The file is not a waveform-audio file. 
else 
    // The file is a waveform-audio file 

```



 

 