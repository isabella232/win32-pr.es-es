---
title: Cómo especificar valores de comparación
description: Cada tipo de atributo tiene una sintaxis que determina el tipo de valores de comparación que puede especificar en un filtro de búsqueda para ese atributo.
ms.assetid: 72bd58e4-e1c3-40a5-9917-4910f40c52c5
ms.tgt_platform: multiple
keywords:
- Cómo especificar valores de comparación de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edba238961cdc18b088b6b5bd5b06ff4be383add
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386755"
---
# <a name="how-to-specify-comparison-values"></a><span data-ttu-id="026f1-104">Cómo especificar valores de comparación</span><span class="sxs-lookup"><span data-stu-id="026f1-104">How to Specify Comparison Values</span></span>

<span data-ttu-id="026f1-105">Cada tipo de atributo tiene una sintaxis que determina el tipo de valores de comparación que puede especificar en un filtro de búsqueda para ese atributo.</span><span class="sxs-lookup"><span data-stu-id="026f1-105">Each attribute type has a syntax that determines the type of comparison values that you can specify in a search filter for that attribute.</span></span>

<span data-ttu-id="026f1-106">En las secciones siguientes se describen los requisitos para cada sintaxis de atributo.</span><span class="sxs-lookup"><span data-stu-id="026f1-106">The following sections describe requirements for each attribute syntax.</span></span> <span data-ttu-id="026f1-107">Para obtener más información sobre las sintaxis de atributo, vea [Sintaxis de atributos en Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="026f1-107">For more information about attribute syntaxes, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<dl> <dt>

<span data-ttu-id="026f1-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Booleana</span><span class="sxs-lookup"><span data-stu-id="026f1-108"><span id="Boolean"></span><span id="boolean"></span><span id="BOOLEAN"></span>Boolean</span></span>
</dt> <dd>

<span data-ttu-id="026f1-109">El valor especificado en un filtro debe ser un valor de cadena que sea "TRUE" o "FALSE".</span><span class="sxs-lookup"><span data-stu-id="026f1-109">The value specified in a filter must be a string value that is either "TRUE" or "FALSE".</span></span> <span data-ttu-id="026f1-110">En los ejemplos siguientes se muestra cómo especificar una cadena de comparación booleana.</span><span class="sxs-lookup"><span data-stu-id="026f1-110">The following examples show how to specify a Boolean comparison string.</span></span>

<span data-ttu-id="026f1-111">En el ejemplo siguiente se buscarán objetos que tengan **un valor showInAdvancedViewOnly** establecido en **TRUE**:</span><span class="sxs-lookup"><span data-stu-id="026f1-111">The following example will search for objects that have a **showInAdvancedViewOnly** set to **TRUE**:</span></span>


```C++
(showInAdvancedViewOnly=TRUE)
```



<span data-ttu-id="026f1-112">En el ejemplo siguiente se buscarán objetos que tengan **un valor showInAdvancedViewOnly** establecido en **FALSE**:</span><span class="sxs-lookup"><span data-stu-id="026f1-112">The following example will search for objects that have a **showInAdvancedViewOnly** set to **FALSE**:</span></span>


```C++
(showInAdvancedViewOnly=FALSE)
```



</dd> <dt>

<span data-ttu-id="026f1-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Entero y enumeración</span><span class="sxs-lookup"><span data-stu-id="026f1-113"><span id="Integer_and_Enumeration"></span><span id="integer_and_enumeration"></span><span id="INTEGER_AND_ENUMERATION"></span>Integer and Enumeration</span></span>
</dt> <dd>

<span data-ttu-id="026f1-114">El valor especificado en un filtro debe ser un entero decimal.</span><span class="sxs-lookup"><span data-stu-id="026f1-114">The value specified in a filter must be a decimal Integer.</span></span> <span data-ttu-id="026f1-115">Los valores hexadecimales deben convertirse en decimales.</span><span class="sxs-lookup"><span data-stu-id="026f1-115">Hexadecimal values must be converted to decimal.</span></span> <span data-ttu-id="026f1-116">Una cadena de comparación de valores tiene la forma siguiente:</span><span class="sxs-lookup"><span data-stu-id="026f1-116">A value comparison string takes the following form:</span></span>


```C++
<attribute name>:<value>
```



<span data-ttu-id="026f1-117">" <attribute name> " es el **lDAPDisplayName** del atributo y "</span><span class="sxs-lookup"><span data-stu-id="026f1-117">"<attribute name>" is the **lDAPDisplayName** of the attribute and "</span></span><value><span data-ttu-id="026f1-118">" es el valor que se va a usar para la comparación.</span><span class="sxs-lookup"><span data-stu-id="026f1-118">" is the value to use for comparison.</span></span>

<span data-ttu-id="026f1-119">En el ejemplo de código siguiente se muestra un filtro que buscará objetos que tengan un valor **groupType** igual a la marca **ADS GROUP TYPE UNIVERSAL \_ \_ \_ \_ GROUP** (8) y la marca **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000).</span><span class="sxs-lookup"><span data-stu-id="026f1-119">The following code example shows a filter that will search for objects that have a **groupType** value that is equal to the **ADS\_GROUP\_TYPE\_UNIVERSAL\_GROUP** (8) flag and the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000) flag.</span></span> <span data-ttu-id="026f1-120">Las dos marcas combinadas son iguales 0x80000008, que se convierten en decimales es 2147483656.</span><span class="sxs-lookup"><span data-stu-id="026f1-120">The two flags combined equal 0x80000008, which converted to decimal is 2147483656.</span></span>


