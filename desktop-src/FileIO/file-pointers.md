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
# <a name="file-pointers"></a><span data-ttu-id="c2adc-103">Punteros de archivo</span><span class="sxs-lookup"><span data-stu-id="c2adc-103">File Pointers</span></span>

<span data-ttu-id="c2adc-104">Cuando se abre un archivo, Windows asocia un *puntero de archivo* a la secuencia predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c2adc-104">When a file is opened, Windows associates a *file pointer* with the default stream.</span></span> <span data-ttu-id="c2adc-105">Este puntero de archivo es un valor de desplazamiento de 64 bits que especifica el siguiente byte que se va a leer o la ubicación para recibir el siguiente byte escrito.</span><span class="sxs-lookup"><span data-stu-id="c2adc-105">This file pointer is a 64-bit offset value that specifies the next byte to be read or the location to receive the next byte written.</span></span> <span data-ttu-id="c2adc-106">Cada vez que se abre un archivo, el sistema coloca el puntero de archivo al principio del archivo, que es el desplazamiento de cero.</span><span class="sxs-lookup"><span data-stu-id="c2adc-106">Each time a file is opened, the system places the file pointer at the beginning of the file, which is offset zero.</span></span> <span data-ttu-id="c2adc-107">Cada operación de lectura y escritura hace avanzar el puntero de archivo por el número de bytes que se leen y se escriben.</span><span class="sxs-lookup"><span data-stu-id="c2adc-107">Each read and write operation advances the file pointer by the number of bytes being read and written.</span></span> <span data-ttu-id="c2adc-108">Por ejemplo, si el puntero de archivo está al principio del archivo y se solicita una operación de lectura de 5 bytes, el puntero de archivo se ubicará en el desplazamiento 5 inmediatamente después de la operación de lectura.</span><span class="sxs-lookup"><span data-stu-id="c2adc-108">For example, if the file pointer is at the beginning of the file and a read operation of 5 bytes is requested, the file pointer will be located at offset 5 immediately after the read operation.</span></span> <span data-ttu-id="c2adc-109">A medida que se lee o escribe cada byte, el sistema hace avanzar el puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="c2adc-109">As each byte is read or written, the system advances the file pointer.</span></span> <span data-ttu-id="c2adc-110">También se puede cambiar la posición del puntero de archivo mediante una llamada a la función [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) .</span><span class="sxs-lookup"><span data-stu-id="c2adc-110">The file pointer can also be repositioned by calling the [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function.</span></span>

<span data-ttu-id="c2adc-111">Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leer el archivo, no se produce ningún error, pero no se lee ningún byte.</span><span class="sxs-lookup"><span data-stu-id="c2adc-111">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="c2adc-112">Por lo tanto, la lectura de cero bytes sin un error significa que la aplicación ha alcanzado el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="c2adc-112">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="c2adc-113">La escritura de cero bytes no hace nada.</span><span class="sxs-lookup"><span data-stu-id="c2adc-113">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="c2adc-114">Una aplicación puede truncar o extender un archivo mediante la función [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) .</span><span class="sxs-lookup"><span data-stu-id="c2adc-114">An application can truncate or extend a file by using the [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile) function.</span></span> <span data-ttu-id="c2adc-115">Esta función establece el final del archivo en la posición actual del puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="c2adc-115">This function sets the end of file to the current position of the file pointer.</span></span>

 

 



