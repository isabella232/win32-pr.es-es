---
title: LDAP ADsPath
description: En este tema se muestra la sintaxis que debe usar para LDAP ADsPath.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP ADsPath
- ADsPath, LDAP, description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1850c30ff8a5a086fbd697080ac32b5e55549496739d9388a6d5e7ab251403d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839475"
---
# <a name="ldap-adspath"></a>LDAP ADsPath

El proveedor LDAP de Microsoft ADsPath requiere el formato siguiente.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Los caracteres de corchete izquierdo y derecho ( ) indican \[ \] parámetros opcionales; no es una parte literal de la cadena de enlace.

 

"HostName" puede ser un nombre de equipo, una dirección IP o un nombre de dominio. También se puede especificar un nombre de servidor en la cadena de enlace. La mayoría de los proveedores LDAP siguen un modelo que requiere que se especifique un nombre de servidor.

"PortNumber" especifica el puerto que se va a usar para la conexión. Si no se especifica ningún número de puerto, el proveedor LDAP usa el número de puerto predeterminado. El número de puerto predeterminado es 389 si no se usa una conexión SSL o 636 si se usa una conexión SSL.

"DistinguishedName" especifica el nombre distintivo de un objeto específico. Se garantiza que un nombre distintivo para un objeto determinado sea único.

En la tabla siguiente se muestran ejemplos de cadenas de enlace.



| Ejemplo de LDAP ADsPath                                      | Descripción                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| Ldap:                                                     | Enlace a la raíz del espacio de nombres LDAP.                    |
| LDAP://server01                                           | Enlazar a un servidor específico.                                 |
| LDAP://server01:390                                       | Enlace a un servidor específico mediante el número de puerto especificado. |
| LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com          | Enlazar a un objeto específico.                                 |
| LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com | Enlazar a un objeto específico a través de un servidor específico.       |



 

Si se requiere la autenticación Kerberos para la finalización correcta de una solicitud de directorio específica, la cadena de enlace debe usar un ADsPath sin servidor, como LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com, o bien debe usar un ADsPath con un nombre de servidor DNS completo, como LDAP://server01.fabrikam.com/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com. No se garantiza que el enlace al servidor mediante un nombre NETBIOS plano o un nombre DNS corto, por ejemplo, mediante el nombre server01 en lugar de server01.fabrikam.com, produce la autenticación Kerberos.

Para obtener más información y ejemplos de cadenas de enlace LDAP, así como una descripción de los caracteres especiales que se pueden usar en cadenas de enlace LDAP, vea LDAP ADsPath.

**Windows 2000 con SP1 y versiones posteriores:** Con el proveedor LDAP, si una cadena de enlace incluye un nombre de servidor, puede aumentar el rendimiento mediante la marca **\_ ADS SERVER \_ BIND** con la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) La **marca ADS SERVER \_ \_ BIND** indica que se especificó un nombre de servidor, lo que permite a ADSI evitar tráfico de red adicional e innecesario.

## <a name="ldap-special-characters"></a>Caracteres especiales LDAP

LDAP tiene varios caracteres especiales que están reservados para su uso por parte de la API LDAP. La lista de caracteres especiales se puede encontrar en [Nombres distintivos](/previous-versions/windows/desktop/ldap/distinguished-names). Para usar uno de estos caracteres en un ADsPath sin generar un error, el carácter debe ir precedido de una barra diagonal inversa ( \\ ). Esto se conoce como *escape* del carácter. Por ejemplo, si se da un nombre de usuario en forma de " , ", la coma del valor <last name> de nombre debe ser de <first name> escape. La cadena resultante tendría el siguiente aspecto:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



El carácter de escape también se puede especificar mediante su código de caracteres hexadecimales de dos dígitos. Esto se muestra en el ejemplo siguiente.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Los caracteres no imprimibles, como el avance de línea y el retorno de carro, deben ser caracteres de escape y especificarse mediante su código de caracteres hexadecimales de dos dígitos. Esto se muestra en el ejemplo siguiente.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Para obtener más información

Para obtener más información sobre la notación de nombre distintivo utilizada por los servicios de directorio compatibles con LDAP, vea [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 