```C++
(groupType=2147483656)
```



<span data-ttu-id="026f1-121">Los operadores de reglas de coincidencia LDAP también se pueden usar para realizar comparaciones bit a bit.</span><span class="sxs-lookup"><span data-stu-id="026f1-121">The LDAP matching rule operators can also be used to perform bitwise comparisons.</span></span> <span data-ttu-id="026f1-122">Para obtener más información sobre las reglas de coincidencia, vea [Sintaxis de filtro de búsqueda.](/windows/desktop/ADSI/search-filter-syntax)</span><span class="sxs-lookup"><span data-stu-id="026f1-122">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span> <span data-ttu-id="026f1-123">En el ejemplo de código siguiente se muestra un filtro que buscará objetos que tienen un **groupType** con el conjunto de bits **ADS GROUP TYPE SECURITY \_ \_ \_ \_ ENABLED** (0x80000000 = 2147483648).</span><span class="sxs-lookup"><span data-stu-id="026f1-123">The following code example shows a filter that will search for objects that have a **groupType** with the **ADS\_GROUP\_TYPE\_SECURITY\_ENABLED** (0x80000000 = 2147483648) bit set.</span></span>


```C++
(groupType:1.2.840.113556.1.4.803:=2147483648))
```



</dd> <dt>

<span data-ttu-id="026f1-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span><span class="sxs-lookup"><span data-stu-id="026f1-124"><span id="OctetString"></span><span id="octetstring"></span><span id="OCTETSTRING"></span>OctetString</span></span>
</dt> <dd>

<span data-ttu-id="026f1-125">El valor especificado en un filtro son los datos que se encuentran.</span><span class="sxs-lookup"><span data-stu-id="026f1-125">The value specified in a filter is the data to be found.</span></span> <span data-ttu-id="026f1-126">Los datos deben representarse como una cadena de bytes codificada en dos caracteres, donde cada byte va precedido de una barra diagonal inversa ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="026f1-126">The data must be represented as a two character encoded byte string where each byte is preceded by a backslash (\\).</span></span> <span data-ttu-id="026f1-127">Por ejemplo, el valor 0x05 aparecerá en la cadena como \\ "05".</span><span class="sxs-lookup"><span data-stu-id="026f1-127">For example, the value 0x05 will appear in the string as "\\05".</span></span>

