---
description: Si desea ver una parte del archivo que no comienza al principio del archivo, debe crear un objeto de asignación de archivos.
ms.assetid: e47a0e79-3000-479b-afba-dcd36210ea3d
title: Crear una vista dentro de un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9425a1c491a5c7d8ae7861d53418ee0f349bf212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907883"
---
# <a name="creating-a-view-within-a-file"></a><span data-ttu-id="486a8-103">Crear una vista dentro de un archivo</span><span class="sxs-lookup"><span data-stu-id="486a8-103">Creating a View Within a File</span></span>

<span data-ttu-id="486a8-104">Si desea ver una parte del archivo que no comienza al principio del archivo, debe crear un objeto de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="486a8-104">If you want to view a portion of the file that does not start at the beginning of the file, you must create a file mapping object.</span></span> <span data-ttu-id="486a8-105">Este objeto es el tamaño de la parte del archivo que desea ver más el desplazamiento en el archivo.</span><span class="sxs-lookup"><span data-stu-id="486a8-105">This object is the size of the portion of the file you want to view plus the offset into the file.</span></span> <span data-ttu-id="486a8-106">Por ejemplo, si desea ver el 1 kilobyte (1K) que empieza 131.072 bytes (128K) en el archivo, debe crear un objeto de asignación de archivos de al menos 132.096 bytes (129K) en tamaño.</span><span class="sxs-lookup"><span data-stu-id="486a8-106">For example, if you want to view the 1 kilobyte (1K) that begins 131,072 bytes (128K) into the file, you must create a file mapping object of at least 132,096 bytes (129K) in size.</span></span> <span data-ttu-id="486a8-107">La vista inicia 131.072 bytes (128K) en el archivo y se extiende para al menos 1.024 bytes.</span><span class="sxs-lookup"><span data-stu-id="486a8-107">The view starts 131,072 bytes (128K) into the file and extend for at least 1,024 bytes.</span></span> <span data-ttu-id="486a8-108">En este ejemplo se presupone una granularidad de asignación de archivos de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="486a8-108">This example assumes a file allocation granularity of 64K.</span></span>

<span data-ttu-id="486a8-109">La granularidad de asignación de archivos afecta a la ubicación en la que se puede iniciar una vista de mapa.</span><span class="sxs-lookup"><span data-stu-id="486a8-109">File allocation granularity affects where a map view can start.</span></span> <span data-ttu-id="486a8-110">Una vista de mapa debe comenzar en un desplazamiento en el archivo que sea un múltiplo de la granularidad de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="486a8-110">A map view must start at an offset into the file that is a multiple of the file allocation granularity.</span></span> <span data-ttu-id="486a8-111">Por tanto, es posible que los datos que desea ver sean el módulo de desplazamiento de archivos de la granularidad de la asignación en la vista.</span><span class="sxs-lookup"><span data-stu-id="486a8-111">So the data you want to view may be the file offset modulo the allocation granularity into the view.</span></span> <span data-ttu-id="486a8-112">El tamaño de la vista es el desplazamiento del módulo de datos que es la granularidad de la asignación, más el tamaño de los datos que desea examinar.</span><span class="sxs-lookup"><span data-stu-id="486a8-112">The size of the view is the offset of the data modulo the allocation granularity, plus the size of the data that you want to examine.</span></span>

<span data-ttu-id="486a8-113">Por ejemplo, supongamos que la función [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) indica una granularidad de asignación de 64 KB.</span><span class="sxs-lookup"><span data-stu-id="486a8-113">For example, suppose that the [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) function indicates an allocation granularity of 64K.</span></span> <span data-ttu-id="486a8-114">Para examinar 1 k de datos de 138.240 bytes (135K) en el archivo, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="486a8-114">To examine 1K of data that is 138,240 bytes (135K) into the file, do the following:</span></span>

