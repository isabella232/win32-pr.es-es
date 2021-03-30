---
title: Enumerar grupos en un dominio
description: Los grupos se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio.
ms.assetid: 7f9d3c90-b6f4-4bfa-960f-58f380aa487c
ms.tgt_platform: multiple
keywords:
- Enumerar grupos en un dominio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3586b8c6d261c769cabe56def2aa9396a58fa3a5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789573"
---
# <a name="enumerating-groups-in-a-domain"></a>Enumerar grupos en un dominio

Los grupos se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio. Esto significa que los grupos pueden estar en varias ubicaciones en la jerarquía de directorios. Por lo tanto, tiene dos opciones para enumerar los grupos:

1.  Enumerar los grupos contenidos directamente en un contenedor, una unidad organizativa o en la raíz del dominio.

    Enlace explícitamente al objeto contenedor que contiene los grupos que se van a enumerar, establezca un filtro que contenga "groups" como la clase mediante la propiedad [**IADsContainer. Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) y use el método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar los objetos de grupo.

    Esta técnica enumera los grupos contenidos directamente en un contenedor o un objeto de unidad organizativa. Si el contenedor contiene otros contenedores que pueden contener otros grupos, debe enlazar a esos contenedores y enumerar de forma recursiva los grupos en esos contenedores. Para manipular los objetos de grupo y leer solo las propiedades específicas, use la búsqueda en profundidad que se describe en la opción 2.

    Dado que la enumeración devuelve punteros a objetos COM ADSI que representan cada objeto de grupo, puede llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener punteros de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)y [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) al objeto de grupo; es decir, puede obtener punteros de interfaz a cada objeto de grupo enumerado en un contenedor sin tener que enlazar explícitamente a cada objeto de grupo. Para realizar operaciones en todos los grupos directamente dentro de un contenedor, la enumeración no requiere un enlace a cada grupo para llamar a métodos **IADs** o **IADsGroup** . Para recuperar propiedades específicas de los grupos, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) tal y como se describe en la segunda opción.

    Se produce una excepción cuando se intenta enumerar un grupo que contiene miembros que son entidades de seguridad conocida, como todos, usuarios autenticados, lote, etc. Dado que no se puede enlazar a estos tipos de objetos, no se enumeran al enumerar los grupos en el ámbito de WinNT, aunque puede parecer que se enlazan, porque ciertos métodos de IADs, como class, ADsPath y Name, devuelven resultados correctos cuando se invocan en miembros enumerados.

2.  Realice una búsqueda en profundidad de "objectCategory = grupo" para buscar todos los grupos de un árbol.

    En primer lugar, enlace al objeto contenedor en el que va a comenzar la búsqueda. Por ejemplo, para buscar todos los grupos de un dominio, enlace a la raíz del dominio; para buscar todos los grupos del bosque, enlace al catálogo global y busque desde la raíz del GC.

    A continuación, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar mediante un filtro de búsqueda que contenga (objectCategory = grupo) y la preferencia de búsqueda del **\_ \_ subárbol del ámbito de ADS**.

    > [!Note]  
    > Puede realizar una búsqueda con una preferencia de búsqueda del **ámbito de ADS \_ \_ onelevel** para limitar la búsqueda al contenido directo del objeto contenedor al que se ha enlazado.

     

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) solo recupera los valores de propiedades específicas de los grupos. Para recuperar valores, use **IDirectorySearch**. Para manipular los objetos de grupo devueltos por una búsqueda, es decir, para usar métodos [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) , enlace explícitamente a ellos. Para ello, especifique **distinguishedName** como una de las propiedades que se van a devolver de la búsqueda y use los nombres distintivos devueltos para enlazar con cada grupo devuelto en la búsqueda.

    Solo se recuperan las propiedades específicas. No se pueden recuperar todos los atributos sin especificar explícitamente cada atributo posible de la clase de grupo.

 

 