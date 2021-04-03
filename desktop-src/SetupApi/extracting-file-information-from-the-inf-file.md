---
description: Una vez abierto el archivo INF, puede recopilar información de él para compilar la interfaz de usuario o para dirigir el proceso de instalación. Las funciones de configuración proporcionan varios niveles de funcionalidad para recopilar información de un archivo INF.
ms.assetid: 3ef2768b-8c73-4258-937c-77a40963ffe4
title: Extracción de información de archivos del archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be4b404f44ca7d1d92fe0ce8eab08b73012ff144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908165"
---
# <a name="extracting-file-information-from-the-inf-file"></a><span data-ttu-id="fc0af-104">Extracción de información de archivos del archivo INF</span><span class="sxs-lookup"><span data-stu-id="fc0af-104">Extracting File Information from the INF file</span></span>

<span data-ttu-id="fc0af-105">Una vez abierto el archivo INF, puede recopilar información de él para compilar la interfaz de usuario o para dirigir el proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="fc0af-105">After the INF file is opened, you can gather information from it to build the user interface, or to direct the installation process.</span></span> <span data-ttu-id="fc0af-106">Las funciones de configuración proporcionan varios niveles de funcionalidad para recopilar información de un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="fc0af-106">The setup functions provide several levels of functionality for gathering information from an INF file.</span></span>



