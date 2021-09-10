---
title: Realización de E/S de archivos de memoria
description: Realización de E/S de archivos de memoria
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- E/S de archivos multimedia, memoria
- E/S de archivo, memoria
- entrada y salida (E/S),memoria
- E/S (entrada y salida),memoria
- E/S de memoria
- Función mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371822"
---
# <a name="performing-memory-file-io"></a>Realización de E/S de archivos de memoria

Los servicios de E/S de archivos multimedia permiten tratar un bloque de memoria como un archivo. Esto puede ser útil si ya tiene una imagen de archivo en memoria. Los archivos de memoria permiten reducir el número de condiciones de casos especiales en el código porque, para fines de E/S, puede tratar los archivos de memoria como si fueran archivos basados en disco. También puede usar archivos de memoria con el Portapapeles.

Al igual que con los búferes de E/S, los archivos de memoria pueden usar memoria asignada por la aplicación o por el administrador de E/S de archivos. Además, los archivos de memoria pueden ser expandibles o no ampliables. Cuando el administrador de E/S de archivo llega al final de un archivo de memoria expandible, expande el archivo de memoria mediante un incremento predefinido.

Para abrir un archivo de memoria, use la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) con el parámetro *szFilename* establecido en **NULL** y la marca MMIO READWRITE establecida en el \_ parámetro *dwOpenFlags.* Establezca el *parámetro lpmmioinfo* para que apunte a una [**estructura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) que se ha configurado de la siguiente manera:

1.  Establezca el **miembro pIOProc** en **NULL.**
2.  Establezca el **miembro fccIOProc** en FOURCC \_ MEM.
3.  Establezca el **miembro pchBuffer** para que apunte al bloque de memoria. Para solicitar que el administrador de E/S de archivo asigne el bloque de memoria, **establezca pchBuffer** en **NULL.**
4.  Establezca el **miembro cchBuffer** en el tamaño inicial del bloque de memoria.
5.  Establezca el **miembro adwInfo** en el tamaño mínimo de expansión del bloque de memoria. Para un archivo de memoria no explorable, establezca **adwInfo** en **NULL.**
6.  Establezca todos los demás miembros en cero.

No hay restricciones en la asignación de memoria para su uso como un archivo de memoria no explorable.

 

 