1.  <span data-ttu-id="486a8-115">Cree un objeto de asignación de archivos de al menos 139.264 bytes (136K) en tamaño.</span><span class="sxs-lookup"><span data-stu-id="486a8-115">Create a file mapping object of at least 139,264 bytes (136K) in size.</span></span>
2.  <span data-ttu-id="486a8-116">Cree una vista de archivo que se inicie en un desplazamiento de archivo que sea el múltiplo más grande de la granularidad de asignación de archivos menos que el desplazamiento que necesite.</span><span class="sxs-lookup"><span data-stu-id="486a8-116">Create a file view that starts at a file offset that is the largest multiple of the file allocation granularity less than the offset you require.</span></span> <span data-ttu-id="486a8-117">En este caso, la vista de archivo comienza en el desplazamiento 131.072 (128K) en el archivo.</span><span class="sxs-lookup"><span data-stu-id="486a8-117">In this case, the file view starts at offset 131,072 (128K) into the file.</span></span> <span data-ttu-id="486a8-118">La vista es 139264 bytes (136K) menos 131.072 bytes (128K) o 8.192 bytes (8K), en tamaño.</span><span class="sxs-lookup"><span data-stu-id="486a8-118">The view is 139264 bytes (136K) minus 131,072 bytes (128K), or 8,192 bytes (8K), in size.</span></span>
3.  <span data-ttu-id="486a8-119">Cree un desplazamiento de puntero 7K en la vista para tener acceso al 1 k en el que está interesado.</span><span class="sxs-lookup"><span data-stu-id="486a8-119">Create a pointer offset 7K into the view to access the 1K in which you are interested.</span></span>

<span data-ttu-id="486a8-120">Si los datos que desea se colocan en un límite de granularidad de asignación de archivos, podría hacer que la vista sea mayor que la granularidad de asignación de archivos.</span><span class="sxs-lookup"><span data-stu-id="486a8-120">If the data you want straddles a file allocation granularity boundary, you could make the view larger than the file allocation granularity.</span></span> <span data-ttu-id="486a8-121">Esto evita dividir los datos en partes.</span><span class="sxs-lookup"><span data-stu-id="486a8-121">This avoids breaking the data into pieces.</span></span>

<span data-ttu-id="486a8-122">El siguiente programa ilustra el segundo ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="486a8-122">The following program illustrates the second example above.</span></span>


