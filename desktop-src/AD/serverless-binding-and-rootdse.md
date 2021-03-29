---
title: Enlace sin servidor y RootDSE
description: Si es posible, no codifique un nombre de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Enlace sin servidor y AD de RootDSE
- Enlace sin servidor AD
- AD de RootDSE
- Active Directory, uso, enlace, enlace sin servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487403"
---
# <a name="serverless-binding-and-rootdse"></a>Enlace sin servidor y RootDSE

Si es posible, no codifique un nombre de servidor. Además, en la mayoría de los casos, el enlace no debe estar asociado innecesariamente a un solo servidor. Active Directory Domain Services admiten el enlace sin servidor, lo que significa que Active Directory se pueden enlazar a en el dominio predeterminado sin especificar el nombre de un controlador de dominio. En el caso de las aplicaciones normales, suele ser el dominio del usuario que ha iniciado sesión. En el caso de las aplicaciones de servicio, es el dominio de la cuenta de inicio de sesión del servicio o el del cliente que suplanta el servicio.

En LDAP 3,0, rootDSE se define como la raíz del árbol de datos de directorio en un servidor de directorio. RootDSE no forma parte de ningún espacio de nombres. El propósito de rootDSE es proporcionar datos sobre el servidor de directorio. A continuación se encuentra la cadena de enlace que se utiliza para enlazar a rootDSE.


```C++
LDAP://<servername>/rootDSE
```



<servername>Es el nombre DNS de un servidor. <servername>Es opcional, como se muestra en el siguiente formato.


```C++
LDAP://rootDSE
```



En este caso, se utilizará un controlador de dominio predeterminado del dominio en el que se encuentra el contexto de seguridad del subproceso que realiza la llamada. Si no se puede tener acceso a un controlador de dominio en el sitio, se utilizará el primer controlador de dominio que se pueda encontrar.

RootDSE es una ubicación conocida y confiable en cada servidor de directorio para obtener nombres distintivos de los contenedores de dominio, esquema y configuración, y otros datos sobre el servidor y el contenido de su árbol de datos de directorio. Estas propiedades rara vez cambian en un servidor determinado. Una aplicación puede leer estas propiedades en el inicio y usarlas en toda la sesión.

En Resumen, una aplicación debe usar el enlace sin servidor para enlazar con el directorio en el dominio actual, usar rootDSE para obtener el nombre distintivo de un espacio de nombres y usar ese nombre distintivo para enlazar con los objetos del espacio de nombres.

Para obtener más información acerca de los atributos admitidos por rootDSE, consulte [RootDSE](/windows/desktop/ADSchema/rootdse) en la documentación del esquema de Active Directory.

Para obtener más información y un ejemplo de código que muestra cómo usar el enlace sin servidor y rootDSE, consulte [el código de ejemplo para obtener el nombre distintivo del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 