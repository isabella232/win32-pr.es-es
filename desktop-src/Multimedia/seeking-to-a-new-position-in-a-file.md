---
title: Buscar en una nueva posición en un archivo
description: Buscar en una nueva posición en un archivo
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- e/s de archivos multimedia, desplazarse al principio de los archivos
- e/s de archivos, mover al principio de los archivos
- entrada y salida (e/s), desplazarse al principio de los archivos
- E/s (entrada y salida), desplazarse al principio de los archivos
- desplazarse al principio de los archivos de e/s
- e/s de archivos multimedia, buscando nueva posición en archivos
- e/s de archivos, buscando nueva posición en archivos
- entrada y salida (e/s), buscando nueva posición en archivos
- E/s (entrada y salida), buscando nueva posición en archivos
- buscar nueva posición en archivos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949ca3e9d118fdd83e5b53ae9336ad8ab601c64b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358819"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Buscar en una nueva posición en un archivo

En el ejemplo siguiente se mueve al principio de un archivo abierto mediante la función [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



En el ejemplo siguiente se desplaza al final de un archivo abierto.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



En el ejemplo siguiente se mueve a una posición de 10 bytes desde el final de un archivo abierto.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 