---
title: Sintaxis de atributos ADSI
description: Cada atributo del directorio tiene una sintaxis asociada. Por ejemplo, entero, cadena, numérico, y así sucesivamente. ADSI define su propia sintaxis que se asigna a la sintaxis de directorio nativo. En esta sección se describen los tipos de sintaxis de atributo en ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- atributos ADSI , sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 310a678c48051909e4a3e7555b9d8ff0a508c339cfcd41ed6c66286529cadde1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023933"
---
# <a name="adsi-attribute-syntax"></a>Sintaxis de atributos ADSI

Cada atributo del directorio tiene una sintaxis asociada. Por ejemplo, entero, cadena, numérico, y así sucesivamente. ADSI define su propia sintaxis que se asigna a la sintaxis de directorio nativo. En esta sección se describen los tipos de sintaxis de atributo en ADSI.

## <a name="distinguished-name-string"></a>Cadena de nombre distintivo


```VB
Syntax Type: ADSTYPE_DN_STRING
```



El nombre distintivo es útil para vincular dos objetos. Por ejemplo, puede crear un vínculo que convierte al objeto Alice en administrador del objeto Bob. Si el objeto Alice se mueve a otro lugar, el vínculo de administrador entre Alice y Bob se actualiza automáticamente.

El nombre distintivo debe contener un objeto de nombre distintivo válido. Si el nombre distintivo no se corresponde con un objeto existente válido, la mayoría de los servidores rechazan la solicitud y devuelven un error de infracción de restricción.

Ejemplos:


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a>Cadena exacta de mayúsculas y minúsculas y cadena de omiso de mayúsculas y minúsculas


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



Cadena exacta de mayúsculas y minúsculas es una cadena que distingue mayúsculas de minúsculas, mientras que La cadena de ignore mayúsculas y minúsculas es una cadena que no distingue mayúsculas de minúsculas. Un gran porcentaje de atributos del directorio usan esta sintaxis.

> [!Note]  
> El directorio puede almacenarlo o no como una cadena Unicode. Sin embargo, ADSI acepta y devuelve cadenas Unicode.

 

Ejemplo:


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a>Cadena imprimible


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



Esta sintaxis se usa para los atributos con valores de cadena donde las mayúsculas y minúsculas se consideran desiguales para las comparaciones, por ejemplo, "FABRIKAM" y "Fabrikam" no coinciden. ADSI acepta cualquier contenido para una cadena imprimible; no intenta comprobar que son realmente imprimibles.

## <a name="numeric-string"></a>Cadena numérica


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



En esta sintaxis, las cadenas coinciden como en Cadena imprimible, salvo que todos los caracteres de espacio se omiten en las comparaciones. ADSI no realiza la comprobación de valores para asegurarse de que solo aparezcan números y espacios en los valores de esta sintaxis. Active Directory acepta cualquier contenido para una cadena numérica; no comprueba que los caracteres sean numéricos.

## <a name="utc-time"></a>Hora UTC


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Esta sintaxis almacena la fecha y hora en una sola cadena. El formato de cadena consta de tres partes concatenadas: (1) YYMMDD; (2) HHMM o HHMMSS (ambos son aceptables); y (3) "Z" para indicar que la hora dada es Hora media de Greenwich (GMT) o "+/-HHMM" para indicar que la hora dada es la hora local con el diferencial determinado de GMT. El diferencial se basa en la fórmula: GMT=Local+differential.

> [!Note]  
> Los dos primeros dígitos del año no se almacenan en esta cadena.

 

Algunos ejemplos de valores legales son "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130". Esta cadena se almacena como caracteres ASCII de un solo byte y no se almacena ningún número de página de códigos con ella.

Aunque se admite la ordenación, solo se realiza como una ordenación de cadenas que no tiene en cuenta las mayúsculas y minúsculas ASCII, no interpretando correctamente el significado de las cadenas.

Se acepta cualquier valor de cadena válido. No se realiza ningún intento para asegurarse de que la cadena contiene una cadena de hora válida.

