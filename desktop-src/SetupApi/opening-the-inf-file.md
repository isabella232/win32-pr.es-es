---
description: Debe usar la función SetupOpenInfFile para abrir el archivo INF para poder recuperar información de él o para anexar otros archivos INF.
ms.assetid: ba4d511a-ad19-4619-a10a-cafef789821b
title: Abrir el archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8493fda983f2942705b97ea243f6cb95e91c15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910337"
---
# <a name="opening-the-inf-file"></a><span data-ttu-id="cb963-103">Abrir el archivo INF</span><span class="sxs-lookup"><span data-stu-id="cb963-103">Opening the INF File</span></span>

<span data-ttu-id="cb963-104">Debe usar la función [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) para abrir el archivo INF para poder recuperar información de él o para anexar otros archivos INF.</span><span class="sxs-lookup"><span data-stu-id="cb963-104">You must use the [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) function to open the INF file before you can retrieve information from it, or append other INF files to it.</span></span>

<span data-ttu-id="cb963-105">Lo siguiente abre un archivo INF mediante [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) y devuelve un identificador, MyInf, al archivo INF abierto.</span><span class="sxs-lookup"><span data-stu-id="cb963-105">The following opens an INF file using [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) and returns a handle, MyInf, to the opened INF file.</span></span> <span data-ttu-id="cb963-106">El parámetro *InfClass* de **SetupOpenInfFile** se especifica como **null** para indicar que la clase del archivo inf debe omitirse.</span><span class="sxs-lookup"><span data-stu-id="cb963-106">The *InfClass* parameter of **SetupOpenInfFile** is specified as **NULL** to indicate that the Class of the INF file should be ignored.</span></span>


```C++
HINF MyInf;                //variable to hold the INF handle
UINT ErrorLine;            //variable to hold errors returned
BOOL test=0;                 //variable to receive function success
 
MyInf = SetupOpenInfFile (
      szInfFileName,       //the filename of the inf file to open
      NULL,                //optional class information
      INF_STYLE_WIN4,      //the inf style
      &ErrorLine           //line number of the syntax error
);
```



<span data-ttu-id="cb963-107">Después de abrir un archivo INF, puede llamar a la función [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) para anexar un archivo al archivo INF abierto.</span><span class="sxs-lookup"><span data-stu-id="cb963-107">After an INF file is opened, you can call the [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) function to append a file to the open INF file.</span></span> <span data-ttu-id="cb963-108">Para anexar varios archivos, repita este proceso.</span><span class="sxs-lookup"><span data-stu-id="cb963-108">To append several files, repeat this process.</span></span> <span data-ttu-id="cb963-109">Si llama a la función **SetupOpenAppendInfFile** y el nombre de archivo que se le ha pasado es **null**, la función buscará en la sección de versión del archivo INF abierto (y los archivos INF anexados) una clave LayoutFile.</span><span class="sxs-lookup"><span data-stu-id="cb963-109">If you call the **SetupOpenAppendInfFile** function and the filename passed to it is **NULL**, then the function will search the Version section of the open INF file (and any appended INF files) for a LayoutFile key.</span></span> <span data-ttu-id="cb963-110">Si la función encuentra una clave, anexará el archivo especificado por esa clave (normalmente, el diseño. INF).</span><span class="sxs-lookup"><span data-stu-id="cb963-110">If the function finds a key, it will append the file specified by that key (usually LAYOUT.INF).</span></span> <span data-ttu-id="cb963-111">Cuando se han combinado varios archivos INF, **SetupOpenAppendInfFile** comienza con el último archivo INF anexado cuando busca una sección de versión.</span><span class="sxs-lookup"><span data-stu-id="cb963-111">When multiple INF files have been combined, **SetupOpenAppendInfFile** starts with the last appended INF file when it searches for a Version section.</span></span>

 

 



