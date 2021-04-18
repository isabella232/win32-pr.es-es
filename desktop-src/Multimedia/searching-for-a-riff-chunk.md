---
title: Buscar un fragmento RIFF
description: Buscar un fragmento RIFF
ms.assetid: ce974fb3-3af0-4400-8f55-65d63627592a
keywords:
- e/s de archivos multimedia, buscar un fragmento RIFF
- e/s de archivos, buscar un fragmento RIFF
- entrada y salida (e/s), buscar fragmentos RIFF
- E/s (entrada y salida), buscar fragmentos RIFF
- buscando fragmento RIFF
- formato de archivo de intercambio de recursos (RIFF)
- RIFF (formato de archivo de intercambio de recursos)
- RIFF E/S
- Fragmento RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b45b2182e44ac84423c29a79fe29e96820d5bf2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420718"
---
# <a name="searching-for-a-riff-chunk"></a>Buscar un fragmento RIFF

En el ejemplo siguiente se usa la función [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend) para buscar un fragmento "Riff" con un tipo de formulario "Wave" para comprobar que el archivo que se acaba de abrir es un archivo de audio de forma de onda.


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



 

 