| <span data-ttu-id="fc0af-107">Para recopilar información...</span><span class="sxs-lookup"><span data-stu-id="fc0af-107">To gather information…</span></span>                | <span data-ttu-id="fc0af-108">Usar estas funciones...</span><span class="sxs-lookup"><span data-stu-id="fc0af-108">Use these functions…</span></span>                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="fc0af-109">Acerca del archivo INF</span><span class="sxs-lookup"><span data-stu-id="fc0af-109">About the INF file</span></span>                    | [<span data-ttu-id="fc0af-110">**SetupGetInfInformation**</span><span class="sxs-lookup"><span data-stu-id="fc0af-110">**SetupGetInfInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [<span data-ttu-id="fc0af-111">**SetupQueryInfFileInformation**</span><span class="sxs-lookup"><span data-stu-id="fc0af-111">**SetupQueryInfFileInformation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | <span data-ttu-id="fc0af-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span><span class="sxs-lookup"><span data-stu-id="fc0af-112">[**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa).</span></span> |
| <span data-ttu-id="fc0af-113">Acerca de los archivos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="fc0af-113">About source and target files</span></span>         | [<span data-ttu-id="fc0af-114">**SetupGetSourceFileLocation**</span><span class="sxs-lookup"><span data-stu-id="fc0af-114">**SetupGetSourceFileLocation**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [<span data-ttu-id="fc0af-115">**SetupGetSourceFileSize**</span><span class="sxs-lookup"><span data-stu-id="fc0af-115">**SetupGetSourceFileSize**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [<span data-ttu-id="fc0af-116">**SetupGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="fc0af-116">**SetupGetTargetPath**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [<span data-ttu-id="fc0af-117">**SetupGetSourceInfo**</span><span class="sxs-lookup"><span data-stu-id="fc0af-117">**SetupGetSourceInfo**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| <span data-ttu-id="fc0af-118">Desde una línea de un archivo INF</span><span class="sxs-lookup"><span data-stu-id="fc0af-118">From a line of an INF file</span></span>            | [<span data-ttu-id="fc0af-119">**SetupGetLineText**</span><span class="sxs-lookup"><span data-stu-id="fc0af-119">**SetupGetLineText**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [<span data-ttu-id="fc0af-120">**SetupFindNextLine**</span><span class="sxs-lookup"><span data-stu-id="fc0af-120">**SetupFindNextLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [<span data-ttu-id="fc0af-121">**SetupFindNextMatchLine**</span><span class="sxs-lookup"><span data-stu-id="fc0af-121">**SetupFindNextMatchLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [<span data-ttu-id="fc0af-122">**SetupGetLineByIndex**</span><span class="sxs-lookup"><span data-stu-id="fc0af-122">**SetupGetLineByIndex**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [<span data-ttu-id="fc0af-123">**SetupFindFirstLine**</span><span class="sxs-lookup"><span data-stu-id="fc0af-123">**SetupFindFirstLine**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| <span data-ttu-id="fc0af-124">Desde un campo de una línea en un archivo INF</span><span class="sxs-lookup"><span data-stu-id="fc0af-124">From a field of a line in an INF file</span></span> | [<span data-ttu-id="fc0af-125">**SetupGetStringField**</span><span class="sxs-lookup"><span data-stu-id="fc0af-125">**SetupGetStringField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [<span data-ttu-id="fc0af-126">**SetupGetIntField**</span><span class="sxs-lookup"><span data-stu-id="fc0af-126">**SetupGetIntField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [<span data-ttu-id="fc0af-127">**SetupGetBinaryField**</span><span class="sxs-lookup"><span data-stu-id="fc0af-127">**SetupGetBinaryField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [<span data-ttu-id="fc0af-128">**SetupGetMultiSzField**</span><span class="sxs-lookup"><span data-stu-id="fc0af-128">**SetupGetMultiSzField**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

<span data-ttu-id="fc0af-129">En el ejemplo siguiente se usa la función [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) para recuperar la descripción inteligible de un medio de origen de un archivo INF.</span><span class="sxs-lookup"><span data-stu-id="fc0af-129">The following example uses the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function to retrieve the human-readable description of a source media from an INF file.</span></span>


```C++
#include <windows.h>
#include <setupapi.h>

BOOL test;  
HINF MyInf;
UINT SourceId;
PTSTR Buffer;
DWORD MaxBufSize;
DWORD BufSize;

int main()  
{ 

test = SetupGetSourceInfo (
     MyInf,   //Handle to the INF file to access                
     SourceId, //Id of the source media                 
     SRCINFO_DESCRIPTION, //which information to retrieve     
     Buffer, //a pointer to the buffer to receive the information                     
     MaxBufSize,  //the size allocated for the buffer 
     &BufSize    //buffer size actually needed
);
  
return 0;
}
```



<span data-ttu-id="fc0af-130">En el ejemplo, MyInf es el identificador del archivo INF abierto.</span><span class="sxs-lookup"><span data-stu-id="fc0af-130">In the example, MyInf is the handle to the open INF file.</span></span> <span data-ttu-id="fc0af-131">SourceId es el identificador de un medio de origen específico.</span><span class="sxs-lookup"><span data-stu-id="fc0af-131">SourceId is the identifier for a specific source media.</span></span> <span data-ttu-id="fc0af-132">El valor SRCINFO \_ Description especifica que la función [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) debe recuperar la descripción del medio de origen.</span><span class="sxs-lookup"><span data-stu-id="fc0af-132">The value SRCINFO\_DESCRIPTION specifies that the [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) function should retrieve the source media description.</span></span> <span data-ttu-id="fc0af-133">El búfer apunta a una cadena que recibirá la descripción, MaxBufSize indica los recursos asignados al búfer y BufSize indica los recursos necesarios para almacenar el búfer.</span><span class="sxs-lookup"><span data-stu-id="fc0af-133">Buffer points to a string that will receive the description, MaxBufSize indicates the resources allocated to the buffer, and BufSize indicates the resources necessary to store the buffer.</span></span>

<span data-ttu-id="fc0af-134">Si BufSize es mayor que MaxBufSize, la función devolverá **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) DEvolverá un error de \_ búfer insuficiente \_ .</span><span class="sxs-lookup"><span data-stu-id="fc0af-134">If BufSize is greater than MaxBufSize, the function will return **FALSE**, and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return ERROR\_INSUFFICIENT\_BUFFER.</span></span>

 

 
