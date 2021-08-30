---
title: Cómo especificar valores de comparación
description: Cada tipo de atributo tiene una sintaxis que determina el tipo de valores de comparación que puede especificar en un filtro de búsqueda para ese atributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Cómo especificar valores de comparación de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b847f681be876ff768a51a9f5da875cb653faa51
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881384"
---
# <a name="how-to-specify-comparison-values"></a>Cómo especificar valores de comparación

Cada tipo de atributo tiene una sintaxis que determina el tipo de valores de comparación que puede especificar en un filtro de búsqueda para ese atributo.

En las secciones siguientes se describen los requisitos de cada sintaxis de atributo. Para obtener más información sobre las sintaxis de atributos, vea [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

<dl> <dt>

<span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Booleana
</dt> <dd>

El valor especificado en un filtro debe ser un valor de cadena que sea "TRUE" o "FALSE". En los ejemplos siguientes se muestra cómo especificar una cadena de comparación booleana.

En el ejemplo siguiente se buscarán objetos que tengan **un valor showInAdvancedViewOnly** establecido en **TRUE:**


```C++
(showInAdvancedViewOnly=TRUE)
```



En el ejemplo siguiente se buscarán objetos que tengan **un valor showInAdvancedViewOnly** establecido en **FALSE**:


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Entero y enumeración
</dt> <dd>

El valor especificado en un filtro debe ser un entero decimal. Los valores hexadecimales deben convertirse en decimales. Una cadena de comparación de valores tiene la forma siguiente:


```C++
<attribute name>:<value>
```



" <attribute name> " es el **lDAPDisplayName** del atributo y " &lt; value " es el valor que se usará para la &gt; comparación.

En el ejemplo de código siguiente se muestra un filtro que buscará objetos que tengan un valor **groupType** igual a la marca **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** (8) y la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000). Las dos marcas combinadas son iguales 0x80000008, que se convierten en decimales 2147483656.


```C++
(groupType=2147483656)
```



Los operadores de reglas de coincidencia LDAP también se pueden usar para realizar comparaciones bit a bit. Para obtener más información sobre las reglas de coincidencia, vea [Sintaxis de filtro de búsqueda.](/windows/desktop/ADSI/search-filter-syntax) En el ejemplo de código siguiente se muestra un filtro que buscará objetos que tienen **un groupType** con el conjunto de bits **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648).


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString
</dt> <dd>

El valor especificado en un filtro son los datos que se encuentran. Los datos deben representarse como una cadena de bytes codificada con dos caracteres, donde cada byte va precedido de una barra diagonal inversa ( \\ ). Por ejemplo, el valor 0x05 aparecerá en la cadena como \\ "05".

La [**función ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) se puede usar para crear una representación de cadena codificada de datos binarios. La **función ADsEncodeBinaryData** no codifica valores de bytes que representan caracteres alfanuméricos. En su lugar, colocará el carácter en la cadena sin codificar. Como resultado, la cadena contiene una mezcla de caracteres codificados y sin codificar. Por ejemplo, si los datos binarios se 0x05 0x1A 0x1B 0x43 0x32, la cadena codificada contendrá \| \| \| \| \\ "05 \\ 1A \\ 1BC2". Esto no tiene ningún efecto en el filtro y los filtros de búsqueda funcionarán correctamente con estos tipos de cadenas.

Se aceptan caracteres comodín.

En el ejemplo de código siguiente se muestra un filtro que contiene una cadena codificada para **schemaIDGUID** con el valor GUID "{BF967ABA-0DE6-11D0-A285-00AAA003049E2}":


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid
</dt> <dd>

El valor especificado en un filtro es la representación de cadena de bytes codificada del SID. Para obtener más información sobre las cadenas de bytes codificadas, vea la sección anterior de este tema en la que se describe la sintaxis de OctetString.

En el ejemplo de código siguiente se muestra un filtro que contiene una cadena codificada para **objectSid** con el valor de cadena SID de "S-1-5-21-1935655697-308236825-1417001333":


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span id="DN"></span><span id="dn"></span>DN
</dt> <dd>

Se debe proporcionar el nombre distintivo completo que se va a coincidir.

No se aceptan caracteres comodín.

Tenga en cuenta que **el atributo objectCategory** también permite especificar **el lDAPDisplayName** de la clase establecida en el atributo .

En el ejemplo siguiente se muestra un filtro que especifica un **miembro** que contiene "CN=TestUser,DC=Fabrikam,DC=COM":


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span id="INTEGER8"></span><span id="integer8"></span>INTEGER8
</dt> <dd>

El valor especificado en un filtro debe ser un entero decimal. Convertir valores hexadecimales en decimales.

