---
title: Crear una unidad organizativa
description: Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creación de un ADSI de unidad organizativa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf2db91c02836e2425cd25e72afe6e57ff6619948372a20d03079d65eee5c882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961994"
---
# <a name="creating-an-organizational-unit"></a>Crear una unidad organizativa

Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas. Fabrikam tiene dos divisiones: Ventas y Producción. La empresa planea contratar a dos Windows 2000 administradores para administrar cada división. Joe Worden, como administrador de la empresa, creará dos nuevas unidades organizativas en el dominio fabrikam. Al crear una unidad organizativa, Joe puede agrupar varios objetos y permitir que otra persona administre estos objetos. En el ejemplo de código siguiente se crea la unidad organizativa (OU) Sales.


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



El [**método IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) acepta el nombre de clase y el nombre del nuevo objeto. En este momento, el objeto no se confirma en Active Directory. Sin embargo, tendrá una referencia de objeto ADSI/COM en el cliente. Con este objeto ADSI, puede establecer o modificar atributos mediante el [**método IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put) El **método IADs.Put** acepta el nombre del atributo y el valor del atributo. Aun así, no se confirma nada en el directorio; todo se almacena en caché en el cliente. Cuando se llama al [**método IADs.SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) los cambios, en este caso, la creación de objetos y la modificación de atributos, se confirman en el directorio . Estos cambios se realizan de forma transaccional, lo que significa que verá el nuevo objeto con todos los atributos establecidos o ningún objeto.

También puede anidar unidades organizativas. En el ejemplo de código siguiente se supone que la división Ventas se divide más en las regiones Este y Oeste.


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



Esto también se aplica a la región Oeste.

Para enlazar directamente a la región Este de la organización Ventas, especifique el nombre distintivo.


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



Si ya ha enlazado al objeto primario (Sales), puede enlazar al objeto secundario (Este) desde el objeto primario con el nombre relativo del objeto secundario.


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



Para asegurarse de que se han creado los objetos, use Usuarios y equipos de Active Directory complemento MMC para ver las nuevas unidades organizativas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mover usuarios existentes a la unidad organizativa](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




