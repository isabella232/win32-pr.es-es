---
title: Conexión a Active Directory
description: Hay varios métodos que se usan para acceder a Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Conexión a Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6afd5aa0edd8a4c4a87bae7cde6a135fc3467771eed2dbc0cb7673984040832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692013"
---
# <a name="connecting-to-active-directory"></a>Conexión a Active Directory

Hay varios métodos que se usan para acceder a Active Directory. Se recomienda usar la API adsi para acceder a Active Directory. ADSI implementa el protocolo LDAP para comunicarse con Active Directory. En los ejemplos de código siguientes se muestra cómo acceder a Active Directory.


```VB
Set ns = GetObject("LDAP:")
```



Esto abre el proveedor LDAP y lo prepara para recuperar datos. No se establece ninguna conexión hasta que se solicitan los datos. Cuando se solicitan datos, ADSI, con la ayuda del servicio de localizador, intenta encontrar el mejor controlador de dominio (DC) para la conexión y establecerá una conexión con el servidor. Este proceso se conoce como enlace sin servidor.

ADSI también permite especificar el nombre del servidor que se va a usar para la conexión.


```VB
Set obj = GetObject("LDAP://mysrv01")
```



En otro escenario, es posible que solo conozca el nombre de dominio, pero no el nombre de servidor específico. De nuevo, ADSI le permite especificar el nombre de dominio. En Windows 2000, el nombre de dominio se representa como un nombre DNS. Por ejemplo, si Joe Worden, el administrador de red, decide conectarse con el nombre de dominio, podría usar el siguiente ejemplo de código.


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI se conectará a uno de los controladores de dominio del fabrikam.com dominio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Enlace a Active Directory objetos](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




