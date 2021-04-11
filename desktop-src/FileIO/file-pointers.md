---
description: Un puntero de archivo es un valor de desplazamiento de 64 bits que especifica el siguiente byte que se va a leer o la ubicación en la que se va a recibir el siguiente byte escrito.
ms.assetid: 1e8bc657-affa-4a17-8435-c93de5075a1d
title: Punteros de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4fc804711665c045361d40c69fb71a4959b4c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276186"
---
# <a name="file-pointers"></a>Punteros de archivo

Cuando se abre un archivo, Windows asocia un *puntero de archivo* a la secuencia predeterminada. Este puntero de archivo es un valor de desplazamiento de 64 bits que especifica el siguiente byte que se va a leer o la ubicación para recibir el siguiente byte escrito. Cada vez que se abre un archivo, el sistema coloca el puntero de archivo al principio del archivo, que es el desplazamiento de cero. Cada operación de lectura y escritura hace avanzar el puntero de archivo por el número de bytes que se leen y se escriben. Por ejemplo, si el puntero de archivo está al principio del archivo y se solicita una operación de lectura de 5 bytes, el puntero de archivo se ubicará en el desplazamiento 5 inmediatamente después de la operación de lectura. A medida que se lee o escribe cada byte, el sistema hace avanzar el puntero de archivo. También se puede cambiar la posición del puntero de archivo mediante una llamada a la función [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .

Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leer el archivo, no se produce ningún error, pero no se lee ningún byte. Por lo tanto, la lectura de cero bytes sin un error significa que la aplicación ha alcanzado el final del archivo. La escritura de cero bytes no hace nada.

Una aplicación puede truncar o extender un archivo mediante la función [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) . Esta función establece el final del archivo en la posición actual del puntero de archivo.

 

 



