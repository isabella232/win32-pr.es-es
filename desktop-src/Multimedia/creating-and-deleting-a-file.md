---
title: Crear y eliminar un archivo
description: Crear y eliminar un archivo
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- e/s de archivos multimedia, crear archivos
- e/s de archivos, crear archivos
- entrada y salida (e/s), crear archivos
- E/s (entrada y salida), crear archivos
- crear archivos de e/s
- e/s de archivos multimedia, eliminar archivos
- e/s de archivos, eliminar archivos
- entrada y salida (e/s), eliminar archivos
- E/s (entrada y salida), eliminar archivos
- eliminar archivos de e/s
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790179"
---
# <a name="creating-and-deleting-a-file"></a>Crear y eliminar un archivo

Para crear un archivo, establezca el parámetro *dwOpenFlags* de la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) en MMIO \_ Create. En el ejemplo siguiente se crea un archivo y se abre para lectura y escritura.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Si el archivo que está creando ya existe, se truncará a longitud cero.

Para eliminar un archivo, establezca el parámetro *dwOpenFlags* de la función **mmioOpen** en la \_ eliminación MMIO. Después de eliminar un archivo, no se puede recuperar por ningún medio estándar. Si la aplicación elimina un archivo en la solicitud de un usuario, consulte al usuario antes de eliminar el archivo para asegurarse de que el usuario desea eliminarlo.

 

 