<span data-ttu-id="026f1-128">La [**función ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) se puede usar para crear una representación de cadena codificada de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="026f1-128">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function can be used to create an encoded string representation of binary data.</span></span> <span data-ttu-id="026f1-129">La **función ADsEncodeBinaryData** no codifica valores de bytes que representan caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="026f1-129">The **ADsEncodeBinaryData** function does not encode byte values that represent alpha-numeric characters.</span></span> <span data-ttu-id="026f1-130">En su lugar, colocará el carácter en la cadena sin codificar.</span><span class="sxs-lookup"><span data-stu-id="026f1-130">It will, instead, place the character into the string without encoding it.</span></span> <span data-ttu-id="026f1-131">Esto da como resultado la cadena que contiene una combinación de caracteres codificados y sin codificar.</span><span class="sxs-lookup"><span data-stu-id="026f1-131">This results in the string containing a mixture of encoded and unencoded characters.</span></span> <span data-ttu-id="026f1-132">Por ejemplo, si los datos binarios se 0x05 0x1A 0x1B 0x43 0x32, la cadena codificada \| \| \| \| contendrá \\ "05 \\ 1A \\ 1BC2".</span><span class="sxs-lookup"><span data-stu-id="026f1-132">For example, if the binary data is 0x05\|0x1A\|0x1B\|0x43\|0x32, the encoded string will contain "\\05\\1A\\1BC2".</span></span> <span data-ttu-id="026f1-133">Esto no tiene ningún efecto en el filtro y los filtros de búsqueda funcionarán correctamente con estos tipos de cadenas.</span><span class="sxs-lookup"><span data-stu-id="026f1-133">This has no effect on the filter and the search filters will work correctly with these types of strings.</span></span>

<span data-ttu-id="026f1-134">Se aceptan caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="026f1-134">Wildcards are accepted.</span></span>

<span data-ttu-id="026f1-135">En el ejemplo de código siguiente se muestra un filtro que contiene una cadena codificada para **schemaIDGUID** con el valor GUID "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span><span class="sxs-lookup"><span data-stu-id="026f1-135">The following code example shows a filter that contains encoded string for **schemaIDGUID** with GUID value of "{BF967ABA-0DE6-11D0-A285-00AA003049E2}":</span></span>


```C++
(schemaidguid=\BA\7A\96\BF\E6\0D\D0\11\A2\85\00\AA\00\30\49\E2)
```



</dd> <dt>

<span data-ttu-id="026f1-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span><span class="sxs-lookup"><span data-stu-id="026f1-136"><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</span></span>
</dt> <dd>

<span data-ttu-id="026f1-137">El valor especificado en un filtro es la representación de cadena de bytes codificada del SID.</span><span class="sxs-lookup"><span data-stu-id="026f1-137">The value specified in a filter is the encoded byte string representation of the SID.</span></span> <span data-ttu-id="026f1-138">Para obtener más información sobre las cadenas de bytes codificadas, vea la sección anterior de este tema en la que se describe la sintaxis octetString.</span><span class="sxs-lookup"><span data-stu-id="026f1-138">For more information about encoded byte strings, see the previous section in this topic which discusses OctetString syntax.</span></span>

<span data-ttu-id="026f1-139">En el ejemplo de código siguiente se muestra un filtro que contiene una cadena codificada para **objectSid** con el valor de cadena SID "S-1-5-21-193565697-308236825-1417001333":</span><span class="sxs-lookup"><span data-stu-id="026f1-139">The following code example shows a filter that contains an encoded string for **objectSid** with SID string value of "S-1-5-21-1935655697-308236825-1417001333":</span></span>


```C++
(ObjectSid=\01\04\00\00\00\00\00\05\15\00\00\00\11\C3\5Fs\19R\5F\12u\B9uT)
```



