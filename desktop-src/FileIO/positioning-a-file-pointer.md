---
description: Windows usa un puntero de archivo para hacer un seguimiento de los bytes leídos o escritos.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Colocar un puntero de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687538"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="ef379-103">Colocar un puntero de archivo</span><span class="sxs-lookup"><span data-stu-id="ef379-103">Positioning a File Pointer</span></span>

<span data-ttu-id="ef379-104">Cuando una aplicación llama a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) para abrir un archivo por primera vez, Windows coloca el [puntero de archivo](file-pointers.md) al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="ef379-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="ef379-105">A medida que los bytes se leen o se escriben en el archivo, Windows desplaza el puntero de archivo el número de bytes leídos o escritos.</span><span class="sxs-lookup"><span data-stu-id="ef379-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="ef379-106">Una aplicación puede colocar el puntero de archivo en un desplazamiento especificado llamando a [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span><span class="sxs-lookup"><span data-stu-id="ef379-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="ef379-107">La función [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) también se puede usar para consultar la posición del puntero de archivo actual mediante la especificación de un método de movimiento de **archivo \_ actual** y una distancia de cero.</span><span class="sxs-lookup"><span data-stu-id="ef379-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



