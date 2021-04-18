---
description: Una aplicación Lee y escribe en un archivo mediante las funciones ReadFile, ReadFileEx, WriteFile y WriteFileEx.
ms.assetid: 14ecb06c-3f80-47b8-9964-6a2c3b572300
title: Leer y escribir en archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd0e6518ce2430e18bbb11033023ee6dc274573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668143"
---
# <a name="reading-from-and-writing-to-files"></a><span data-ttu-id="cbc37-103">Leer y escribir en archivos</span><span class="sxs-lookup"><span data-stu-id="cbc37-103">Reading From and Writing to Files</span></span>

<span data-ttu-id="cbc37-104">Una aplicación Lee y escribe en un archivo mediante las funciones [**readfile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) .</span><span class="sxs-lookup"><span data-stu-id="cbc37-104">An application reads from and writes to a file by using the [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex), [**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) functions.</span></span> <span data-ttu-id="cbc37-105">Estas funciones requieren un identificador de un archivo que se va a abrir para lectura y escritura, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cbc37-105">These functions require a handle to a file to be opened for reading and writing, respectively.</span></span> <span data-ttu-id="cbc37-106">Leen y escriben un número especificado de bytes en la ubicación indicada por el puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="cbc37-106">They read and write a specified number of bytes at the location indicated by the file pointer.</span></span> <span data-ttu-id="cbc37-107">Los datos se leen y escriben exactamente como se especifican; las funciones no dan formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="cbc37-107">The data is read and written exactly as specified; the functions do not format the data.</span></span>

<span data-ttu-id="cbc37-108">Cuando el puntero de archivo alcanza el final de un archivo y la aplicación intenta leer el archivo, no se produce ningún error, pero no se lee ningún byte.</span><span class="sxs-lookup"><span data-stu-id="cbc37-108">When the file pointer reaches the end of a file and the application attempts to read from the file, no error occurs, but no bytes are read.</span></span> <span data-ttu-id="cbc37-109">Por lo tanto, la lectura de cero bytes sin un error significa que la aplicación ha alcanzado el final del archivo.</span><span class="sxs-lookup"><span data-stu-id="cbc37-109">Therefore, reading zero bytes without an error means the application has reached the end of the file.</span></span> <span data-ttu-id="cbc37-110">La escritura de cero bytes no hace nada.</span><span class="sxs-lookup"><span data-stu-id="cbc37-110">Writing zero bytes does nothing.</span></span>

<span data-ttu-id="cbc37-111">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="cbc37-111">For more information, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="cbc37-112">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cbc37-112">In this section</span></span>



| <span data-ttu-id="cbc37-113">Tema</span><span class="sxs-lookup"><span data-stu-id="cbc37-113">Topic</span></span>                                                                                                                                           | <span data-ttu-id="cbc37-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbc37-114">Description</span></span>                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbc37-115">Colocar un puntero de archivo</span><span class="sxs-lookup"><span data-stu-id="cbc37-115">Positioning a File Pointer</span></span>](positioning-a-file-pointer.md)<br/>                                                                         | <span data-ttu-id="cbc37-116">Windows usa un puntero de archivo para hacer un seguimiento de los bytes leídos o escritos.</span><span class="sxs-lookup"><span data-stu-id="cbc37-116">Windows uses a file pointer to keep track of bytes read or written.</span></span><br/>                                                       |
| [<span data-ttu-id="cbc37-117">Leer o escribir en archivos mediante un esquema de Scatter-Gather</span><span class="sxs-lookup"><span data-stu-id="cbc37-117">Reading From or Writing To Files Using a Scatter-Gather Scheme</span></span>](reading-from-or-writing-to-files-using-a-scatter-gather-scheme.md)<br/> | <span data-ttu-id="cbc37-118">Describe un esquema de dispersión y recopilación para leer o escribir fragmentos de datos no contiguos en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="cbc37-118">Describes a scatter-gather scheme for reading or writing noncontiguous chunks of data in one operation.</span></span><br/>                   |
| [<span data-ttu-id="cbc37-119">Vaciar System-Buffered datos de e/s en el disco</span><span class="sxs-lookup"><span data-stu-id="cbc37-119">Flushing System-Buffered I/O Data to Disk</span></span>](flushing-system-buffered-i-o-data-to-disk.md)<br/>                                           | <span data-ttu-id="cbc37-120">Windows almacena los datos en las operaciones de lectura y escritura de archivos en los búferes de datos mantenidos por el sistema para optimizar el rendimiento del disco.</span><span class="sxs-lookup"><span data-stu-id="cbc37-120">Windows stores the data in file read and write operations in system-maintained data buffers to optimize disk performance.</span></span><br/> |
| [<span data-ttu-id="cbc37-121">Truncar o extender archivos</span><span class="sxs-lookup"><span data-stu-id="cbc37-121">Truncating or Extending Files</span></span>](truncating-or-extending-files.md)<br/>                                                                   | <span data-ttu-id="cbc37-122">Una aplicación puede truncar o extender un archivo mediante una llamada a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="cbc37-122">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span><br/>                             |



 

 

 




