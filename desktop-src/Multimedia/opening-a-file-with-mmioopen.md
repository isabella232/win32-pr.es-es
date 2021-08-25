---
title: Abrir un archivo con mmioOpen
description: Abrir un archivo con mmioOpen
ms.assetid: 947d1b1c-ec00-4bd9-948a-4b8e3bfb84f6
keywords:
- E/S de archivos multimedia, abrir archivos
- E/S de archivo, abrir archivos
- entrada y salida (E/S), abrir archivos
- E/S (entrada y salida), abrir archivos
- E/S de archivos multimedia, función mmioOpen
- E/S de archivo, función mmioOpen
- entrada y salida (E/S),función mmioOpen
- E/S (entrada y salida),función mmioOpen
- mmioOpen ( Función)
- abrir archivos de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd323e888b181b0166572d11687d3dde66e83f0ce73541555b1f49083564ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893195"
---
# <a name="opening-a-file-with-mmioopen"></a>Abrir un archivo con mmioOpen

Para abrir un archivo para operaciones básicas de E/S, establezca el parámetro *lpmmioinfo* de la [**función mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) en **NULL.** En el ejemplo siguiente se abre un archivo denominado "C: SAMPLESSAMPLE1.TXT" para leer y se comprueba si hay error en \\ \\ el valor devuelto.


```C++
HMMIO hFile; 

if ((hFile = mmioOpen("C:\\SAMPLES\\SAMPLE1.TXT", NULL, 
    MMIO_READ)) != NULL) 
    // File opened successfully. 
else 
    // File cannot be opened. 
```



Use el *parámetro dwFlags* de **mmioOpen para** especificar marcas para abrir un archivo.

 

 