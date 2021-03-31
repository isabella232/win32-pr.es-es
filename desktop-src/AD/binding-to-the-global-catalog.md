---
title: Enlazar con el catálogo global
description: El catálogo global es un espacio de nombres que contiene los datos de directorio de todos los dominios de un bosque.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Enlazar al anuncio de catálogo global
- Catálogo global (AD), enlazar a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077563"
---
# <a name="binding-to-the-global-catalog"></a>Enlazar con el catálogo global

El catálogo global es un espacio de nombres que contiene los datos de directorio de todos los dominios de un bosque. El catálogo global contiene una réplica parcial de cada directorio de dominio. Contiene una entrada para cada objeto del bosque de empresa, pero no contiene todas las propiedades de cada objeto. En su lugar, solo contiene las propiedades especificadas para su inclusión en el catálogo global.

El catálogo global se almacena en servidores específicos de toda la empresa. Solo los controladores de dominio pueden servir como servidores de catálogo global. Los administradores indican si un controlador de dominio determinado contiene un catálogo global mediante el Active Directory el administrador de sitios y servicios.

Para enlazar con el catálogo global con ADSI, use el moniker "GC:".

Hay dos maneras de enlazar con el catálogo global para realizar una búsqueda en un bosque:

-   Enlazar con el objeto raíz de la empresa para buscar en todos los dominios del bosque.
-   Enlazar a un objeto específico para buscar ese objeto y sus elementos secundarios. Por ejemplo, si se enlaza a un dominio que tiene dos dominios debajo en un árbol de dominios del bosque, puede buscar en estos tres dominios. Tenga en cuenta que el nombre distintivo del objeto al que se va a enlazar es exactamente el mismo que el nombre distintivo que se usa para enlazar con el espacio de nombres "LDAP:". Recuerde que "LDAP:" es una réplica completa de un solo dominio y que "GC:" es una réplica parcial de todos los dominios del bosque.

Al igual que con el moniker "LDAP:", puede utilizar el enlace sin servidor o enlazar a un servidor de catálogo global específico. Si busca en el bosque actual, use el enlace sin servidor. Sin embargo, si realiza búsquedas en otro bosque, especifique un nombre de dominio o un servidor de catálogo global con el que enlazar, como se muestra en los ejemplos siguientes.

Enlazar con el nombre de dominio:

``` syntax
GC://fabrikam.com
```

Enlazar con el nombre del servidor:

``` syntax
GC://servername
```

También puede enlazar a un objeto específico en el catálogo global. Para enlazar con el objeto sales del dominio Fabrikam, use el formato siguiente.

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

O bien, para enlazar al objeto sales del servidor, use el formato siguiente.

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**Para buscar en todo el bosque**

1.  Enlazar a la raíz del espacio de nombres del catálogo global.
2.  Enumerar el contenedor de catálogo global. El contenedor de catálogos globales contiene un solo objeto que puede usar para buscar en todo el bosque.
3.  Use el objeto en el contenedor para realizar la búsqueda. En C/C++, llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) en el objeto, de modo que pueda usar la interfaz **IDirectorySearch** para realizar la búsqueda. En Visual Basic, utilice el objeto devuelto de la enumeración en la consulta de ADO.

Para enumerar los servidores de catálogo global de un sitio, realice una búsqueda de subárbol LDAP de "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> ", usando la siguiente cadena de filtro.

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

Este filtro usa el **bit de la \_ regla de coincidencia LDAP \_ \_ \_ y** el operador de regla de coincidencia (1.2.840.113556.1.4.803) para buscar objetos **nTDSDSA** que tengan el bit de orden inferior establecido en la máscara de bits del atributo **Options** . El bit de orden inferior, que corresponde a la constante de **\_ \_ \_ GC nTDSDSA is** Defined en ntdsapi. h, identifica el objeto **nTDSDSA** de un servidor de catálogo global. Para obtener más información sobre las reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).

El elemento primario del objeto **nTDSDSA** es el objeto Server y la propiedad **DnsHostName** del objeto Server es el nombre DNS del servidor de catálogo global.

No puede usar las \# constantes de definición como **nTDSDSA \_ OPC \_ es \_** el bit de la regla de coincidencia de GC y **LDAP, \_ \_ \_ \_ y** directamente en una cadena de filtro de búsqueda. Sin embargo, puede usar estas constantes como argumentos para una función como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) para insertar los valores constantes en una cadena de filtro.

El catálogo global no representa la estructura de árbol de todo el bosque. Por ejemplo, podría esperar que el ejemplo de código siguiente enumerara todos los dominios del bosque y todos los objetos secundarios de cada dominio. En realidad, lo que realmente hace es enumerar todos los dominios del bosque, pero ninguno de los objetos de dominio enumerados contiene elementos secundarios. Se trata de una limitación del catálogo global.


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



Para corregir esto, es necesario enlazar con cada objeto de dominio y, a continuación, enumerar los objetos secundarios de cada dominio. En el ejemplo de código siguiente se muestra la técnica adecuada.


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



Para obtener más información y ejemplos de código que muestren cómo buscar en todo el bosque, vea el [código de ejemplo para buscar en un bosque](example-code-for-searching-a-forest.md).

 

 