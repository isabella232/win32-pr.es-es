---
title: Enumeración de usuarios
description: A Windows los dominios NT 4.0, Windows 2000 usuarios se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio.
ms.assetid: 4a35af7a-f43b-4cf9-a030-77f6c2518ae7
ms.tgt_platform: multiple
keywords:
- Enumeración de USUARIOS AD
- usuarios de AD , enumerando un usuario
- Active Directory, usar,users, enumerar un usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa43034c6c006c9c70531f25e2a838ecfc30520e9b42e0b9599e5714a29f225e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191345"
---
# <a name="enumerating-users"></a>Enumeración de usuarios

A Windows los dominios NT 4.0, Windows 2000 usuarios se pueden colocar en cualquier contenedor o unidad organizativa (OU) de un dominio, así como en la raíz del dominio. Esto significa que los usuarios pueden estar en numerosas ubicaciones de la jerarquía de directorios. Por lo tanto, tiene dos opciones para enumerar usuarios:

-   Enumerar los usuarios contenidos directamente en un contenedor, una unidad organizativa o en la raíz del dominio:

    Enlace explícitamente al objeto contenedor que contiene los usuarios que le interesa enumerar, establezca un filtro que contenga "user" como clase mediante la propiedad [**IADsContainer.Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) y use el método [**IADsContainer::get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) para enumerar los objetos de usuario.

    Esta técnica se puede usar para enumerar los usuarios que están contenidos directamente en un contenedor u objeto de unidad organizativa. Si el contenedor contiene otros contenedores que pueden contener otros usuarios, debe enlazar a esos contenedores y enumerar de forma recursiva los usuarios de esos contenedores. Si no es necesario manipular los objetos de usuario y solo necesita leer propiedades específicas, use la búsqueda en profundidad descrita en opción 2.

    Dado que la enumeración devuelve punteros a objetos COM ADSI que representan cada objeto de usuario, puede llamar a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener los punteros de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads), [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser)e [**IADsPropertyList**](/windows/desktop/api/iads/nn-iads-iadspropertylist) al objeto de usuario. Esto significa que puede obtener punteros de interfaz a cada objeto de usuario enumerado en un contenedor sin tener que enlazar explícitamente a cada objeto de usuario. Para realizar operaciones en todos los usuarios directamente dentro de un contenedor, la enumeración evita tener que enlazar a cada usuario para llamar a los **métodos IADs** o **IADsUser.** Para recuperar propiedades específicas de los usuarios, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) como se describe en la opción 2.

-   Realice una búsqueda en profundidad (&(objectClass=user)(objectCategory=person)) para buscar todos los usuarios en un árbol:

    En primer lugar, enlace al objeto contenedor donde se va a iniciar la búsqueda. Por ejemplo, para buscar todos los usuarios de un dominio, enlace a la raíz del dominio; para buscar todos los usuarios en el bosque, enlace al catálogo global y busque desde la raíz del GC.

    A continuación, use [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) para realizar consultas mediante un filtro de búsqueda que contenga (&(objectClass=user)(objectCategory=person)) y la preferencia de búsqueda de ADS \_ SCOPE \_ SUBTREE.

    Puede realizar una búsqueda con una preferencia de búsqueda de ADS SCOPE ONELEVEL para limitar la búsqueda al contenido directo del objeto contenedor al que \_ \_ se enlaza.

    [**IDirectorySearch recupera**](/windows/desktop/api/iads/nn-iads-idirectorysearch) solo los valores de propiedades específicas de los usuarios. Para recuperar valores, use **IDirectorySearch**. Para manipular los objetos de usuario devueltos por una búsqueda, es decir, quiere usar los [**métodos IADs**](/windows/desktop/api/iads/nn-iads-iads) o [**IADsUser,**](/windows/desktop/api/iads/nn-iads-iadsuser) debe enlazarlos explícitamente. Para ello, especifique **distinguishedName** como una de las propiedades que se devolverán de la búsqueda y use los nombres distintivos devueltos para enlazar a cada usuario devuelto en la búsqueda.

    Solo se recuperan propiedades específicas. No se pueden recuperar todos los atributos sin especificar explícitamente todos los atributos posibles de la clase de usuario.

 

 