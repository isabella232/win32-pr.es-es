---
description: Windows un puntero de archivo para realizar un seguimiento de los bytes leídos o escritos.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Colocar un puntero de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93caefcb622f297d391aba4d695a2b0c2c2e2ca368a97c68332862a7f8bfa8a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951094"
---
# <a name="positioning-a-file-pointer"></a>Colocar un puntero de archivo

Cuando una aplicación llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un archivo por primera vez, Windows el puntero de [archivo](file-pointers.md) al principio del archivo. A medida que los bytes se leen o se escriben en el archivo, Windows el puntero de archivo el número de bytes leídos o escritos.

Una aplicación puede colocar el puntero de archivo en un desplazamiento especificado llamando a [**SetFilePointer.**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer)

La [**función SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) también se puede usar para consultar la posición del puntero de archivo actual especificando un método de movimiento **de FILE \_ CURRENT** y una distancia de cero.

 

 



