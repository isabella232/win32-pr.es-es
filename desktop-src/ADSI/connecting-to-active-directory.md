---
title: Conexión a Active Directory
description: Hay varios métodos que se usan para tener acceso a Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Conectarse a Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993865"
---
# <a name="connecting-to-active-directory"></a>Conexión a Active Directory

Hay varios métodos que se usan para tener acceso a Active Directory. Se recomienda usar la API ADSI para tener acceso a Active Directory. ADSI implementa el protocolo LDAP para comunicarse con Active Directory. En los siguientes ejemplos de código se muestra cómo obtener acceso a Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Esto abre el proveedor LDAP y lo prepara para recuperar los datos. No se establece ninguna conexión hasta que se soliciten los datos. Cuando se solicitan datos, ADSI, con la ayuda del servicio de ubicación, intenta encontrar el mejor controlador de dominio (DC) para la conexión y establecerá una conexión con el servidor. Este proceso se conoce como enlace sin servidor.

ADSI también permite especificar el nombre del servidor que se va a utilizar para la conexión.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



En otro escenario, es posible que solo conozca el nombre de dominio, pero no el nombre de servidor específico. De nuevo, ADSI le permite especificar el nombre de dominio. En Windows 2000, el nombre de dominio se representa como un nombre DNS. Por ejemplo, si Joe Worden, el administrador de red elige conectarse con el nombre de dominio, podría usar el siguiente ejemplo de código.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI se conectará a uno de los controladores de dominio del dominio fabrikam.com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlazar a objetos de Active Directory](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




