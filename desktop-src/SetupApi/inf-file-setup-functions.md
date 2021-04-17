---
description: Las siguientes funciones de la API de instalación se utilizan con archivos INF.
ms.assetid: fb4263fc-5f59-460a-a7d9-93f10729c02a
title: Funciones de configuración de archivos INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24944f19938217d40ff4a7eaebbfb638c26e4afb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668001"
---
# <a name="inf-file-setup-functions"></a>Funciones de configuración de archivos INF

Las siguientes funciones de la API de instalación se utilizan con archivos INF.



| Función                                                                         | Descripción                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile)                                   | Libera recursos y cierra el identificador INF.                                                                                                                                                             |
| [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea)                   | Copia un archivo y, si es necesario, lo descomprime.                                                                                                                                                      |
| [**SetupFindFirstLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindfirstlinea)                                 | Busca la primera línea de una sección de un archivo INF o, si se especifica una clave, la primera línea que coincide con esa clave. Actualiza el miembro de **línea** de una estructura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) . |
| [**SetupFindNextLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextline)                                   | Devuelve la línea siguiente de una sección relativa al miembro de **línea** de la estructura [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) especificada.                                                                    |
| [**SetupFindNextMatchLine**](/windows/desktop/api/Setupapi/nf-setupapi-setupfindnextmatchlinea)                         | Devuelve la siguiente línea en una sección relativa al miembro de la **línea** del [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) especificado que coincide con una clave especificada.                                                 |
| [**SetupGetBinaryField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetbinaryfield)                               | Recupera datos de una línea cuyos campos están en formato binario.                                                                                                                                          |
| [**SetupGetFieldCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfieldcount)                                 | Devuelve el número de campos de una línea.                                                                                                                                                                |
| [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa)               | Recupera información de compresión de archivos de un archivo INF.                                                                                                                                               |
| [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista)                               | Obtiene una lista de los tipos de archivos INF en un directorio especificado.                                                                                                                                        |
| [**SetupGetInfInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinfinformationa)                         | Devuelve información sobre un archivo INF (por miembro de **línea** de un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) o un nombre de archivo).                                                                                     |
| [**SetupGetIntField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetintfield)                                     | Devuelve el campo de entero especificado de una línea en un archivo INF.                                                                                                                                          |
| [**SetupGetLineByIndex**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinebyindexa)                               | Actualiza el miembro de **línea** de un [**INFCONTEXT**](/windows/desktop/api/Setupapi/ns-setupapi-infcontext) para la línea en el índice especificado de la sección especificada.                                                                     |
| [**SetupGetLineCount**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinecounta)                                   | Devuelve el número de líneas de la sección especificada.                                                                                                                                                  |
| [**SetupGetLineText**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetlinetexta)                                     | Recupera el contenido de una línea especificada de un archivo INF.                                                                                                                                            |
| [**SetupGetMultiSzField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetmultiszfielda)                             | Devuelve una lista de cadenas, comenzando por el campo especificado de una línea en un archivo INF.                                                                                                                   |
| [**SetupGetSourceFileLocation**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilelocationa)                 | Obtiene el ordinal y la ruta de acceso del disco de origen (relativo a la raíz de origen) donde se encuentra el archivo de código fuente.                                                                                                       |
| [**SetupGetSourceFileSize**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourcefilesizea)                         | Obtiene el tamaño de archivo de un archivo de código fuente individual o de una sección de **archivos de copia** de un archivo INF.                                                                                                           |
| [**SetupGetSourceInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetsourceinfoa)                                 | Recupera la ruta de acceso, el archivo de etiqueta o la descripción de un origen.                                                                                                                                             |
| [**SetupGetStringField**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetstringfielda)                               | Devuelve el campo de cadena especificado de una línea en un archivo INF.                                                                                                                                           |
| [**SetupGetTargetPath**](/windows/desktop/api/Setupapi/nf-setupapi-setupgettargetpatha)                                 | Obtiene la ruta de acceso de destino para una sección de **archivos de copia** en un archivo INF.                                                                                                                                      |
| [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)                                     | Instala un archivo.                                                                                                                                                                                       |
| [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)                                 | Instala un archivo y devuelve una variable que indica si el archivo estaba en uso o no.                                                                                                                  |
| [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)       | Pone en cola todos los archivos especificados en las secciones **copiar archivos**, **eliminar archivos** y **cambiar nombre de archivo** que aparecen en una sección de **instalación** .                                                       |
| [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)                 | Realiza las directivas especificadas en una sección de **instalación** de archivos INF.                                                                                                                                  |
| [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) | Realiza operaciones de instalación y eliminación de servicios como se especifica en una sección de **servicio** de un archivo INF.                                                                                            |
| [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)                         | Abre un archivo INF y lo anexa a un identificador INF existente.                                                                                                                                             |
| [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea)                                     | Abre un archivo INF y le devuelve un identificador.                                                                                                                                                          |
| [**SetupOpenMasterInf**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenmasterinf)                                 | Abre el archivo INF que contiene información sobre el archivo y el diseño de los archivos que se incluyen con el sistema.                                                                                                        |
| [**SetupQueryInfFileInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinffileinformationa)             | Consulta una estructura de información de INF sobre sus nombres de archivo INF asociados.                                                                                                                               |
| [**SetupQueryInfVersionInformation**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryinfversioninformationa)       | Consulta una estructura de información de INF para obtener información de versión en uno de sus archivos INF constituyentes.                                                                                                      |
| [**SetupSetDirectoryId**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetdirectoryida)                               | Asocia un nuevo identificador de directorio a un directorio determinado.                                                                                                                                     |



 

 

 



