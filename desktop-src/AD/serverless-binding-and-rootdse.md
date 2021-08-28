---
title: Enlace sin servidor y RootDSE
description: Si es posible, no codifie de forma hard-code un nombre de servidor.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Enlace sin servidor y RootDSE AD
- AD de enlace sin servidor
- RootDSE AD
- Active Directory, Using, Binding, Serverless Binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a2b567ebfae52a316dce59c3bc6ab442780e61
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881224"
---
# <a name="serverless-binding-and-rootdse"></a>Enlace sin servidor y RootDSE

Si es posible, no codifie de forma hard-code un nombre de servidor. Además, en la mayoría de las circunstancias, el enlace no debe asociarse innecesariamente a un único servidor. Active Directory Domain Services enlace sin servidor, lo que significa Active Directory se puede enlazar a en el dominio predeterminado sin especificar el nombre de un controlador de dominio. En el caso de las aplicaciones normales, suele ser el dominio del usuario que ha iniciado sesión. Para las aplicaciones de servicio, este es el dominio de la cuenta de inicio de sesión del servicio o el del cliente que suplanta el servicio.

En LDAP 3.0, rootDSE se define como la raíz del árbol de datos de directorio en un servidor de directorios. RootDSE no forma parte de ningún espacio de nombres. El propósito de rootDSE es proporcionar datos sobre el servidor de directorios. A continuación se muestra la cadena de enlace que se usa para enlazar a rootDSE.


```C++
LDAP://<servername>/rootDSE
```



Servername &lt; es el nombre DNS de un &gt; servidor. &lt;Servername &gt; es opcional, como se muestra en el formato siguiente.


```C++
LDAP://rootDSE
```



En este caso, se usará un controlador de dominio predeterminado del dominio en el que se encuentra el contexto de seguridad del subproceso que realiza la llamada. Si no se puede acceder a un controlador de dominio dentro del sitio, se usará el primer controlador de dominio que se pueda encontrar.

RootDSE es una ubicación conocida y confiable en cada servidor de directorio para obtener nombres distintivos de los contenedores de dominio, esquema y configuración, y otros datos sobre el servidor y el contenido de su árbol de datos de directorio. Estas propiedades rara vez cambian en un servidor determinado. Una aplicación puede leer estas propiedades en el inicio y usarlas a lo largo de la sesión.

En resumen, una aplicación debe usar el enlace sin servidor para enlazar con el directorio del dominio actual, usar rootDSE para obtener el nombre distintivo de un espacio de nombres y usar ese nombre distintivo para enlazar a los objetos del espacio de nombres.

Para obtener más información sobre los atributos admitidos por rootDSE, vea [RootDSE](/windows/desktop/ADSchema/rootdse) en la documentación Active Directory schema.

Para obtener más información y un ejemplo de código que muestra cómo usar el enlace sin servidor y rootDSE, vea Código de ejemplo para obtener el nombre distintivo [del dominio](example-code-for-getting-the-distinguished-name-of-the-domain.md).

 

 
