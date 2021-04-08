---
description: Puede controlar la capacidad de un proceso para tener acceso a objetos protegibles o para realizar tareas de administración del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificación de un descriptor de seguridad de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002962"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Especificación de un descriptor de seguridad de un archivo INF

Puede controlar la capacidad de un proceso para tener acceso a objetos protegibles o para realizar tareas de administración del sistema. Un objeto protegible es un objeto que puede tener un descriptor de seguridad. Todos los objetos con nombre son protegibles. Algunos objetos sin nombre, como los objetos de proceso y de subprocesos, también pueden tener descriptores de seguridad. Para obtener más información sobre cómo controlar el acceso a los objetos protegibles, vea [Access Control](/windows/desktop/SecAuthZ/access-control).

Los [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors) contienen la información de seguridad asociada a los objetos protegibles. Para la mayoría de los objetos protegibles, puede especificar el descriptor de seguridad de un objeto en la llamada de función que crea el objeto. Por ejemplo, puede especificar un descriptor de seguridad en las funciones [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) y [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Para establecer un descriptor de seguridad a partir de un archivo INF, agregue una sección de seguridad creada por el archivo INF-Writer inmediatamente después de la sección que instala el archivo, la clave del registro o el componente. La sección de seguridad debe contener una línea con el descriptor de seguridad de cadena escrito en ella con el formato de las [cadenas de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-strings). La línea también debe incluirse entre comillas (").

Por ejemplo, el siguiente fragmento de archivo INF crearía una clave del registro a la que solo los administradores y el sistema tienen acceso. Tenga en cuenta que este ejemplo requiere privilegios administrativos.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

En este caso, el significado de la cadena es que los administradores tienen control total, el sistema tiene control total y el acceso se puede heredar en todas las subclaves. Para obtener más información, consulte [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