</dd> <dt>

<span data-ttu-id="026f1-140"><span id="DN"></span><span id="dn"></span>Dn</span><span class="sxs-lookup"><span data-stu-id="026f1-140"><span id="DN"></span><span id="dn"></span>DN</span></span>
</dt> <dd>

<span data-ttu-id="026f1-141">Se debe proporcionar el nombre distintivo completo que se va a coincidir.</span><span class="sxs-lookup"><span data-stu-id="026f1-141">The entire distinguished name, to be matched, must be supplied.</span></span>

<span data-ttu-id="026f1-142">No se aceptan caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="026f1-142">Wildcards are not accepted.</span></span>

<span data-ttu-id="026f1-143">Tenga en cuenta que el **atributo objectCategory** también permite especificar **el lDAPDisplayName** de la clase establecida en el atributo .</span><span class="sxs-lookup"><span data-stu-id="026f1-143">Be aware that the **objectCategory** attribute also enables you to specify the **lDAPDisplayName** of the class set on the attribute.</span></span>

<span data-ttu-id="026f1-144">En el ejemplo siguiente se muestra un filtro que especifica un **miembro** que contiene "CN=TestUser,DC=Fabrikam,DC=COM":</span><span class="sxs-lookup"><span data-stu-id="026f1-144">The following example shows a filter that specifies a **member** that contains "CN=TestUser,DC=Fabrikam,DC=COM":</span></span>


```C++
(member=CN=TestUser,DC=Fabrikam,DC=COM)
```



</dd> <dt>

<span data-ttu-id="026f1-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span><span class="sxs-lookup"><span data-stu-id="026f1-145"><span id="INTEGER8"></span><span id="integer8"></span>INTEGER8</span></span>
</dt> <dd>

<span data-ttu-id="026f1-146">El valor especificado en un filtro debe ser un entero decimal.</span><span class="sxs-lookup"><span data-stu-id="026f1-146">The value specified in a filter must be a decimal integer.</span></span> <span data-ttu-id="026f1-147">Convertir valores hexadecimales en decimales.</span><span class="sxs-lookup"><span data-stu-id="026f1-147">Convert hexadecimal values to decimal.</span></span>

<span data-ttu-id="026f1-148">En el ejemplo de código siguiente se muestra un filtro que especifica un **valor creationTime** establecido en [**filetime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) de "1999-12-31 23:59:59 (UTC/GMT)":</span><span class="sxs-lookup"><span data-stu-id="026f1-148">The following code example shows a filter that specifies a **creationTime** set to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) of "1999-12-31 23:59:59 (UTC/GMT)":</span></span>


```C++
(creationTime=125911583990000000)
```



<span data-ttu-id="026f1-149">Las funciones siguientes crean un filtro de coincidencia exacta (=) para un atributo entero grande y comprueban el atributo en el esquema y su sintaxis:</span><span class="sxs-lookup"><span data-stu-id="026f1-149">The following functions create an exact match (=) filter for a large integer attribute and verify the attribute in the schema and its syntax:</span></span>


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

<span data-ttu-id="026f1-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span><span class="sxs-lookup"><span data-stu-id="026f1-150"><span id="PrintableString"></span><span id="printablestring"></span><span id="PRINTABLESTRING"></span>PrintableString</span></span>
</dt> <dd>

