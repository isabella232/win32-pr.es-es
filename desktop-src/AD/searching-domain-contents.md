---
title: Buscar en el contenido del dominio
description: Antes de explicar dónde enlazar para iniciar una búsqueda de objetos en un dominio, es útil entender cómo se almacenan los datos en Active Directory Domain Services.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- Active Directory del contenido del dominio
- Buscar en el contenido del dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c18cd879e950fd9c467f6674092947d430d8f87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075105"
---
# <a name="searching-domain-contents"></a>Buscar en el contenido del dominio

Antes de explicar dónde enlazar para iniciar una búsqueda de objetos en un dominio, es útil entender cómo se almacenan los datos en Active Directory Domain Services.

Si tiene un bosque con más de un dominio, Active Directory Domain Services no almacena todos los datos de objetos en un solo controlador de dominio, por motivos de rendimiento, escalabilidad y confiabilidad. Un controlador de dominio contiene toda la información sobre solo el dominio del que es miembro (tiene una réplica completa del dominio). Sin embargo, un controlador de dominio no contiene información completa sobre ningún otro dominio.

Si se enlaza al objeto de dominio con el uso de referencia desactivado, puede buscar cualquier objeto de ese dominio y solo ese dominio. Para obtener más información sobre el seguimiento de referencias, vea [Referrals](referrals.md). Una búsqueda puede recuperar cualquier propiedad y puede usar un filtro de consulta que contenga cualquier propiedad.

En un bosque, los dominios se organizan jerárquicamente como árboles de dominio. Un árbol de dominios puede ser simplemente un dominio único o un dominio con uno o varios dominios secundarios. Estos dominios secundarios, a su vez, pueden tener dominios secundarios por debajo de ellos. Un árbol de dominios también es un espacio de nombres contiguo. Un espacio de nombres contiguo significa que los dominios secundarios son una continuación de la jerarquía de nomenclatura. Por ejemplo, un dominio fabrikam.com (o DC = Fabrikam, DC = COM) puede tener un dominio secundario llamado mydivision.fabrikam.com o DC =, DC = Fabrikam, DC = COM, que a su vez podría tener un dominio secundario denominado mydev (mydev.mydivision.fabrikam.com o DC = mydev, DC =, DC = Fabrikam, DC = COM).

Si enlaza a un objeto de dominio (con el seguimiento de referencia activado) para un dominio dentro de un árbol de dominios, buscará ese dominio y toda la jerarquía dentro de él. La búsqueda puede recuperar cualquier propiedad y puede usar un filtro de consulta que contenga cualquier propiedad.

Si un controlador de dominio contiene una réplica completa de solo su propio dominio, puede realizar una búsqueda de subárbol en un árbol de dominios. Un dominio contiene referencias a sus dominios secundarios. Cuando un controlador de dominio procesa una solicitud de búsqueda de subárbol en su propio dominio, el controlador de dominio busca en ese dominio y, a continuación, devuelve las referencias a cada uno de sus dominios secundarios al cliente. Una referencia es la forma en que un servidor de directorio comunica que no contiene la información necesaria para completar una solicitud (por ejemplo, una consulta) pero tiene una referencia a un servidor que puede contener la información necesaria. En el caso de una búsqueda de subárbol de un árbol de dominios, se devuelve una referencia para cada dominio secundario directo, de modo que la búsqueda pueda continuar en un controlador de dominio de cada dominio secundario. Si está activado el seguimiento de referencias, la biblioteca de cliente LDAP (Wldap32.dll) utiliza esas referencias para enlazar con un controlador de dominio en cada dominio secundario y continuar la búsqueda. Si el seguimiento de referencia está desactivado, el cliente LDAP no resuelve las referencias y la búsqueda se completa.

Una búsqueda de subárbol en un árbol de dominios con el seguimiento de referencia activado puede llevar mucho tiempo si hay una conexión lenta a los controladores de dominio de los dominios secundarios. Si desea buscar un solo dominio, debe activar la opción de referencia para evitar tener que buscar los dominios secundarios innecesariamente.

 

 




