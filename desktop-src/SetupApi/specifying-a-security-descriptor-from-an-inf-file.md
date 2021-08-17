---
description: Puede controlar la capacidad de un proceso para acceder a objetos protegibles o para realizar tareas de administración del sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificar un descriptor de seguridad a partir de un archivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52267f443bf20fe8a9b71a64e2422ac43688d7a54bca2692f1b61ad891fda8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964841"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a>Especificar un descriptor de seguridad a partir de un archivo INF

Puede controlar la capacidad de un proceso para acceder a objetos protegibles o para realizar tareas de administración del sistema. Un objeto protegible es un objeto que puede tener un descriptor de seguridad. Todos los objetos con nombre son protegibles. Algunos objetos sin nombre, como los objetos de proceso y subproceso, también pueden tener descriptores de seguridad. Para obtener más información sobre cómo controlar el acceso a objetos protegibles, [vea Access Control](/windows/desktop/SecAuthZ/access-control).

[Los descriptores de](/windows/desktop/SecAuthZ/security-descriptors) seguridad contienen la información de seguridad asociada a los objetos protegibles. Para la mayoría de los objetos protegibles, puede especificar el descriptor de seguridad de un objeto en la llamada de función que crea el objeto. Por ejemplo, puede especificar un descriptor de seguridad en las [**funciones CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**y CreateProcess.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Para establecer un descriptor de seguridad a partir de un archivo INF, agregue una sección Seguridad de autor de INF-writer inmediatamente después de la sección que instala el archivo, la clave del Registro o el componente. La sección Seguridad debe contener una línea con el descriptor de seguridad de cadena escrito en él con el formato de [Cadenas de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-strings). La línea también debe ir entre comillas (").

Por ejemplo, el siguiente fragmento de código de archivo INF crearía una clave del Registro a la que solo tienen acceso los administradores y el sistema. Tenga en cuenta que este ejemplo requiere privilegios administrativos.

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

En este caso, el significado de la cadena es que los administradores tienen control total, el sistema tiene control total y el acceso se puede heredar a todas las subclaves. Para obtener más información, vea [Lenguaje de definición de descriptor de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language).

 

 