```C++
/*
   This program demonstrates file mapping, especially how to align a
   view with the system file allocation granularity.
*/

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define BUFFSIZE 1024 // size of the memory to examine at any one time

#define FILE_MAP_START 138240 // starting point within the file of
                              // the data to examine (135K)

/* The test file. The code below creates the file and populates it,
   so there is no need to supply it in advance. */

TCHAR * lpcTheFile = TEXT("fmtest.txt"); // the file to be manipulated

int main(void)
{
  HANDLE hMapFile;      // handle for the file's memory-mapped region
  HANDLE hFile;         // the file handle
  BOOL bFlag;           // a result holder
  DWORD dBytesWritten;  // number of bytes written
  DWORD dwFileSize;     // temporary storage for file sizes
  DWORD dwFileMapSize;  // size of the file mapping
  DWORD dwMapViewSize;  // the size of the view
  DWORD dwFileMapStart; // where to start the file map view
  DWORD dwSysGran;      // system allocation granularity
  SYSTEM_INFO SysInfo;  // system information; used to get granularity
  LPVOID lpMapAddress;  // pointer to the base address of the
                        // memory-mapped region
  char * pData;         // pointer to the data
  int i;                // loop counter
  int iData;            // on success contains the first int of data
  int iViewDelta;       // the offset into the view where the data
                        //shows up

  // Create the test file. Open it "Create Always" to overwrite any
  // existing file. The data is re-created below
  hFile = CreateFile(lpcTheFile,
                     GENERIC_READ | GENERIC_WRITE,
                     0,
                     NULL,
                     CREATE_ALWAYS,
                     FILE_ATTRIBUTE_NORMAL,
                     NULL);

  if (hFile == INVALID_HANDLE_VALUE)
  {
    _tprintf(TEXT("hFile is NULL\n"));
    _tprintf(TEXT("Target file is %s\n"),
             lpcTheFile);
    return 4;
  }

  // Get the system allocation granularity.
  GetSystemInfo(&SysInfo);
  dwSysGran = SysInfo.dwAllocationGranularity;

  // Now calculate a few variables. Calculate the file offsets as
  // 64-bit values, and then get the low-order 32 bits for the
  // function calls.

  // To calculate where to start the file mapping, round down the
  // offset of the data into the file to the nearest multiple of the
  // system allocation granularity.
  dwFileMapStart = (FILE_MAP_START / dwSysGran) * dwSysGran;
  _tprintf (TEXT("The file map view starts at %ld bytes into the file.\n"),
          dwFileMapStart);

  // Calculate the size of the file mapping view.
  dwMapViewSize = (FILE_MAP_START % dwSysGran) + BUFFSIZE;
  _tprintf (TEXT("The file map view is %ld bytes large.\n"),
            dwMapViewSize);

  // How large will the file mapping object be?
  dwFileMapSize = FILE_MAP_START + BUFFSIZE;
  _tprintf (TEXT("The file mapping object is %ld bytes large.\n"),
          dwFileMapSize);

  // The data of interest isn't at the beginning of the
  // view, so determine how far into the view to set the pointer.
  iViewDelta = FILE_MAP_START - dwFileMapStart;
  _tprintf (TEXT("The data is %d bytes into the view.\n"),
            iViewDelta);

  // Now write a file with data suitable for experimentation. This
  // provides unique int (4-byte) offsets in the file for easy visual
  // inspection. Note that this code does not check for storage
  // medium overflow or other errors, which production code should
  // do. Because an int is 4 bytes, the value at the pointer to the
  // data should be one quarter of the desired offset into the file

  for (i=0; i<(int)dwSysGran; i++)
  {
    WriteFile (hFile, &i, sizeof (i), &dBytesWritten, NULL);
  }

  // Verify that the correct file size was written.
  dwFileSize = GetFileSize(hFile,  NULL);
  _tprintf(TEXT("hFile size: %10d\n"), dwFileSize);

  // Create a file mapping object for the file
  // Note that it is a good idea to ensure the file size is not zero
  hMapFile = CreateFileMapping( hFile,          // current file handle
                NULL,           // default security
                PAGE_READWRITE, // read/write permission
                0,              // size of mapping object, high
                dwFileMapSize,  // size of mapping object, low
                NULL);          // name of mapping object

  if (hMapFile == NULL)
  {
    _tprintf(TEXT("hMapFile is NULL: last error: %d\n"), GetLastError() );
    return (2);
  }

  // Map the view and test the results.

  lpMapAddress = MapViewOfFile(hMapFile,            // handle to
                                                    // mapping object
                               FILE_MAP_ALL_ACCESS, // read/write
                               0,                   // high-order 32
                                                    // bits of file
                                                    // offset
                               dwFileMapStart,      // low-order 32
                                                    // bits of file
                                                    // offset
                               dwMapViewSize);      // number of bytes
                                                    // to map
  if (lpMapAddress == NULL)
  {
    _tprintf(TEXT("lpMapAddress is NULL: last error: %d\n"), GetLastError());
    return 3;
  }

  // Calculate the pointer to the data.
  pData = (char *) lpMapAddress + iViewDelta;

  // Extract the data, an int. Cast the pointer pData from a "pointer
  // to char" to a "pointer to int" to get the whole thing
  iData = *(int *)pData;

  _tprintf (TEXT("The value at the pointer is %d,\nwhich %s one quarter of the desired file offset.\n"),
            iData,
            iData*4 == FILE_MAP_START ? TEXT("is") : TEXT("is not"));

  // Close the file mapping object and the open file

  bFlag = UnmapViewOfFile(lpMapAddress);
  bFlag = CloseHandle(hMapFile); // close the file mapping object

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the mapping object!"),
             GetLastError());
  }

  bFlag = CloseHandle(hFile);   // close the file itself

  if(!bFlag)
  {
    _tprintf(TEXT("\nError %ld occurred closing the file!"),
           GetLastError());
  }

  return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="486a8-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="486a8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="486a8-124">Crear una vista de archivo</span><span class="sxs-lookup"><span data-stu-id="486a8-124">Creating a File View</span></span>](creating-a-file-view.md)
</dt> </dl>

 

 