## <a name="generalized-time"></a>Tiempo generalizado


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



Si se define un nuevo atributo para almacenar valores de tiempo, se debe usar la sintaxis GeneralizedTime. La sintaxis GeneralizedTime usa cuatro caracteres para representar el año en lugar de dos como con UTCTime.

El formato de la sintaxis GeneralizedTime es "AAAAMMDDHHMMSS.0Z". Un ejemplo de un valor aceptable es "20010928060000.0Z". La "Z" indica que no hay diferencial de tiempo. Active Directory almacena la fecha y hora como Hora media de Greenwich (GMT). Si no se especifica ningún diferencial de hora, GMT es el valor predeterminado.

Si la hora se especifica en una zona horaria que no sea GMT, el diferencial entre la zona horaria y GMT se anexa a la cadena en lugar de "Z" con el formato "AAAAMMDDHHMMSS.0 \[ +/- \] HHMM". Un ejemplo de un valor aceptable es "20010928060000.0+0200".

El diferencial se basa en la fórmula: GMT=Local+differential.

## <a name="boolean"></a>Boolean


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



Active Directory acepta solo un valor de 32 bits firmado para esta sintaxis. Controla cero como **FALSE y** todos los valores distintos de cero como **TRUE.**

## <a name="integer"></a>Entero


```VB
Syntax Type: ADSTYPE_INTEGER
```



Valor numérico de 32 bits con firma.

## <a name="large-integer"></a>Entero grande


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



Valor numérico de 64 bits con firma. Los enteros grandes se implementan realmente como objetos COM en [**la interfaz IADsLargeInteger.**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) Los **métodos HighPart** y **LowPart** se usan para tener acceso a las dos mitades de 32 bits del valor entero grande.

Ejemplo:


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a>Cadena de octeto


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



Una cadena de octeto se devuelve como una matriz variante de bytes. Consta de un recuento de tamaño (número de octetos) seguido de una serie de octetos. Un octeto es un byte de 8 bits, por lo que una serie de octetos es una cadena de datos binarios.

## <a name="object-class"></a>Clase de objeto


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



Clase de objeto es un identificador de objeto único para una clase de esquema determinada. El atributo **objectClass** identifica la clase de cada instancia de objeto. Cuando se crea, nunca se puede cambiar una clase de objeto. **objectClass** es un atributo con varios valores. Enumera la clase específica del objeto y las clases de todas las clases estructurales o abstractas de las que se derivó la clase específica. Esto incluye Top, la clase de la que se derivan en última instancia todas las demás clases. Active Directory enumera las clases auxiliares en el **atributo objectClass.**

## <a name="security-descriptor"></a>Descriptor de seguridad


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



Los derechos de acceso definen las capacidades que tiene una entidad de seguridad cuando intenta realizar una operación en un objeto Active Directory seguridad. Un descriptor de seguridad describe la información de control de acceso asociada a un objeto .

El descriptor de seguridad se almacena como una propiedad de un objeto de directorio en la **propiedad nTSecurityDescriptor.** Cuando un usuario autenticado intenta acceder a un objeto de directorio, el servidor de directorio determina el acceso concedido o denegado al usuario en función del descriptor de seguridad del objeto.

La [**\_ enumeración ADS SD \_ CONTROL \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) especifica marcas de control para un descriptor de seguridad.

En el ejemplo de código siguiente se muestra cómo obtener un descriptor de seguridad.


```VB
' Obtain a security descriptor.
Dim x as IADs
Dim sd as IADsSecurityDescriptor
Dim acl as IADsAccessControlList
 
Set x = GetObject("LDAP://DC=Fabrikam, DC=com")
Set sd = x.Get("nTSecurityDescriptor")
 
Debug.Print sd.Control
Debug.Print sd.Group
Debug.Print sd.Owner
Debug.Print sd.Revision
 
Set acl = sd.DiscretionaryAcl
Set sacl = sd.SystemAcl
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sintaxis para Active Directory atributos](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[Elección de una sintaxis](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[Cómo especificar valores de comparación](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 