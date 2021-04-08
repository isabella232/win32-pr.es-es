---
description: Después de recuperar la información de instalación de un archivo INF, hay varias funciones de control de archivos que puede usar para instalar los archivos enumerados en una sección de INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Instalación desde un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc3642edfb7abc2864c2c0784c79fbb21612fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911554"
---
# <a name="installing-from-an-inf-file"></a>Instalación desde un archivo INF

Después de recuperar la información de instalación de un archivo INF, hay varias funciones de control de archivos que puede usar para instalar los archivos enumerados en una sección de INF. Las funciones de bajo nivel, como [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) y [**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) , instalan un único archivo.

También hay funciones para administrar archivos comprimidos. La función [**SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) devuelve información acerca de los archivos comprimidos. A continuación, [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) puede usar esta información para copiar y, si es necesario, expandir el archivo.

Las funciones de alto nivel como [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)y [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) procesan las operaciones de instalación en una sección de **instalación** o **servicio** . De estos, **SetupInstallFromInfSection** es el más versátil porque puede realizar cualquier tipo de operación de instalación enumerada en **la sección de instalación de** un archivo INF. Esto incluye las operaciones de registro y de INI que aparecen en las líneas **AddReg**, **DelReg**, **UpdateInis** o **UpdateIniField** de una sección de **instalación** .

Las funciones [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) y [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) ponen en cola las operaciones de una sección de **instalación** o **servicio** , respectivamente, en una cola de archivos existente. Tenga en cuenta que debe llamar a SetupInstallFromInfSection y SetupInstallServicesFromInfSection por separado para poner en cola las operaciones y los servicios. Para obtener más información, vea [colas de archivos](file-queues.md).

En cambio, la función [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea y destruye su propia cola interna. Un uso común de **SetupInstallFromInfSection** es llamarlo después de que todos los archivos se hayan copiado correctamente para realizar las transacciones del registro y del archivo ini.

En Windows 2000, los archivos DLL se pueden registrar automáticamente mediante una llamada a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) en un archivo INF que incluye la directiva **RegisterDlls** en su sección **install** . **SetupInstallFromInfSection** también puede registrar automáticamente archivos dll de 32 bits de un proceso de 64 bits.

En los sistemas operativos de 64 bits, se puede llamar a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) para realizar operaciones en la parte de 32 bits del registro. Para agregar una clave del registro a la parte de 32 bits del registro, incluya la \_ marca FLG ADDREG \_ 32BITKEY en la línea **AddReg** del archivo INF. Para eliminar una clave del registro solo en la parte de 32 bits del registro, incluya la \_ clave FLG DELREG \_ 32BITKEY en la línea **DELREG** . Para establecer o borrar un valor binario solo en la parte de 32 bits del registro, incluya FLG \_ BITREG \_ 32BITKEY en la línea **BITREG** .

Además de las funciones enumeradas anteriormente, la API de instalación incluye funciones que ponen en cola las operaciones de instalación de archivos, ya sea por archivo o por sección de INF. Para obtener más información, vea [colas de archivos](file-queues.md).

 

 



