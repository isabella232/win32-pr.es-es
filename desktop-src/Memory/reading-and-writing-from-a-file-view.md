---
description: Para leer desde una vista de archivo, desreferencia el puntero devuelto por la función MapViewOfFile tal como se muestra en los ejemplos siguientes.
ms.assetid: c2a3da09-d116-4c2c-9e6c-ec9e80c88b99
title: Leer y escribir en una vista de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98ec50dc6cd8b0224f2ba33a17ba80c7b0fc658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688683"
---
# <a name="reading-and-writing-from-a-file-view"></a><span data-ttu-id="9c241-103">Leer y escribir en una vista de archivo</span><span class="sxs-lookup"><span data-stu-id="9c241-103">Reading and Writing From a File View</span></span>

<span data-ttu-id="9c241-104">Para leer desde una vista de archivo, desreferencia el puntero devuelto por la función [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) tal como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="9c241-104">To read from a file view, dereference the pointer returned by the [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) function as shown in the examples below.</span></span>

<span data-ttu-id="9c241-105">Leer o escribir en una vista de archivo de un archivo que no sea el archivo de paginación puede producir una **excepción en la excepción \_ de \_ \_ error de página** .</span><span class="sxs-lookup"><span data-stu-id="9c241-105">Reading from or writing to a file view of a file other than the page file can cause an **EXCEPTION\_IN\_PAGE\_ERROR** exception.</span></span> <span data-ttu-id="9c241-106">Por ejemplo, el acceso a un archivo asignado que se encuentra en un servidor remoto puede generar una excepción si se pierde la conexión al servidor.</span><span class="sxs-lookup"><span data-stu-id="9c241-106">For example, accessing a mapped file that resides on a remote server can generate an exception if the connection to the server is lost.</span></span> <span data-ttu-id="9c241-107">También se pueden producir excepciones debido a un disco completo, un error de dispositivo subyacente o un error de asignación de memoria.</span><span class="sxs-lookup"><span data-stu-id="9c241-107">Exceptions can also occur because of a full disk, an underlying device failure, or a memory allocation failure.</span></span> <span data-ttu-id="9c241-108">Al escribir en una vista de archivos, las excepciones también pueden producirse porque el archivo está compartido y un proceso diferente ha bloqueado un intervalo de bytes.</span><span class="sxs-lookup"><span data-stu-id="9c241-108">When writing to a file view, exceptions can also occur because the file is shared and a different process has locked a byte range.</span></span> <span data-ttu-id="9c241-109">Para protegerse frente a excepciones debido a errores de entrada y salida (e/s), todos los intentos de acceso a archivos asignados a memoria se deben encapsular en controladores de excepciones estructurados.</span><span class="sxs-lookup"><span data-stu-id="9c241-109">To guard against exceptions due to input and output (I/O) errors, all attempts to access memory mapped files should be wrapped in structured exception handlers.</span></span> <span data-ttu-id="9c241-110">Cuando reciba una **excepción \_ en \_ un \_ error de página** en el filtro **\_ \_ excepto** , asegúrese de que la dirección está dentro de la asignación a la que está accediendo actualmente.</span><span class="sxs-lookup"><span data-stu-id="9c241-110">When you receive **EXCEPTION\_IN\_PAGE\_ERROR** in your **\_\_except** filter, make sure that the address is within the mapping you are currently accessing.</span></span> <span data-ttu-id="9c241-111">Si es así, recupere o produzca un error correctamente; de lo contrario, no controle la excepción.</span><span class="sxs-lookup"><span data-stu-id="9c241-111">If so, recover or fail gracefully; otherwise, do not handle the exception.</span></span>

<span data-ttu-id="9c241-112">En el ejemplo siguiente se usa el puntero devuelto por **MapViewOfFile** para leer desde la vista de archivo:</span><span class="sxs-lookup"><span data-stu-id="9c241-112">The following example uses the pointer returned by **MapViewOfFile** to read from the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    dwLength = *((LPDWORD) lpMapAddress);
  }
  __except(GetExceptionCode()==EXCEPTION_IN_PAGE_ERROR ?
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to read from the view.
  }
```



<span data-ttu-id="9c241-113">En el ejemplo siguiente se usa el puntero devuelto por **MapViewOfFile** para escribir en la vista de archivo:</span><span class="sxs-lookup"><span data-stu-id="9c241-113">The following example uses the pointer returned by **MapViewOfFile** to write to the file view:</span></span>


```C++
  DWORD dwLength;

  __try
  {
    *((LPDWORD) lpMapAddress) = dwLength;
  }
  __except (GetExceptionCode() == EXCEPTION_IN_PAGE_ERROR ? 
    EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH)
  {
    // Failed to write to the view.
  }
```



<span data-ttu-id="9c241-114">La función [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) copia el número especificado de bytes de la vista de archivo en el archivo físico, sin esperar a que se produzca la operación de escritura almacenada en caché:</span><span class="sxs-lookup"><span data-stu-id="9c241-114">The [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) function copies the specified number of bytes of the file view to the physical file, without waiting for the cached write operation to occur:</span></span>


```C++
  if (!FlushViewOfFile(lpMapAddress, dwBytesToFlush)) 
  {
    printf("Could not flush memory to disk (%d).\n", GetLastError()); 
  }
```



<span data-ttu-id="9c241-115">Si está asignando un archivo comprimido o disperso en una partición NTFS, existe una posibilidad adicional de que se produzca un error de e/s al paginar en una parte del archivo.</span><span class="sxs-lookup"><span data-stu-id="9c241-115">If you are mapping a compressed or sparse file on an NTFS partition, there is additional potential for an I/O error when paging in a portion of the file.</span></span> <span data-ttu-id="9c241-116">En este caso, es posible que el espacio de direcciones asignado por [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) no esté respaldado por el espacio en disco asignado.</span><span class="sxs-lookup"><span data-stu-id="9c241-116">In this case, the address space mapped by [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) may not be backed by allocated disk space.</span></span> <span data-ttu-id="9c241-117">Esto se debe a que un archivo disperso puede tener regiones de ceros para los que NTFS no asigna espacio en disco, y un archivo comprimido puede ocupar menos espacio en disco que los datos reales que representa.</span><span class="sxs-lookup"><span data-stu-id="9c241-117">This is because a sparse file can have regions of zeros for which NTFS does not allocate disk space, and a compressed file can take up less disk space than the actual data that it represents.</span></span> <span data-ttu-id="9c241-118">Si lee o escribe en una parte de un archivo disperso o comprimido que no está respaldado por el espacio en disco, el sistema operativo puede intentar asignar espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="9c241-118">If you read from or write to a portion of a sparse or compressed file that is not backed by disk space, the operating system may try to allocate disk space.</span></span> <span data-ttu-id="9c241-119">Si el disco está lleno, se puede producir una excepción que indica un error de e/s.</span><span class="sxs-lookup"><span data-stu-id="9c241-119">If the disk is full, this can result in an exception indicating an I/O error.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c241-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c241-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c241-121">Control estructurado de excepciones</span><span class="sxs-lookup"><span data-stu-id="9c241-121">Structured Exception Handling</span></span>](../debug/structured-exception-handling.md)
</dt> </dl>

 

 
