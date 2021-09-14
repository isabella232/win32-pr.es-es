---
title: Crear y eliminar un archivo
description: Crear y eliminar un archivo
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- E/S de archivos multimedia, crear archivos
- E/S de archivo, crear archivos
- entrada y salida (E/S), creación de archivos
- E/S (entrada y salida), creación de archivos
- crear archivos de E/S
- E/S de archivos multimedia, eliminar archivos
- E/S de archivo, eliminar archivos
- entrada y salida (E/S), eliminar archivos
- E/S (entrada y salida), eliminar archivos
- eliminar archivos de E/S
- Función mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071770"
---
# <a name="creating-and-deleting-a-file"></a>Crear y eliminar un archivo

Para crear un archivo, establezca el *parámetro dwOpenFlags* de la [**función mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) en MMIO \_ CREATE. En el ejemplo siguiente se crea un archivo y se abre para leer y escribir.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Si el archivo que está creando ya existe, se truncará a una longitud cero.

Para eliminar un archivo, establezca el *parámetro dwOpenFlags* de la **función mmioOpen** en MMIO \_ DELETE. Después de eliminar un archivo, no se puede recuperar por ningún medio estándar. Si la aplicación elimina un archivo a petición de un usuario, consulte al usuario antes de eliminarlo para asegurarse de que el usuario desea eliminarlo.

 

 