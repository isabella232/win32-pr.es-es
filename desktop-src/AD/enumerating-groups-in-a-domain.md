---
title: Enumerar grupos en un dominio
description: Los grupos se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Enumeración de grupos en un dominio de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3723122ef2ab70a7396b2b2821c96a20b4d92419c1e10d1c00b11ff903cb6719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429851"
---
# <a name="enumerating-groups-in-a-domain"></a>Enumerar grupos en un dominio

Los grupos se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio. Esto significa que los grupos pueden estar en numerosas ubicaciones de la jerarquía de directorios. Por lo tanto, tiene dos opciones para enumerar grupos:

1.  Enumerar los grupos contenidos directamente en un contenedor, una unidad organizativa o en la raíz del dominio.

    Enlace explícitamente al objeto contenedor que contiene los grupos que se deben enumerar, establezca un filtro que contenga "groups" como clase mediante la propiedad [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) y use el método [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar los objetos de grupo.

    Esta técnica enumera los grupos contenidos directamente en un contenedor u objeto de unidad organizativa. Si el contenedor contiene otros contenedores que pueden contener otros grupos, debe enlazar a esos contenedores y enumerar de forma recursiva los grupos de esos contenedores. Para manipular los objetos de grupo y leer solo propiedades específicas, use la búsqueda en profundidad descrita en opción 2.

    Dado que la enumeración devuelve punteros a objetos COM ADSI que representan cada objeto de grupo, puede llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener los punteros de interfaz [**IADs,**](/windows/desktop/api/iads/nn-iads-iads) [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) al objeto de grupo; Es decir, puede obtener punteros de interfaz a cada objeto de grupo enumerado en un contenedor sin tener que enlazar explícitamente a cada objeto de grupo. Para realizar operaciones en todos los grupos directamente dentro de un contenedor, la enumeración no requiere el enlace a cada grupo para llamar a los **métodos IADs** o **IADsGroup.** Para recuperar propiedades específicas de grupos, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) como se describe en la segunda opción.

    Una excepción a esto se produce cuando se intenta enumerar un grupo que contiene miembros que son entidades de seguridad wellKnown, como Todos, Usuarios autenticados, BATCH, y así sucesivamente. Dado que no se puede enlazar a estos tipos de objetos, no se muestran al enumerar grupos en el ámbito winNT, aunque parezca que se enlazan, porque ciertos métodos de IAD como Class, ADsPath y Name devuelven resultados correctos cuando se invocan en miembros enumerados.

2.  Realice una búsqueda en profundidad de "objectCategory=group" para buscar todos los grupos de un árbol.

    En primer lugar, enlace al objeto contenedor donde se va a iniciar la búsqueda. Por ejemplo, para buscar todos los grupos de un dominio, enlace a la raíz del dominio; para buscar todos los grupos del bosque, enlace al catálogo global y busque desde la raíz del GC.

    A [**continuación, use IDirectorySearch para**](/windows/desktop/api/iads/nn-iads-idirectorysearch) realizar consultas mediante un filtro de búsqueda que contenga (objectCategory=group) y la preferencia de búsqueda de **ADS SCOPE \_ \_ SUBTREE**.

    > [!Note]  
    > Puede realizar una búsqueda con una preferencia de búsqueda de **ADS \_ SCOPE \_ ONELEVEL** para limitar la búsqueda al contenido directo del objeto contenedor al que se enlaza.

     

    [**IDirectorySearch recupera**](/windows/desktop/api/iads/nn-iads-idirectorysearch) solo los valores de propiedades específicas de los grupos. Para recuperar valores, use **IDirectorySearch**. Para manipular los objetos de grupo devueltos desde una búsqueda, es decir, para usar los [**métodos IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsGroup,**](/windows/desktop/api/iads/nn-iads-iadsgroup) se enlazan explícitamente a ellos. Para ello, especifique **distinguishedName** como una de las propiedades que se devolverán de la búsqueda y use los nombres distintivos devueltos para enlazar a cada grupo devuelto en la búsqueda.

    Solo se recuperan propiedades específicas. No se pueden recuperar todos los atributos sin especificar explícitamente todos los atributos posibles de la clase de grupo.

 

 