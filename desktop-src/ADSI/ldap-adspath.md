---
title: ADsPath de LDAP
description: En este tema se muestra la sintaxis que se debe usar para la ADsPath de LDAP.
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- ADsPath de LDAP
- ADsPath, LDAP, descripción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1728d2531bb2043f95e5896e67ec054095f2595a
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793881"
---
# <a name="ldap-adspath"></a>ADsPath de LDAP

El atributo ADsPath del proveedor LDAP de Microsoft requiere el formato siguiente.


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> Los caracteres de corchete de apertura y cierre ( \[ \] ) indican parámetros opcionales; no es una parte literal de la cadena de enlace.

 

El "nombre de host" puede ser un nombre de equipo, una dirección IP o un nombre de dominio. También se puede especificar un nombre de servidor en la cadena de enlace. La mayoría de los proveedores LDAP siguen un modelo que requiere que se especifique un nombre de servidor.

El "númeroDePuerto" especifica el puerto que se va a utilizar para la conexión. Si no se especifica ningún número de puerto, el proveedor LDAP utiliza el número de puerto predeterminado. El número de puerto predeterminado es 389 si no se usa una conexión SSL o 636 si se usa una conexión SSL.

"DistinguishedName" especifica el nombre distintivo de un objeto concreto. Se garantiza que un nombre distintivo de un objeto determinado es único.

En la tabla siguiente se muestran ejemplos de cadenas de enlace.



| Ejemplo de ADsPath de LDAP                                      | Descripción                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| LDAP                                                     | Enlazar a la raíz del espacio de nombres LDAP.                    |
| LDAP://server01                                           | Enlazar a un servidor específico.                                 |
| LDAP://server01:390                                       | Enlazar a un servidor específico usando el número de puerto especificado. |
| LDAP:Rio de la siguiente Juan Smith, CN = users, DC = Fabrikam, DC = com          | Enlazar a un objeto específico.                                 |
| LDAP://server01/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com | Enlazar a un objeto específico a través de un servidor específico.       |



 

Si se requiere la autenticación Kerberos para la finalización correcta de una solicitud de directorio específica, la cadena de enlace debe usar una ADsPath sin servidor, como LDAP: encontrada = Jeff Smith, CN = users, DC = Fabrikam, DC = com o debe usar una ADsPath con un nombre de servidor DNS completo, como LDAP://server01.fabrikam.com/CN=Jeff Smith, CN = users, DC = Fabrikam, DC = com. No se garantiza que el enlace al servidor mediante un nombre NETBIOS plano o un nombre DNS corto, por ejemplo, con el nombre Server01 en lugar de server01.fabrikam.com, produzca la autenticación Kerberos.

Para obtener más información y ejemplos de cadenas de enlace LDAP, así como una descripción de los caracteres especiales que se pueden usar en las cadenas de enlace LDAP, vea ADsPath de LDAP.

**Windows 2000 con SP1 y versiones posteriores:** Con el proveedor LDAP, si una cadena de enlace incluye un nombre de servidor, puede aumentar el rendimiento mediante el uso del marcador de **\_ \_ enlace del servidor ADS** con la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . La marca de **\_ \_ enlace del servidor de ADS** indica que se especificó un nombre de servidor, lo que permite que ADSI Evite tráfico de red adicional e innecesario.

## <a name="ldap-special-characters"></a>Caracteres especiales LDAP

LDAP tiene varios caracteres especiales que se reservan para su uso con la API de LDAP. La lista de caracteres especiales puede encontrarse en [nombres distintivos](/previous-versions/windows/desktop/ldap/distinguished-names). Para usar uno de estos caracteres en una ADsPath sin generar un error, el carácter debe ir precedido de un carácter de barra diagonal inversa ( \\ ). Esto se conoce como *escapar* del carácter. Por ejemplo, si se proporciona un nombre de usuario con el formato " <last name> , <first name> ", la coma del valor de nombre debe ser de escape. La cadena resultante tendría el siguiente aspecto:


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



El carácter de escape también se puede especificar mediante el código de carácter hexadecimal de dos dígitos. Esto se muestra en el ejemplo siguiente.


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



Los caracteres no imprimibles, como el avance de línea y el retorno de carro, deben ser de escape y se pueden especificar mediante el código de carácter hexadecimal de dos dígitos. Esto se muestra en el ejemplo siguiente.


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>Para obtener más información

Para obtener más información acerca de la notación de nombre distintivo utilizada por los servicios de directorio compatibles con LDAP, vea [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) .

 

 