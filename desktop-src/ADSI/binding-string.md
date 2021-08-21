---
title: Cadena de enlace
description: Debido al número de objetos accesibles desde un servicio de directorio, pueden producirse conflictos de nomenclatura.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI de cadena de enlace
- ADsPath ADSI , Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8e1bc59011c1279b340348572fa0681a0d301319f75603b73714df4c9cb96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023693"
---
# <a name="binding-string"></a>Cadena de enlace

Debido al número de objetos accesibles desde un servicio de directorio, pueden producirse conflictos de nomenclatura. La cadena de enlace, a la que normalmente se hace referencia como ADsPath, permite especificar un objeto determinado sin provocar una colisión de nomenclatura. Esto se puede aplicar a un único proveedor de servicios de directorio o a varios proveedores de servicios de directorio.

ADsPath es una cadena que identifica de forma única un objeto ADSI en un servicio de directorio. Dado que los objetos ADSI existen en el contexto del espacio de nombres del servicio de directorio subyacente, parte de la sintaxis de un nombre ADsPath es específica del proveedor.

En la tabla siguiente se enumeran los proveedores adsi proporcionados de forma predeterminada.



| Proveedor         | Descripción                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winnt<br/> | Se usa para comunicarse con Windows controladores de dominio. Para obtener más información sobre WinNT ADsPath, vea [WinNT ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Se usa para comunicarse con servidores LDAP, como Active Directory. Para obtener más información sobre LDAP ADsPath, vea [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Anuncios<br/>   | Proporciona una [**implementación de IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) que se puede usar para enumerar todos los proveedores adsi instalados en el cliente.<br/> |



 

Use estos nombres de proveedor para acceder al espacio de nombres de proveedor predeterminado. Por ejemplo, si enlaza a LDAP, ADSI se enlaza a un contenedor que contiene el objeto de dominio que ha iniciado sesión actualmente. Si enlaza a WinNT, ADSI se enlaza a un contenedor que contiene objetos que se correlacionan con todos los dominios de la red.

Los elementos iniciales de la cadena ADsPath son el identificador de programación (progID) del proveedor adsi, seguido de "://", seguido de la sintaxis dictada por el espacio de nombres del proveedor. La cadena progID puede o no distingue mayúsculas de minúsculas, según el proveedor. Las cadenas progID de los proveedores enumerados anteriormente distinguen mayúsculas de minúsculas.

La cadena de ruta de acceso puede o no distingue mayúsculas de minúsculas, según el proveedor. Las cadenas de ruta de acceso para los proveedores enumerados anteriormente no distinguen mayúsculas de minúsculas.

A continuación se muestran ejemplos de ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Para buscar todos los proveedores instalados en el equipo, enlace al proveedor de ADs como se muestra en el ejemplo de código siguiente.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Con el proveedor LDAP, puede especificar ADsPath en un formulario de nombre distintivo (DN) X.500, empezando por la etiqueta CN, o bien puede especificar su inverso jerárquico, empezando por la etiqueta O. El formulario que se usa en el ADsPath inicial determina el orden de las etiquetas.

En la tabla siguiente se enumeran los caracteres especiales de ADsPath.



| Nombre                      | Carácter           | Descripción                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Comilla doble<br/>   | "<br/>        | Se usa para citar cualquier parte de ADsPath que pueda contener un carácter especial para que la cadena se interprete literalmente. Por ejemplo, "CN=Nombre/Prefijo".<br/>                                     |
| Barra diagonal inversa<br/>      | \\<br/>       | Se usa para preceder a caracteres especiales para indicar que se deben usar como literales. Para obtener más información y una lista de caracteres especiales, vea [Nombres distintivos.](/previous-versions/windows/desktop/ldap/distinguished-names)<br/> |
| Slash<br/>          | /<br/>        | Separador de componentes.<br/>                                                                                                                                                                       |
| Corchetes angulares<br/> | <><br/> | Delimitar un ADsPath dentro de otra convención de nomenclatura.<br/>                                                                                                                                       |



 

Para delimitar un ADsPath en una especificación de búsqueda o como parte de una dirección URL, use el corchete angular izquierdo y derecho (< >). Por ejemplo, " &lt; WinNT://MyDomain/UserAccount &gt; ".

Algunos proveedores adsi pueden haber agregado restricciones de sintaxis debido a los requisitos de espacio de nombres.

## <a name="active-directory-binding-options"></a>Active Directory enlace de datos

Active Directory proporciona la capacidad de enlazar a un objeto mediante otros tipos de cadenas de enlace, como un identificador único global (GUID) COM o un identificador de seguridad (SID). Para obtener más información, vea [Enlace a Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

