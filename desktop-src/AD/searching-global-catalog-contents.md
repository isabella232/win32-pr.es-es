---
title: Buscar en el catálogo global
description: Active Directory Domain Services también tienen un catálogo global (GC), que contiene una réplica parcial de todos los objetos del directorio.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- Buscar en el catálogo global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773093"
---
# <a name="searching-the-global-catalog"></a>Buscar en el catálogo global

Active Directory Domain Services también tienen un catálogo global (GC), que contiene una réplica parcial de todos los objetos del directorio. También contiene réplicas parciales del esquema y los contenedores de configuración. Uno o varios controladores de dominio de un dominio pueden contener una copia del catálogo global. Para obtener más información sobre cómo enlazar a un catálogo global, vea [enlazar con el catálogo global](binding-to-the-global-catalog.md).

El catálogo global contiene una réplica de cada objeto en Active Directory Domain Services, pero solo con un número pequeño de sus atributos. Los atributos del catálogo global son los que se usan con más frecuencia en las operaciones de búsqueda, como el nombre y los apellidos de un usuario, los nombres de inicio de sesión, etc. Los atributos del catálogo global también incluyen los necesarios para buscar una réplica completa del objeto. El catálogo global permite a los usuarios encontrar rápidamente objetos de interés sin saber qué dominio los contiene y sin necesidad de un espacio de nombres extendido contiguo en la empresa. es decir, puede buscar en todo el bosque.

Por lo tanto, si se enlaza a un objeto en el catálogo global, buscará ese objeto y toda la jerarquía debajo de él, sin tener que ir a ningún otro servidor. Sin embargo, la búsqueda solo puede utilizar un filtro de consulta que contenga propiedades en el catálogo global y solo puede recuperar propiedades en el catálogo global.

La búsqueda en el catálogo global presenta las siguientes ventajas:

-   El catálogo global permite buscar en todo el bosque o en cualquier parte del bosque, así como en el esquema y los contenedores de configuración.
-   El catálogo global permite realizar una búsqueda completa en un solo servidor. No es necesario realizar referencias ni el seguimiento de la referencia.

La búsqueda en el catálogo global tiene las siguientes desventajas:

-   El catálogo global contiene un pequeño subconjunto de las propiedades de cada objeto. Si el filtro de consulta incluye propiedades que no están en el catálogo global, la consulta evaluará las expresiones que contienen esas propiedades como false. Si especifica propiedades de catálogo no globales en la lista de propiedades que se van a devolver, dichas propiedades no se recuperan.
-   Para buscar en el catálogo global, debe haber disponible un controlador de dominio que contenga un catálogo global. Si no hay ninguno disponible, no se puede realizar una búsqueda en el catálogo global.
-   El catálogo global es de solo lectura. Esto significa que no se puede enlazar a un objeto en el catálogo global para crear, modificar o eliminar objetos.

 

 




