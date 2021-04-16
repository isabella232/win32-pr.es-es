---
title: Enumerar usuarios
description: A diferencia de los dominios de Windows NT 4,0, los usuarios de Windows 2000 se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumerar AD de usuarios
- usuarios AD, enumeración de un usuario
- Active Directory, uso, usuarios, enumeración de un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e922d92f4313ed0238ff068f7ae1c0fbf693d497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656349"
---
# <a name="enumerating-users"></a>Enumerar usuarios

A diferencia de los dominios de Windows NT 4,0, los usuarios de Windows 2000 se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio. Esto significa que los usuarios pueden estar en varias ubicaciones en la jerarquía de directorios. Por lo tanto, tiene dos opciones para enumerar los usuarios:

-   Enumerar los usuarios que se encuentran directamente en un contenedor, una unidad organizativa o en la raíz del dominio:

    Enlace explícitamente al objeto contenedor que contiene los usuarios que está interesado en enumerar, establezca un filtro que contenga "User" como la clase mediante la propiedad [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) y use el método [**IADsContainer:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar los objetos de usuario.

    Esta técnica se puede usar para enumerar los usuarios que están contenidos directamente en un contenedor o un objeto de unidad organizativa. Si el contenedor contiene otros contenedores que pueden contener otros usuarios, debe enlazar a esos contenedores y enumerar de forma recursiva los usuarios de esos contenedores. Si no es necesario manipular los objetos de usuario y solo necesita leer propiedades específicas, use la búsqueda en profundidad que se describe en la opción 2.

    Dado que la enumeración devuelve punteros a objetos COM ADSI que representan cada objeto de usuario, puede llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener punteros de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)y [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) al objeto de usuario. Esto significa que puede obtener punteros de interfaz a cada objeto de usuario enumerado en un contenedor sin tener que enlazar explícitamente a cada objeto de usuario. Para realizar operaciones en todos los usuarios directamente dentro de un contenedor, la enumeración evita tener que enlazar a cada usuario para poder llamar a métodos **IADs** o **IADsUser** . Para recuperar propiedades específicas de los usuarios, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) tal y como se describe en la opción 2.

-   Realice una búsqueda en profundidad (& (objectClass = User) (objectCategory = person)) para buscar todos los usuarios en un árbol:

    En primer lugar, enlace al objeto contenedor en el que va a comenzar la búsqueda. Por ejemplo, para buscar todos los usuarios de un dominio, enlace a la raíz del dominio; para buscar todos los usuarios del bosque, enlace con el catálogo global y busque desde la raíz del GC.

    A continuación, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para consultar mediante un filtro de búsqueda que contenga (& (objectClass = User) (objectCategory = person)) y la preferencia de búsqueda del \_ subárbol del ámbito de ADS \_ .

    Puede realizar una búsqueda con una preferencia de búsqueda del ámbito de ADS \_ \_ onelevel para limitar la búsqueda al contenido directo del objeto contenedor al que se ha enlazado.

    [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) solo recupera los valores de propiedades específicas de los usuarios. Para recuperar valores, use **IDirectorySearch**. Para manipular los objetos de usuario devueltos por una búsqueda, es decir, desea usar métodos [**IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) , debe enlazarlos explícitamente. Para ello, especifique **distinguishedName** como una de las propiedades que se van a devolver de la búsqueda y use los nombres distintivos devueltos para enlazar con cada usuario devuelto en la búsqueda.

    Solo se recuperan las propiedades específicas. No se pueden recuperar todos los atributos sin especificar explícitamente cada atributo posible de la clase de usuario.

 

 