En el ejemplo de código siguiente se muestra un filtro que especifica un **valor creationTime** establecido en [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de "1999-12-31 23:59:59 (UTC/GMT)":


```C++
(creationTime=125911583990000000)
```



Las siguientes funciones crean un filtro de coincidencia exacta (=) para un atributo entero grande y comprueban el atributo en el esquema y su sintaxis:


```C++
//***************************************************************************
//
//  CheckAttribute()
//
//***************************************************************************

HRESULT CheckAttribute(LPOLESTR szAttribute, LPOLESTR szSyntax)
{
    HRESULT hr = E_FAIL;
    BSTR bstr;
    IADsProperty *pObject = NULL;
    LPWSTR szPrefix = L"LDAP://schema/";
    LPWSTR szPath;
     
    if((!szAttribute) || (!szSyntax))
    {
        return E_POINTER;
    }

    // Allocate a buffer large enough to hold the ADsPath of the attribute.
    szPath = new WCHAR[lstrlenW(szPrefix) + lstrlenW(szAttribute) + 1];
    if(NULL == szPath)
    {
        return E_OUTOFMEMORY;
    }
     
    // Create the ADsPath of the attribute.
    wcscpy_s(szPath, szPrefix);
    wcscat_s(szPath, szAttribute);

    hr = ADsOpenObject( szPath,
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                        IID_IADsProperty,
                        (void**)&pObject);
    if(SUCCEEDED(hr)) 
    {
        hr = pObject->get_Syntax(&bstr);
        if (SUCCEEDED(hr)) 
        {
            if (0==lstrcmpiW(bstr, szSyntax)) 
            {
                hr = S_OK;
            }
            else
            {
                hr = S_FALSE;
            }
        }

        SysFreeString(bstr);
    }
    
    if(pObject)
    {
        pObject->Release();
    }

    delete szPath;
    
    return hr;
}

//***************************************************************************
//
//  CreateExactMatchFilterLargeInteger()
//
//***************************************************************************

HRESULT CreateExactMatchFilterLargeInteger( LPOLESTR szAttribute, 
                                            INT64 liValue, 
                                            LPOLESTR *pszFilter)
{
    HRESULT hr = E_FAIL;
     
    if ((!szAttribute) || (!pszFilter))
    {
        return E_POINTER;
    }
     
    // Verify that the attribute exists and has 
    // Integer8 (Large Integer) syntax.
     
    hr = CheckAttribute(szAttribute, L"Integer8");
    if (S_OK == hr) 
    {
        LPWSTR szFormat = L"%s=%I64d";
        LPWSTR szTempFilter = new WCHAR[lstrlenW(szFormat) + lstrlenW(szAttribute) + 20 + 1];

        if(NULL == szTempFilter)
        {
            return E_OUTOFMEMORY;
        }
        
        swprintf_s(szTempFilter, L"%s=%I64d", szAttribute, liValue);
     
        // Allocate buffer for the filter string.
        // Caller must free the buffer using CoTaskMemFree.
        *pszFilter = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (lstrlenW(szTempFilter) + 1));
        if (*pszFilter) 
        {
            wcscpy_s(*pszFilter, szTempFilter);
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }

        delete szTempFilter;
    }

    return hr;
}
```



</dd> <dt>

<span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString
</dt> <dd>

Los atributos con estas sintaxis deben cumplir con conjuntos de caracteres específicos. Para obtener más información, vea [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).

Actualmente, Active Directory Domain Services no aplican esos juegos de caracteres.

El valor especificado en un filtro es una cadena. La comparación distingue mayúsculas de minúsculas.

</dd> <dt>

<span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime
</dt> <dd>

El valor especificado en un filtro es una cadena que representa la fecha en el formato siguiente:


```C++
YYYYMMDDHHMMSS.0Z
```



"0Z" indica que no hay diferencial de tiempo. Tenga en cuenta que Active Directory servidor almacena la fecha y hora como Hora media de Greenwich (GMT). Si no se especifica un diferencial de hora, el valor predeterminado es GMT.

Si la zona horaria local no es GMT, use un valor diferencial para especificar la zona horaria local y aplicar el diferencial a GMT. El diferencial se basa en: GMT=Local+differential.

Para especificar un diferencial, use:


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



En el ejemplo siguiente se muestra un filtro que especifica una hora **whenCreated** establecida en 3/23/99 8:52:58 PM GMT:


```C++
(whenCreated=19990323205258.0Z)
```



En el ejemplo siguiente se muestra un filtro que especifica un valor **whenCreated** time establecido en 3/23/99 8:52:58 PM Hora estándar de Nueva Zelanda (el diferencial es +12 horas):


```C++
(whenCreated=19990323205258.0+1200)
```



En el ejemplo de código siguiente se muestra cómo calcular el diferencial de zona horaria. La función devuelve el diferencial entre la zona horaria local actual y GMT. El valor devuelto es una cadena con el formato siguiente:


```C++
[+/-]HHMM
```



Por ejemplo, la hora estándar del Pacífico es -0800.


```C++
//***************************************************************************
//
//  GetLocalTimeZoneDifferential()
//
//***************************************************************************

HRESULT GetLocalTimeZoneDifferential(LPOLESTR *pszDifferential)
{
    if(NULL == pszDifferential)
    {
        return E_INVALIDARG;
    }
    
    HRESULT hr = E_FAIL;
    DWORD dwReturn;
    TIME_ZONE_INFORMATION timezoneinfo;
    LONG lTimeDifferential;
    LONG lHours;
    LONG lMinutes;
    
    dwReturn  = GetTimeZoneInformation(&timezoneinfo);

    switch (dwReturn)
    {
    case TIME_ZONE_ID_STANDARD:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.StandardBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;

        hr = S_OK;
        break;

    case TIME_ZONE_ID_DAYLIGHT:
        lTimeDifferential = timezoneinfo.Bias + timezoneinfo.DaylightBias;
        
        // Bias is in minutes. Calculate the hours for HHMM format.
        // Apply the additive inverse.
        // Bias is based on GMT=Local+Bias.
        // A differential, based on GMT=Local-Bias, is required.
        lHours = -(lTimeDifferential/60);
        
        // Bias is in minutes. Calculate the minutes for HHMM format.
        lMinutes = lTimeDifferential%60L;
        
        hr = S_OK;
        break;

    case TIME_ZONE_ID_INVALID:
    default:
        hr = E_FAIL;
        break;
    }
     
    if (SUCCEEDED(hr))
    {
        // The caller must free the memory using CoTaskMemFree.
        *pszDifferential = (OLECHAR *)CoTaskMemAlloc(sizeof(OLECHAR) * (3 + 2 + 1));
        if (*pszDifferential)
        {
            swprintf_s(*pszDifferential, L"%+03d%02d", lHours, lMinutes);
            
            hr = S_OK;
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
    }
     
    return hr;
}
```



</dd> <dt>

<span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>HORA UTC
</dt> <dd>

El valor especificado en un filtro es una cadena que representa la fecha en el formato siguiente:


```C++
YYMMDDHHMMSSZ
```



Z indica que no hay diferencial de tiempo. Tenga en cuenta que el servidor Active Directory almacena la fecha y la hora como hora GMT. Si no se especifica un diferencial de hora, GMT es el valor predeterminado.

El valor de segundos ("SS") es opcional.

Si GMT no es la zona horaria local, aplique un valor diferencial local para especificar la zona horaria local. El diferencial es: GMT=Local+differential.

Para especificar un diferencial, use el siguiente formulario:


```C++
YYMMDDHHMMSS[+/-]HHMM
```



En el ejemplo siguiente se muestra un filtro que especifica una hora **myTimeAttrib** establecida en 3/23/99 8:52:58 PM GMT:


```C++
(myTimeAttrib=990323205258Z)
```



En el ejemplo siguiente se muestra un filtro que especifica un tiempo **myTimeAttrib** establecido en 3/23/99 8:52:58 PM sin segundos especificados:


```C++
(myTimeAttrib=9903232052Z)
```



En el ejemplo siguiente se muestra un filtro que especifica un tiempo **myTimeAttrib** establecido en 3/23/99 8:52:58 PM Hora estándar de Nueva Zelanda (el diferencial es 12 horas). Esto equivale a 3/23/99 8:52:58 AM GMT.


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString
</dt> <dd>

El valor especificado en un filtro es una cadena. DirectoryString puede contener caracteres Unicode. La comparación distingue entre mayúsculas y minúsculas.

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Se debe proporcionar todo el OID que se va a coincidir.

No se aceptan caracteres comodín.

El **atributo objectCategory** permite especificar el **lDAPDisplayName** del conjunto de clases para el atributo.

En el ejemplo siguiente se muestra un filtro que especifica **governsID para** la clase de volumen:


```C++
(governsID=1.2.840.113556.1.5.36)
```



Dos filtros equivalentes que especifican el atributo **systemMustContain** que contiene **uNCName**, que tiene un OID de 1.2.840.113556.1.4.137:


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Otras sintaxis
</dt> <dd>

Las sintaxis siguientes se evalúan en un filtro similar a una cadena de octeto:

-   ObjectSecurityDescriptor
-   AccessPointDN
-   PresentationAddresses
-   ReplicaLink
-   DNWithString
-   DNWithOctetString
-   ORName

</dd> </dl>

 

 
