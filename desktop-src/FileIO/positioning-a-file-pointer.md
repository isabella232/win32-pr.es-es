---
description: Windows un puntero de archivo para realizar un seguimiento de los bytes leídos o escritos.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Colocar un puntero de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069871"
---
# <a name="positioning-a-file-pointer"></a>Colocar un puntero de archivo

Cuando una aplicación llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un archivo [](file-pointers.md) por primera vez, Windows el puntero de archivo al principio del archivo. A medida que los bytes se leen o se escriben en el archivo, Windows el puntero de archivo el número de bytes leídos o escritos.

Una aplicación puede colocar el puntero de archivo en un desplazamiento especificado llamando a [**SetFilePointer.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)

La [**función SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) también se puede usar para consultar la posición del puntero de archivo actual especificando un método de movimiento **de FILE \_ CURRENT** y una distancia de cero.

 

 



