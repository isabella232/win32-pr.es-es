---
title: Enlace al catálogo global
description: El catálogo global es un espacio de nombres que contiene datos de directorio para todos los dominios de un bosque.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Enlace al catálogo global de AD
- catálogo global de AD, enlace a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d094a0c07a40fa063b726d0ba1c5a15977873d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881646"
---
# <a name="binding-to-the-global-catalog"></a>Enlace al catálogo global

El catálogo global es un espacio de nombres que contiene datos de directorio para todos los dominios de un bosque. El catálogo global contiene una réplica parcial de cada directorio de dominio. Contiene una entrada para cada objeto del bosque empresarial, pero no contiene todas las propiedades de cada objeto. En su lugar, solo contiene las propiedades especificadas para su inclusión en el catálogo global.

El catálogo global se almacena en servidores específicos de toda la empresa. Solo los controladores de dominio pueden actuar como servidores de catálogo global. Los administradores indican si un controlador de dominio determinado contiene un catálogo global mediante Active Directory Sites and Services Manager.

Para enlazar al catálogo global con ADSI, use el moniker "GC:".

Hay dos maneras de enlazar al catálogo global para realizar una búsqueda en un bosque:

-   Enlace al objeto raíz de la empresa para buscar en todos los dominios del bosque.
-   Enlace a un objeto específico para buscar ese objeto y sus objetos secundarios. Por ejemplo, si enlaza a un dominio que tiene dos dominios debajo de él en un árbol de dominio del bosque, puede buscar en esos tres dominios. Tenga en cuenta que el nombre distintivo del objeto al que se va a enlazar es exactamente el mismo que el nombre distintivo utilizado para enlazar al espacio de nombres "LDAP:". Recuerde que "LDAP:" es una réplica completa de un solo dominio y que "GC:" es una réplica parcial de todos los dominios del bosque.

Al igual que con el moniker "LDAP:", puede usar el enlace sin servidor o enlazar a un servidor de catálogo global específico. Si busca en el bosque actual, use el enlace sin servidor. Sin embargo, si busca en otro bosque, especifique un nombre de dominio o un servidor de catálogo global al que enlazar, como se muestra en los ejemplos siguientes.

Enlace mediante el nombre de dominio:

``` syntax
GC://fabrikam.com
```

Enlace mediante el nombre del servidor:

``` syntax
GC://servername
```

También puede enlazar a un objeto específico dentro del catálogo global. Para enlazar al objeto sales en el dominio fabrikam, use el formato siguiente.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

O bien, para enlazar al objeto sales en el servidor, use el formato siguiente.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Para buscar en todo el bosque**

1.  Enlace a la raíz del espacio de nombres del catálogo global.
2.  Enumerar el contenedor del catálogo global. El contenedor catálogo global contiene un único objeto que puede usar para buscar en todo el bosque.
3.  Use el objeto del contenedor para realizar la búsqueda. En C/C++, llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) en el objeto para que pueda usar la **interfaz IDirectorySearch** para realizar la búsqueda. En Visual Basic, use el objeto devuelto por la enumeración en la consulta de ADO.

Para enumerar los servidores del catálogo global de un sitio, realice una búsqueda de subárbol LDAP de "cn= &lt; yoursite &gt; ,cn=sites, ", mediante la <DN of the configurationNamingContext> siguiente cadena de filtro.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Este filtro usa el operador de regla de coincidencia **\_ LDAP MATCHING RULE BIT \_ \_ \_ AND** (1.2.840.113556.1.4.803) para buscar **objetos nTDSDSA** que tienen el bit de orden bajo establecido en la máscara de bits del atributo **options.** El bit de orden bajo, que corresponde a la constante **GC NTDSDSA \_ OPT \_ IS \_** definida en Ntdsapi.h, identifica el objeto **nTDSDSA** de un servidor de catálogo global. Para obtener más información sobre las reglas de coincidencia, vea [Sintaxis de filtro de búsqueda.](/windows/desktop/ADSI/search-filter-syntax)

El elemento primario del objeto **nTDSDSA** es el objeto de servidor y la propiedad **dNSHostName** del objeto de servidor es el nombre DNS del servidor de catálogo global.

No puede usar constantes de definición como \# **NTDSDSA \_ OPT \_ IS \_ GC** y **LDAP \_ MATCHING RULE BIT \_ \_ \_ Y** directamente en una cadena de filtro de búsqueda. Sin embargo, puede usar estas constantes como argumentos para una función como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) para insertar los valores constantes en una cadena de filtro.

El catálogo global no representa toda la estructura de árbol de bosque. Por ejemplo, puede esperar que en el ejemplo de código siguiente se enumeren todos los dominios del bosque y todos los objetos secundarios de cada dominio. En realidad, lo que realmente hace es enumerar todos los dominios del bosque, pero ninguno de los objetos de dominio enumerados contiene ningún elemento secundario. Se trata de una limitación del catálogo global.


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



Para corregirlo, es necesario enlazar a cada objeto de dominio y, a continuación, enumerar los objetos secundarios de cada dominio. La técnica adecuada se muestra en el ejemplo de código siguiente.


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



Para obtener más información y ejemplos de código que muestran cómo buscar en todo un bosque, vea [Código de ejemplo para buscar un bosque.](example-code-for-searching-a-forest.md)

 

 
