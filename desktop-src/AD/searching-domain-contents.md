---
title: Buscar contenido del dominio
description: Antes de analizar dónde enlazar para iniciar una búsqueda de objetos en un dominio, es útil comprender cómo se almacenan los datos en Active Directory Domain Services.
ms.assetid: fd0b4556-465b-4338-87cb-375450590c44
ms.tgt_platform: multiple
keywords:
- contenido del dominio Active Directory
- buscar contenido de dominio Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51f775e199cd269eec8a67054ca26bcd69e11eacaa6436781f4481083d11e60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118183880"
---
# <a name="searching-domain-contents"></a>Buscar contenido del dominio

Antes de analizar dónde enlazar para iniciar una búsqueda de objetos en un dominio, es útil comprender cómo se almacenan los datos en Active Directory Domain Services.

Si tiene un bosque con más de un dominio, Active Directory Domain Services no almacena todos los datos de objeto en un solo controlador de dominio, por motivos de rendimiento, escalabilidad y confiabilidad. Un controlador de dominio contiene toda la información sobre solo el dominio del que es miembro (tiene una réplica completa del dominio). Pero un controlador de dominio no contiene información completa sobre ningún otro dominio.

Si enlaza al objeto de dominio con la búsqueda de referencias desactivada, puede buscar cualquier objeto de ese dominio y solo ese dominio. Para obtener más información sobre la búsqueda de referencias, vea [Referencias.](referrals.md) Una búsqueda puede recuperar cualquier propiedad y puede usar un filtro de consulta que contenga cualquier propiedad.

En un bosque, los dominios se organizan jerárquicamente como árboles de dominio. Un árbol de dominio puede ser solo un dominio o un dominio con uno o varios dominios secundarios. Estos dominios secundarios, a su vez, pueden tener dominios secundarios debajo de ellos. Un árbol de dominio también es un espacio de nombres contiguo. Un espacio de nombres contiguo significa que los dominios secundarios son una continuación de la jerarquía de nomenclatura. Por ejemplo, un dominio fabrikam.com (o DC=Fabrikam, DC=COM) puede tener un dominio secundario denominado mydivision (mydivision.fabrikam.com o DC=mydivision, DC=Fabrikam, DC=COM), que a su vez podría tener un dominio secundario denominado mydev (mydev.mydivision.fabrikam.com o DC=mydev, DC=mydivision, DC=Fabrikam, DC=COM).

Si enlaza a un objeto de dominio (con la búsqueda de referencias activada) para un dominio dentro de un árbol de dominio, buscará ese dominio y toda la jerarquía dentro de él. La búsqueda puede recuperar cualquier propiedad y puede usar un filtro de consulta que contenga cualquier propiedad.

Si un controlador de dominio contiene una réplica completa de solo su propio dominio, puede realizar una búsqueda de subárbol en un árbol de dominio. Un dominio contiene referencias a sus dominios secundarios. Cuando un controlador de dominio procesa una solicitud de búsqueda de subárbol en su propio dominio, el controlador de dominio busca ese dominio y, a continuación, devuelve referencias a cada uno de sus dominios secundarios al cliente. Una referencia es la manera en que un servidor de directorio comunica que no contiene la información necesaria para completar una solicitud (como una consulta), pero tiene una referencia a un servidor que puede contener la información necesaria. En el caso de una búsqueda de subárbol de un árbol de dominio, se devuelve una referencia para cada dominio secundario directo para que la búsqueda pueda continuar en un controlador de dominio en cada dominio secundario. Si la búsqueda de referencias está activada, la biblioteca cliente LDAP (Wldap32.dll) usa esas referencias para enlazarse a un controlador de dominio en cada dominio secundario y continuar la búsqueda. Si la búsqueda de referencias está desactivada, el cliente LDAP no resuelve las referencias y la búsqueda se completa.

Una búsqueda de subárbol en un árbol de dominio con la búsqueda de referencias activada puede llevar mucho tiempo si hay una conexión lenta a los controladores de dominio para los dominios secundarios. Si solo desea buscar un dominio único, debe desactivar la búsqueda de referencias para evitar tener que buscar innecesariamente en los dominios secundarios.

 

 




