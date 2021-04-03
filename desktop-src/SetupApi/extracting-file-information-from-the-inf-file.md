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
# <a name="extracting-file-information-from-the-inf-file"></a>Extracción de información de archivos del archivo INF

Una vez abierto el archivo INF, puede recopilar información de él para compilar la interfaz de usuario o para dirigir el proceso de instalación. Las funciones de configuración proporcionan varios niveles de funcionalidad para recopilar información de un archivo INF.



| Para recopilar información...                | Usar estas funciones...                                                        |
|---------------------------------------|-----------------------------------------------------------------------------|
| Acerca del archivo INF                    | [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                    |
|                                       | [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)        |
|                                       | [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa). |
| Acerca de los archivos de origen y de destino         | [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)            |
|                                       | [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                    |
|                                       | [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                            |
|                                       | [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                            |
| Desde una línea de un archivo INF            | [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                |
|                                       | [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                              |
|                                       | [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                    |
|                                       | [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                          |
|                                       | [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                            |
| Desde un campo de una línea en un archivo INF | [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                          |
|                                       | [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                |
|                                       | [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                          |
|                                       | [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                        |



 

En el ejemplo siguiente se usa la función [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) para recuperar la descripción inteligible de un medio de origen de un archivo INF.


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



En el ejemplo, MyInf es el identificador del archivo INF abierto. SourceId es el identificador de un medio de origen específico. El valor SRCINFO \_ Description especifica que la función [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa) debe recuperar la descripción del medio de origen. El búfer apunta a una cadena que recibirá la descripción, MaxBufSize indica los recursos asignados al búfer y BufSize indica los recursos necesarios para almacenar el búfer.

Si BufSize es mayor que MaxBufSize, la función devolverá **false** y una llamada subsiguiente a [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) DEvolverá un error de \_ búfer insuficiente \_ .

 

 
