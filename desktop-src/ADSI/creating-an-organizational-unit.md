---
title: Crear una unidad organizativa
description: Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creación de una unidad organizativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993863"
---
# <a name="creating-an-organizational-unit"></a>Crear una unidad organizativa

Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas. Fabrikam tiene dos divisiones: sales y Production. La compañía planea contratar dos administradores de Windows 2000 para administrar cada división. Joe Worden, como administrador de la empresa, creará dos nuevas unidades organizativas en el dominio de fabrikam. Al crear una unidad organizativa, Joe puede agrupar varios objetos y permitir que otra persona administre estos objetos. En el ejemplo de código siguiente se crea la unidad organizativa (OU) de ventas.


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



El método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) acepta el nombre de clase y el nombre del nuevo objeto. En este momento, el objeto no se confirma en Active Directory. Sin embargo, tendrá una referencia de objeto ADSI/COM en el cliente. Con este objeto ADSI, puede establecer o modificar atributos mediante el método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) . El método **IADs. put** acepta el nombre del atributo y el valor del atributo. Sin embargo, no se confirma nada en el directorio. todo está almacenado en la memoria caché del cliente. Cuando se llama al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , los cambios, en este caso, la creación de objetos y la modificación de atributos, se confirman en el directorio. Estos cambios se transfieren, lo que significa que verá el nuevo objeto con todos los atributos que establezca, o bien ningún objeto.

También puede anidar unidades organizativas. En el ejemplo de código siguiente se da por supuesto que la división sales está dividida en las regiones este y oeste.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Esto también se aplica a la región oeste.

Para enlazar directamente con la región East de la organización sales, especifique el nombre distintivo.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Si ya ha enlazado al objeto primario (sales), puede enlazar con el objeto secundario (East) del objeto primario mediante el nombre relativo del objeto secundario.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Para asegurarse de que los objetos se han creado, use el complemento de MMC Active Directory usuarios y equipos para ver las nuevas unidades organizativas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Traslado de usuarios existentes a la unidad organizativa](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




