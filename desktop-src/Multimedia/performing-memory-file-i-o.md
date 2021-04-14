---
title: Realizar e/s de archivos de memoria
description: Realizar e/s de archivos de memoria
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de archivos multimedia, memoria
- e/s de archivos, memoria
- entrada y salida (e/s), memoria
- E/s (entrada y salida), memoria
- e/s de memoria
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487538"
---
# <a name="performing-memory-file-io"></a>Realizar e/s de archivos de memoria

Los servicios de e/s de archivos multimedia permiten tratar un bloque de memoria como un archivo. Esto puede ser útil si ya tiene una imagen de archivo en memoria. Los archivos de memoria permiten reducir el número de condiciones especiales en el código, ya que, con fines de e/s, puede tratar los archivos de memoria como si fueran archivos basados en disco. También puede usar archivos de memoria con el portapapeles.

Al igual que con los búferes de e/s, los archivos de memoria pueden usar la memoria asignada por la aplicación o por el administrador de e/s de archivos. Además, los archivos de memoria pueden ser expansibles o no expansibles. Cuando el administrador de e/s de archivos alcanza el final de un archivo de memoria expansible, expande el archivo de memoria por un incremento predefinido.

Para abrir un archivo de memoria, use la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) con el parámetro *SzFilename* establecido en **null** y la \_ marca ReadWrite de MMIO establecida en el parámetro *dwOpenFlags* . Establezca el parámetro *lpmmioinfo* para que apunte a una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) que se ha configurado de la siguiente manera:

1.  Establezca el miembro **pIOProc** en **null**.
2.  Establezca el miembro **fccIOProc** en el valor de \_ MEM.
3.  Establezca el miembro **pchBuffer** para que apunte al bloque de memoria. Para solicitar que el administrador de e/s de archivos asigne el bloque de memoria, establezca **pchBuffer** en **null**.
4.  Establezca el miembro **cchBuffer** en el tamaño inicial del bloque de memoria.
5.  Establezca el miembro **adwInfo** en el tamaño mínimo de expansión del bloque de memoria. Para un archivo de memoria no expansible, establezca **adwInfo** en **null**.
6.  Establezca el resto de miembros en cero.

No hay restricciones en la asignación de memoria para su uso como archivo de memoria no expansible.

 

 