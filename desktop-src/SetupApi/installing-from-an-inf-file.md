---
description: Después de recuperar la información de instalación de un archivo INF, hay varias funciones de control de archivos que puede usar para instalar los archivos enumerados en una sección INF.
ms.assetid: 4e6042a0-36a9-4f74-b6cc-554e7f7aa2d9
title: Instalación desde un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e32780855e126eaaa38ae937a265951711662434e90ab0ffb425e2e4f4f6c42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867575"
---
# <a name="installing-from-an-inf-file"></a>Instalación desde un archivo INF

Después de recuperar la información de instalación de un archivo INF, hay varias funciones de control de archivos que puede usar para instalar los archivos enumerados en una sección INF. Las funciones de bajo nivel, [**como SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea) [**y SetupInstallFileEx,**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa) instalan un único archivo.

También hay funciones para controlar archivos comprimidos. La [**función SetupGetFileCompressionInfo**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetfilecompressioninfoa) devuelve información sobre los archivos comprimidos. Después, [**SetupDecompressOrCopyFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupdecompressorcopyfilea) puede usar esta información para copiar y, si es necesario, expandir el archivo.

Las funciones de alto nivel como [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona), [**SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona)y [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) procesan las operaciones de instalación en una sección Instalación **o servicio.**  De estas, **SetupInstallFromInfSection** es la más versátil porque puede realizar  cualquier tipo de operación de instalación que se muestra en la sección Instalación de un archivo INF. Esto incluye las operaciones de registro e INI enumeradas en las líneas **AddReg**, **DelReg,** **UpdateInis** o **UpdateIniField** de una **sección Install.**

Las [**funciones SetupInstallFilesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilesfrominfsectiona) y [**SetupInstallServicesFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallservicesfrominfsectiona) ponen en cola las operaciones desde una sección **Install** o **Service,** respectivamente, a una cola de archivos existente. Tenga en cuenta que debe llamar a SetupInstallFromInfSection y SetupInstallServicesFromInfSection por separado para las operaciones y servicios de cola. Para obtener más información, vea [Colas de archivos](file-queues.md).

En cambio, la [**función SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) crea y destruye su propia cola interna. Un uso común de **SetupInstallFromInfSection** es llamarlo después de que todos los archivos se hayan copiado correctamente para realizar las transacciones del Registro y del INI.

En Windows 2000, los archivos DLL pueden registrarse automáticamente mediante una llamada a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) en un archivo INF que incluye la directiva **RegisterDlls** en su **sección Install.** **SetupInstallFromInfSection también** puede registrar archivos DLL de 32 bits de forma independiente desde un proceso de 64 bits.

En sistemas operativos de 64 bits, se puede llamar a [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) para realizar operaciones en la parte de 32 bits del registro. Para agregar una clave del Registro a la parte de 32 bits del registro, incluya la marca \_ FLG ADDREG \_ 32BITKEY en la **línea AddReg** del INF. Para eliminar una clave del Registro solo en la parte de 32 bits del registro, incluya la clave \_ FLG DELREG \_ 32BITKEY en la **línea DelReg.** Para establecer o borrar un valor binario solo en la parte de 32 bits del registro, incluya FLG \_ BITREG \_ 32BITKEY en la **línea BitReg.**

Además de las funciones enumeradas anteriormente, la API de instalación incluye funciones que ponen en cola las operaciones de instalación de archivos, ya sea por archivo o por sección INF. Para obtener más información, vea [Colas de archivos](file-queues.md).

 

 



