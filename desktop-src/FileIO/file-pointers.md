---
description: Un puntero de archivo es un valor de desplazamiento de 64 bits que especifica el byte siguiente que se va a leer o la ubicación en la que se va a recibir el byte siguiente escrito.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Punteros de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069949"
---
# <a name="file-pointers"></a>Punteros de archivo

Cuando se abre un archivo, Windows asocia un puntero de *archivo* a la secuencia predeterminada. Este puntero de archivo es un valor de desplazamiento de 64 bits que especifica el byte siguiente que se va a leer o la ubicación en la que se va a recibir el byte siguiente escrito. Cada vez que se abre un archivo, el sistema coloca el puntero de archivo al principio del archivo, que es el desplazamiento cero. Cada operación de lectura y escritura avanza el puntero de archivo según el número de bytes que se leen y escriben. Por ejemplo, si el puntero de archivo está al principio del archivo y se solicita una operación de lectura de 5 bytes, el puntero de archivo se ubicará en el desplazamiento 5 inmediatamente después de la operación de lectura. A medida que se lee o escribe cada byte, el sistema avanza el puntero de archivo. El puntero de archivo también se puede cambiar de posición llamando a la [**función SetFilePointer.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)

Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leerlo, no se produce ningún error, pero no se leen bytes. Por lo tanto, leer cero bytes sin un error significa que la aplicación ha llegado al final del archivo. Escribir cero bytes no hace nada.

Una aplicación puede truncar o extender un archivo mediante la [**función SetEndOfFile.**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) Esta función establece el final del archivo en la posición actual del puntero de archivo.

 

 



