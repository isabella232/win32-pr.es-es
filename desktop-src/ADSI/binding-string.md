---
title: Cadena de enlace
description: Debido al número de objetos a los que se puede tener acceso desde un servicio de directorio, pueden producirse conflictos de nomenclatura.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI de cadena de enlace
- ADsPath ADSI, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995620"
---
# <a name="binding-string"></a>Cadena de enlace

Debido al número de objetos a los que se puede tener acceso desde un servicio de directorio, pueden producirse conflictos de nomenclatura. La cadena de enlace, que se conoce comúnmente como ADsPath, le permite especificar un objeto determinado sin producir una colisión de nombres. Esto se puede aplicar a un único proveedor de servicios de directorio o a través de varios proveedores de servicios de directorio.

ADsPath es una cadena que identifica de forma única un objeto ADSI en un servicio de directorio. Dado que los objetos ADSI existen en el contexto del espacio de nombres del servicio de directorio subyacente, parte de la sintaxis de un nombre ADsPath es específica del proveedor.

En la tabla siguiente se enumeran los proveedores ADSI proporcionados de forma predeterminada.



| Proveedor         | Descripción                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | Se usa para comunicarse con los controladores de dominio de Windows. Para obtener más información sobre el ADsPath de WinNT, consulte [WinNT ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Se utiliza para comunicarse con servidores LDAP, como Active Directory. Para obtener más información acerca de la ADsPath de LDAP, consulte [ADsPath de LDAP](ldap-adspath.md).<br/>  |
| Anuncios<br/>   | Proporciona una implementación de [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que se puede utilizar para enumerar todos los proveedores ADSI instalados en el cliente.<br/> |



 

Use estos nombres de proveedor para tener acceso al espacio de nombres del proveedor predeterminado. Por ejemplo, si se enlaza a LDAP, ADSI se enlaza a un contenedor que contiene el objeto de dominio que ha iniciado sesión actualmente. Si se enlaza a WinNT, ADSI enlaza a un contenedor que contiene objetos que se correlacionan con todos los dominios de la red.

Los elementos iniciales de la cadena ADsPath son el identificador de programación (progID) del proveedor ADSI, seguido de "://", seguido de la sintaxis dictada por el espacio de nombres del proveedor. La cadena progID puede o no distinguir mayúsculas de minúsculas, dependiendo del proveedor. Las cadenas progID para los proveedores enumerados anteriormente distinguen mayúsculas de minúsculas.

La cadena de ruta de acceso puede distinguir entre mayúsculas y minúsculas, en función del proveedor. Las cadenas de ruta de acceso de los proveedores enumerados anteriormente no distinguen mayúsculas de minúsculas.

A continuación se muestran ejemplos de ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Para buscar todos los proveedores instalados en el equipo, enlace al proveedor de ADs tal y como se muestra en el ejemplo de código siguiente.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Con el proveedor LDAP, puede especificar el ADsPath en un formulario de nombre distintivo X. 500 (DN), empezando por la etiqueta CN, o puede especificar su inversa jerárquica, empezando por la etiqueta O. El formato que se usa en el ADsPath inicial determina el orden de las etiquetas.

En la tabla siguiente se enumeran los caracteres especiales de ADsPath.



| Nombre                      | Carácter           | Descripción                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comilla doble<br/>   | "<br/>        | Se usa para citar cualquier parte del ADsPath que pueda contener un carácter especial para que la cadena se interprete literalmente. Por ejemplo, "CN = nombre/prefijo".<br/>                                     |
| Barra diagonal inversa<br/>      | \\<br/>       | Se usa para anteponer caracteres especiales para indicar que deben usarse como literales. Para obtener más información y una lista de caracteres especiales, consulte [nombres distintivos](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| Slash<br/>          | /<br/>        | Separador de componentes.<br/>                                                                                                                                                                       |
| Corchetes angulares<br/> | <><br/> | Delimite un ADsPath dentro de otra Convención de nomenclatura.<br/>                                                                                                                                       |



 

Para delimitar una ADsPath en una especificación de búsqueda o como parte de una dirección URL, use el corchete angular de apertura y derecha (< >). Por ejemplo, " &lt; WinNT://mydomain/UserAccount &gt; ".

Algunos proveedores ADSI pueden haber agregado restricciones de sintaxis debido a los requisitos de espacio de nombres.

## <a name="active-directory-binding-options"></a>Opciones de enlace de Active Directory

Active Directory proporciona la capacidad de enlazar a un objeto utilizando varios otros tipos de cadenas de enlace, como un identificador único global (GUID) COM o un identificador de seguridad (SID). Para obtener más información, vea [enlazar a Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

