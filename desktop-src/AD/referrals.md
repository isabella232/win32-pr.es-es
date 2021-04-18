---
title: Referencias (AD DS)
description: Active Directory Domain Services mantener los datos de referencia en objetos crossRef almacenados en el contenedor de particiones (crossRefContainer) en el contenedor de configuración.
ms.assetid: e4d6cc8a-9c2c-4e0f-acca-e9ecdd5e879b
ms.tgt_platform: multiple
keywords:
- AD de referencias
- Active Directory, referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63c87fb0248d85ab20191296f9659eb58e460f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656326"
---
# <a name="referrals-ad-ds"></a>Referencias (AD DS)

Active Directory Domain Services mantener los datos de referencia en objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) almacenados en el contenedor de particiones ([**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer)) en el contenedor de configuración. En el tema [decidir dónde buscar](where-to-search.md) , las referencias se describen en el contexto de un dominio dentro de un árbol de dominios y la generación de referencias a dominios subordinados en una búsqueda de subárbol.

Active Directory Domain Services crear y mantener objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) para todos los dominios del bosque. Además, hay objetos **crossRef** para los contenedores de configuración y de esquema. Estos objetos **crossRef** se utilizan para generar referencias en respuesta a las consultas que solicitan datos sobre los objetos que existen en el bosque, pero no se incluyen en el servidor de directorio que controla la solicitud. Se denominan *referencias cruzadas internas*, porque hacen referencia a los dominios, esquemas y contenedores de configuración del bosque.

Si no está habilitado el seguimiento de referencias y se realiza una búsqueda de subárbol, la búsqueda devolverá todos los objetos del dominio especificado que cumplan los criterios de búsqueda. La búsqueda también devolverá referencias a cualquier dominio subordinado que sea descendiente directo del dominio del servidor de directorio. El cliente debe resolver las referencias enlazando a la ruta de acceso especificada por la referencia y enviando otra consulta.

Si está activado el seguimiento de referencia y se realiza una búsqueda de subárbol, la API de LDAP subyacente intentará enlazar automáticamente con cualquier referencia y agregar los resultados de la búsqueda al conjunto de resultados. En la mayoría de los casos, el seguimiento de la referencia será transparente para el autor de la llamada. Si la referencia es a un objeto de un dominio o bosque diferente, la API de LDAP subyacente intentará utilizar las credenciales actuales para enlazar con el destino de la referencia. Si esto se realiza correctamente, el seguimiento de la referencia será transparente. Si no se realiza correctamente, se devolverá el código de error de referencia y de referencia.

Para obtener más información sobre la configuración de las preferencias de búsqueda para el seguimiento de referencias, vea [especificar otras opciones de búsqueda](specifying-other-search-options.md).

Además de las propiedades [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) (nombre DNS del dominio) y [**NCName**](/windows/desktop/ADSchema/a-ncname) (nombre distintivo para el dominio), el objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) también contiene el **nETBIOSName** (nombre NetBIOS del dominio) y **trustParent** (nombre distintivo del objeto **crossRef** que representa las propiedades del dominio primario directo del dominio).

Active Directory Domain Services también pueden tener *referencias cruzadas externas* que hacen referencia a objetos fuera del bosque. Un administrador debe agregar explícitamente las referencias cruzadas externas. Tenga en cuenta que el servidor de destino de la referencia cruzada externa debe tener una raíz DNS; es decir, debe adherirse a RFC 2247.

Una referencia cruzada externa hace referencia a un objeto de cualquier otro bosque, siempre que el nombre sea único en el bosque de destino. Por ejemplo, las aplicaciones cliente LDAP que usa su empresa pueden enviar operaciones a los servidores de directorio para Fabrikam.com. Cree un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para fabrikam.com. Ahora, en lugar de devolver un error de objeto no encontrado, los servidores de directorio pueden devolver una referencia a un objeto en el dominio Fabrikam.com y los clientes pueden hacer el seguimiento de la referencia. Por ejemplo, si tiene un objeto con el siguiente nombre distintivo:


```C++
CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Puede Agregar una referencia cruzada externa para un objeto con el nombre "ChildOfSomeObject".


```C++
CN=ChildOfSomeObject,CN=SomeObject,OU=SomeOU,DC=Fabrikam,DC=Com
```



Una búsqueda de subárbol que contenga "objeto" también devolverá una referencia a "ChildOfSomeObject". Tenga en cuenta que debe haber un servidor LDAP en la dirección especificada por la referencia (una de las propiedades del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) ) y que este servidor LDAP debe proporcionar el espacio de nombres identificado por "ChildOfSomeObject".

Dado que los objetos [**crossRef**](/windows/desktop/ADSchema/c-crossref) se almacenan en el contenedor de configuración, cada controlador de dominio (DC) tiene una copia de todos los objetos **crossRef** . Por lo tanto, cada DC contiene datos sobre cada dominio del bosque, así como sus relaciones superiores/subordinadas. Esto permite que cada controlador de dominio genere referencias a cualquier dominio del bosque y las referencias para los contenedores de dominio subordinado, de esquema o de configuración no explorados en una búsqueda de subárbol.

Para obtener más información sobre las referencias, vea:

-   [Cuándo se generan las referencias](when-referrals-are-generated.md)
-   [Crear una referencia externa](creating-an-external-referral.md)

Para obtener más información y un ejemplo de código que muestra cómo obtener el nombre distintivo del contenedor de particiones, consulte [el código de ejemplo para buscar el contenedor de particiones](example-code-for-locating-the-partitions-container.md).

 

 