<span data-ttu-id="026f1-151">Los atributos con estas sintaxis deben cumplir con conjuntos de caracteres específicos.</span><span class="sxs-lookup"><span data-stu-id="026f1-151">Attributes with these syntaxes should adhere to specific character sets.</span></span> <span data-ttu-id="026f1-152">Para obtener más información, vea [Sintaxis para atributos en Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="026f1-152">For more information, see [Syntaxes for Attributes in Active Directory Domain Services](syntaxes-for-attributes-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="026f1-153">Actualmente, Active Directory Domain Services no aplican esos juegos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="026f1-153">Currently, Active Directory Domain Services do not enforce those character sets.</span></span>

<span data-ttu-id="026f1-154">El valor especificado en un filtro es una cadena.</span><span class="sxs-lookup"><span data-stu-id="026f1-154">The value specified in a filter is a string.</span></span> <span data-ttu-id="026f1-155">La comparación distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="026f1-155">The comparison is case-sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="026f1-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span><span class="sxs-lookup"><span data-stu-id="026f1-156"><span id="GeneralizedTime"></span><span id="generalizedtime"></span><span id="GENERALIZEDTIME"></span>GeneralizedTime</span></span>
</dt> <dd>

<span data-ttu-id="026f1-157">El valor especificado en un filtro es una cadena que representa la fecha con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="026f1-157">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYYYMMDDHHMMSS.0Z
```



<span data-ttu-id="026f1-158">"0Z" indica que no hay diferencias de tiempo.</span><span class="sxs-lookup"><span data-stu-id="026f1-158">"0Z" indicates no time differential.</span></span> <span data-ttu-id="026f1-159">Tenga en cuenta que Active Directory servidor almacena la fecha y hora como Hora media de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="026f1-159">Be aware that the Active Directory server stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="026f1-160">Si no se especifica un diferencial de hora, el valor predeterminado es GMT.</span><span class="sxs-lookup"><span data-stu-id="026f1-160">If a time differential is not specified, the default is GMT.</span></span>

<span data-ttu-id="026f1-161">Si la zona horaria local no es GMT, use un valor diferencial para especificar la zona horaria local y aplicar el diferencial a GMT.</span><span class="sxs-lookup"><span data-stu-id="026f1-161">If the local time zone is not GMT, use a differential value to specify your local time zone and apply the differential to GMT.</span></span> <span data-ttu-id="026f1-162">El diferencial se basa en: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="026f1-162">The differential is based on: GMT=Local+differential.</span></span>

<span data-ttu-id="026f1-163">Para especificar un diferencial, use:</span><span class="sxs-lookup"><span data-stu-id="026f1-163">To specify a differential, use:</span></span>


```C++
YYYYMMDDHHMMSS.0[+/-]HHMM
```



<span data-ttu-id="026f1-164">En el ejemplo siguiente se muestra un filtro que especifica una hora **whenCreated** establecida en 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="026f1-164">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(whenCreated=19990323205258.0Z)
```



<span data-ttu-id="026f1-165">En el ejemplo siguiente se muestra un filtro que especifica una hora **whenCreated** establecida en 3/23/99 8:52:58 PM Hora estándar de Nueva Zelanda (diferencial es +12 horas):</span><span class="sxs-lookup"><span data-stu-id="026f1-165">The following example shows a filter that specifies a **whenCreated** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is +12 hours):</span></span>


```C++
(whenCreated=19990323205258.0+1200)
```



<span data-ttu-id="026f1-166">En el ejemplo de código siguiente se muestra cómo calcular la diferencia de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="026f1-166">The following code example shows how to calculate time zone differential.</span></span> <span data-ttu-id="026f1-167">La función devuelve el diferencial entre la zona horaria local actual y GMT.</span><span class="sxs-lookup"><span data-stu-id="026f1-167">The function returns the differential between the current local time zone and GMT.</span></span> <span data-ttu-id="026f1-168">El valor devuelto es una cadena con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="026f1-168">The value returned is a string in the following format:</span></span>


```C++
[+/-]HHMM
```



<span data-ttu-id="026f1-169">Por ejemplo, la hora estándar del Pacífico es -0800.</span><span class="sxs-lookup"><span data-stu-id="026f1-169">For example, Pacific Standard Time is -0800.</span></span>


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

<span data-ttu-id="026f1-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>HORA UTC</span><span class="sxs-lookup"><span data-stu-id="026f1-170"><span id="UTCTime"></span><span id="utctime"></span><span id="UTCTIME"></span>UTCTime</span></span>
</dt> <dd>

<span data-ttu-id="026f1-171">El valor especificado en un filtro es una cadena que representa la fecha con el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="026f1-171">The value specified in a filter is a string that represents the date in the following form:</span></span>


```C++
YYMMDDHHMMSSZ
```



<span data-ttu-id="026f1-172">Z indica que no hay diferencias de tiempo.</span><span class="sxs-lookup"><span data-stu-id="026f1-172">Z indicates no time differential.</span></span> <span data-ttu-id="026f1-173">Tenga en cuenta que el Active Directory almacena la fecha y la hora como hora GMT.</span><span class="sxs-lookup"><span data-stu-id="026f1-173">Be aware that the Active Directory server stores date and time as GMT time.</span></span> <span data-ttu-id="026f1-174">Si no se especifica un diferencial de hora, GMT es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="026f1-174">If a time differential is not specified, GMT is the default.</span></span>

<span data-ttu-id="026f1-175">El valor de segundos ("SS") es opcional.</span><span class="sxs-lookup"><span data-stu-id="026f1-175">The seconds value ("SS") is optional.</span></span>

<span data-ttu-id="026f1-176">Si GMT no es la zona horaria local, aplique un valor diferencial local para especificar la zona horaria local.</span><span class="sxs-lookup"><span data-stu-id="026f1-176">If GMT is not the local time zone, apply a local differential value to specify your local time zone.</span></span> <span data-ttu-id="026f1-177">El diferencial es: GMT=Local+differential.</span><span class="sxs-lookup"><span data-stu-id="026f1-177">The differential is: GMT=Local+differential.</span></span>

<span data-ttu-id="026f1-178">Para especificar un diferencial, use el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="026f1-178">To specify a differential, use the following form:</span></span>


```C++
YYMMDDHHMMSS[+/-]HHMM
```



<span data-ttu-id="026f1-179">En el ejemplo siguiente se muestra un filtro que especifica una hora **myTimeAttrib** establecida en 3/23/99 8:52:58 PM GMT:</span><span class="sxs-lookup"><span data-stu-id="026f1-179">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM GMT:</span></span>


```C++
(myTimeAttrib=990323205258Z)
```



<span data-ttu-id="026f1-180">En el ejemplo siguiente se muestra un filtro que especifica un tiempo **myTimeAttrib** establecido en 3/23/99 8:52:58 PM sin segundos especificados:</span><span class="sxs-lookup"><span data-stu-id="026f1-180">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM without seconds specified:</span></span>


```C++
(myTimeAttrib=9903232052Z)
```



<span data-ttu-id="026f1-181">En el ejemplo siguiente se muestra un filtro que especifica una hora **myTimeAttrib** establecida en 3/23/99 8:52:58 PM Hora estándar de Nueva Zelanda (diferencial es 12 horas).</span><span class="sxs-lookup"><span data-stu-id="026f1-181">The following example shows a filter that specifies a **myTimeAttrib** time set to 3/23/99 8:52:58 PM New Zealand Standard Time (differential is 12 hours).</span></span> <span data-ttu-id="026f1-182">Esto equivale al 23/03/99 8:52:58 AM GMT.</span><span class="sxs-lookup"><span data-stu-id="026f1-182">This is equivalent to 3/23/99 8:52:58 AM GMT.</span></span>


```C++
(myTimeAttrib=990323205258+1200)
```



</dd> <dt>

<span data-ttu-id="026f1-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span><span class="sxs-lookup"><span data-stu-id="026f1-183"><span id="DirectoryString"></span><span id="directorystring"></span><span id="DIRECTORYSTRING"></span>DirectoryString</span></span>
</dt> <dd>

<span data-ttu-id="026f1-184">El valor especificado en un filtro es una cadena.</span><span class="sxs-lookup"><span data-stu-id="026f1-184">The value specified in a filter is a string.</span></span> <span data-ttu-id="026f1-185">DirectoryString puede contener caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="026f1-185">DirectoryString can contain Unicode characters.</span></span> <span data-ttu-id="026f1-186">La comparación distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="026f1-186">The comparison is case-insensitive.</span></span>

</dd> <dt>

<span data-ttu-id="026f1-187"><span id="OID"></span><span id="oid"></span>Oid</span><span class="sxs-lookup"><span data-stu-id="026f1-187"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="026f1-188">Se debe proporcionar el OID completo que se va a coincidir.</span><span class="sxs-lookup"><span data-stu-id="026f1-188">The entire OID to be matched must be supplied.</span></span>

<span data-ttu-id="026f1-189">No se aceptan caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="026f1-189">Wildcards are not accepted.</span></span>

<span data-ttu-id="026f1-190">El **atributo objectCategory** permite especificar el **valor lDAPDisplayName** del conjunto de clases para el atributo.</span><span class="sxs-lookup"><span data-stu-id="026f1-190">The **objectCategory** attribute enables you to specify the **lDAPDisplayName** of the class set for the attribute.</span></span>

<span data-ttu-id="026f1-191">En el ejemplo siguiente se muestra un filtro que especifica **governsID para** la clase de volumen:</span><span class="sxs-lookup"><span data-stu-id="026f1-191">The following example shows a filter that specifies **governsID** for volume class:</span></span>


```C++
(governsID=1.2.840.113556.1.5.36)
```



<span data-ttu-id="026f1-192">Dos filtros equivalentes que especifican el atributo **systemMustContain** que contiene **uNCName**, que tiene un OID de 1.2.840.113556.1.4.137:</span><span class="sxs-lookup"><span data-stu-id="026f1-192">Two equivalent filters that specifies **systemMustContain** attribute containing **uNCName**, which has an OID of 1.2.840.113556.1.4.137:</span></span>


```C++
(SystemMustContain=uNCName)
 
(SystemMustContain=1.2.840.113556.1.4.137)
```



</dd> <dt>

<span data-ttu-id="026f1-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Otras sintaxis</span><span class="sxs-lookup"><span data-stu-id="026f1-193"><span id="Other_Syntaxes"></span><span id="other_syntaxes"></span><span id="OTHER_SYNTAXES"></span>Other Syntaxes</span></span>
</dt> <dd>

<span data-ttu-id="026f1-194">Las sintaxis siguientes se evalúan en un filtro similar a una cadena de octeto:</span><span class="sxs-lookup"><span data-stu-id="026f1-194">The following syntaxes are evaluated in a filter similar to an octet string:</span></span>

-   <span data-ttu-id="026f1-195">ObjectSecurityDescriptor</span><span class="sxs-lookup"><span data-stu-id="026f1-195">ObjectSecurityDescriptor</span></span>
-   <span data-ttu-id="026f1-196">AccessPointDN</span><span class="sxs-lookup"><span data-stu-id="026f1-196">AccessPointDN</span></span>
-   <span data-ttu-id="026f1-197">PresentationAddresses</span><span class="sxs-lookup"><span data-stu-id="026f1-197">PresentationAddresses</span></span>
-   <span data-ttu-id="026f1-198">ReplicaLink</span><span class="sxs-lookup"><span data-stu-id="026f1-198">ReplicaLink</span></span>
-   <span data-ttu-id="026f1-199">DNWithString</span><span class="sxs-lookup"><span data-stu-id="026f1-199">DNWithString</span></span>
-   <span data-ttu-id="026f1-200">DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="026f1-200">DNWithOctetString</span></span>
-   <span data-ttu-id="026f1-201">ORName</span><span class="sxs-lookup"><span data-stu-id="026f1-201">ORName</span></span>

</dd> </dl>

 

 