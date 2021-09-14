---
title: Buscar una nueva posición en un archivo
description: Buscar una nueva posición en un archivo
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- E/S de archivos multimedia, pasar al principio de los archivos
- E/S de archivo, pasar al principio de los archivos
- entrada y salida (E/S), pasar al principio de los archivos
- E/S (entrada y salida), pasar al principio de los archivos
- mover al principio de los archivos de E/S
- E/S de archivos multimedia, buscar nueva posición en los archivos
- E/S de archivo, buscar nueva posición en los archivos
- entrada y salida (E/S), buscar nueva posición en los archivos
- E/S (entrada y salida), buscar nueva posición en los archivos
- buscar nueva posición en los archivos de E/S
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173613"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Buscar una nueva posición en un archivo

En el ejemplo siguiente se mueve al principio de un archivo abierto mediante la [**función mmioSeek.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



En el ejemplo siguiente se mueve al final de un archivo abierto.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



En el ejemplo siguiente se mueve a una posición de 10 bytes desde el final de un archivo abierto.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 