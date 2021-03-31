---
title: Sintaxis de atributo ADSI
description: Cada atributo del directorio tiene una sintaxis asociada. Por ejemplo, integer, String, Numeric, etc. ADSI define su propia sintaxis que se asigna a la sintaxis de directorio nativo. En esta sección se describen los tipos de sintaxis de atributo de ADSI.
ms.assetid: 83d3d42f-e35e-4bd1-b26e-d141e9ec9c31
ms.tgt_platform: multiple
keywords:
- atributos ADSI, sintaxis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23d58b48b27fa88077f388b47535afd1dbd0a4f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793810"
---
# <a name="adsi-attribute-syntax"></a><span data-ttu-id="934a5-107">Sintaxis de atributo ADSI</span><span class="sxs-lookup"><span data-stu-id="934a5-107">ADSI Attribute Syntax</span></span>

<span data-ttu-id="934a5-108">Cada atributo del directorio tiene una sintaxis asociada.</span><span class="sxs-lookup"><span data-stu-id="934a5-108">Each attribute in the directory has an associated syntax.</span></span> <span data-ttu-id="934a5-109">Por ejemplo, integer, String, Numeric, etc.</span><span class="sxs-lookup"><span data-stu-id="934a5-109">For example, integer, string, numeric, and so on.</span></span> <span data-ttu-id="934a5-110">ADSI define su propia sintaxis que se asigna a la sintaxis de directorio nativo.</span><span class="sxs-lookup"><span data-stu-id="934a5-110">ADSI defines its own syntax that maps to the native directory syntax.</span></span> <span data-ttu-id="934a5-111">En esta sección se describen los tipos de sintaxis de atributo de ADSI.</span><span class="sxs-lookup"><span data-stu-id="934a5-111">This section describes the types of attribute syntaxes in ADSI.</span></span>

## <a name="distinguished-name-string"></a><span data-ttu-id="934a5-112">Cadena de nombre distintivo</span><span class="sxs-lookup"><span data-stu-id="934a5-112">Distinguished Name String</span></span>


```VB
Syntax Type: ADSTYPE_DN_STRING
```



<span data-ttu-id="934a5-113">El nombre distintivo es útil para vincular dos objetos a la vez.</span><span class="sxs-lookup"><span data-stu-id="934a5-113">The distinguished name is useful for linking two objects together.</span></span> <span data-ttu-id="934a5-114">Por ejemplo, puede crear un vínculo que convierte el objeto Alice en Administrador del objeto Bob.</span><span class="sxs-lookup"><span data-stu-id="934a5-114">For example, it can create a link that makes the Alice object a manager of the Bob object.</span></span> <span data-ttu-id="934a5-115">Si el objeto Alice se mueve a una ubicación diferente, el vínculo de administrador entre Alice y Bob se actualiza automáticamente.</span><span class="sxs-lookup"><span data-stu-id="934a5-115">If the Alice object moves to different place, the manager link between Alice and Bob is updated automatically.</span></span>

<span data-ttu-id="934a5-116">El nombre distintivo debe contener un objeto de nombre distintivo válido.</span><span class="sxs-lookup"><span data-stu-id="934a5-116">The distinguished name must contain a valid distinguished name object.</span></span> <span data-ttu-id="934a5-117">Si el nombre distintivo no se corresponde con un objeto existente válido, la mayoría de los servidores rechazan la solicitud y devuelven un error de infracción de restricción.</span><span class="sxs-lookup"><span data-stu-id="934a5-117">If the distinguished name does not correspond to a valid existing object, most servers reject the request and return a constraint violation error.</span></span>

<span data-ttu-id="934a5-118">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="934a5-118">Examples:</span></span>


```VB
Set x = GetObject("LDAP://CN=Bob, OU=Sales,DC=Fabrikam, DC=com)
x.Put "manager", "CN=Alice, OU=Sales, DC=Fabrikam, DC=COM"
x.SetInfo
 
PADS_ATTR_INFO pInfo;
// .. IDirectoryObject::GetObjectAttribute
printf("%S\n", pInfo->pADsValues->DNString );
```



## <a name="case-exact-string-and-case-ignore-string"></a><span data-ttu-id="934a5-119">Cadena exacta de caso y diferencia de mayúsculas y minúsculas</span><span class="sxs-lookup"><span data-stu-id="934a5-119">Case Exact String and Case Ignore String</span></span>


```VB
Syntax Types: ADSTYPE_CASE_IGNORE_STRING, ADSTYPE_CASE_EXACT_STRING.
```



<span data-ttu-id="934a5-120">Case Exact String es una cadena que distingue entre mayúsculas y minúsculas, mientras que Case ignore String es una cadena que no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="934a5-120">Case Exact String is a case-sensitive string while Case Ignore String is a case-insensitive string.</span></span> <span data-ttu-id="934a5-121">Un gran porcentaje de atributos en el directorio usa esta sintaxis.</span><span class="sxs-lookup"><span data-stu-id="934a5-121">A large percentage of attributes in the directory use this syntax.</span></span>

> [!Note]  
> <span data-ttu-id="934a5-122">El directorio puede almacenarlo o no como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="934a5-122">The directory may or may not store this as a Unicode string.</span></span> <span data-ttu-id="934a5-123">Sin embargo, ADSI acepta y devuelve cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="934a5-123">However, ADSI accepts and returns Unicode strings.</span></span>

 

<span data-ttu-id="934a5-124">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="934a5-124">Example:</span></span>


```VB
Dim propList As IADsPropertyList
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
Set propVal = New PropertyValue
 
' --- Property Value ---
propVal.CaseIgnoreString = "Fabrikam, Inc - Seattle, WA"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
```



## <a name="printable-string"></a><span data-ttu-id="934a5-125">Cadena imprimible</span><span class="sxs-lookup"><span data-stu-id="934a5-125">Printable String</span></span>


```VB
Syntax Type: ADSTYPE_PRINTABLE_STRING
```



<span data-ttu-id="934a5-126">Esta sintaxis se usa para los atributos con valores de cadena en los que las mayúsculas y minúsculas se consideran diferentes para las comparaciones, por ejemplo, "FABRIKAM" y "fabrikam" no coinciden.</span><span class="sxs-lookup"><span data-stu-id="934a5-126">This syntax is used for attributes with string values where uppercase and lowercase are considered unequal for comparisons, for example, "FABRIKAM" and "Fabrikam" do not match.</span></span> <span data-ttu-id="934a5-127">ADSI acepta todo el contenido de una cadena imprimible; no intenta comprobar si realmente se pueden imprimir.</span><span class="sxs-lookup"><span data-stu-id="934a5-127">ADSI accepts any contents for a Printable-String; it does not attempt to verify that they are indeed printable.</span></span>

## <a name="numeric-string"></a><span data-ttu-id="934a5-128">Cadena numérica</span><span class="sxs-lookup"><span data-stu-id="934a5-128">Numeric String</span></span>


```VB
Syntax Type: ADSTYPE_NUMERIC_STRING
```



<span data-ttu-id="934a5-129">En esta sintaxis, las cadenas coinciden como en la cadena imprimible, excepto en que se omiten todos los caracteres de espacio en las comparaciones.</span><span class="sxs-lookup"><span data-stu-id="934a5-129">In this syntax, strings match as in Printable String, except that all space characters are ignored in comparisons.</span></span> <span data-ttu-id="934a5-130">ADSI no realiza la comprobación de valores para asegurarse de que solo los números y espacios aparecen en los valores de esta sintaxis.</span><span class="sxs-lookup"><span data-stu-id="934a5-130">ADSI does not perform value checking to ensure that only numerals and spaces appear in values of this syntax.</span></span> <span data-ttu-id="934a5-131">Active Directory acepta cualquier contenido para una cadena numérica; no comprueba que los caracteres sean numéricos.</span><span class="sxs-lookup"><span data-stu-id="934a5-131">Active Directory accepts any content for a numeric string; it does not verify that the characters are numeric.</span></span>

## <a name="utc-time"></a><span data-ttu-id="934a5-132">Hora UTC</span><span class="sxs-lookup"><span data-stu-id="934a5-132">UTC Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="934a5-133">Esta sintaxis almacena la fecha y la hora en una sola cadena.</span><span class="sxs-lookup"><span data-stu-id="934a5-133">This syntax stores the date and time in a single string.</span></span> <span data-ttu-id="934a5-134">El formato de cadena consta de tres partes concatenadas: (1) AAMMDD; (2) HHMM o HHMMSS (ambos son aceptables); y (3) "Z" para indicar que la hora dada es la hora del meridiano de Greenwich (GMT) o "+/-HHMM" para indicar que la hora dada es la hora local con la diferencia diferencial de GMT.</span><span class="sxs-lookup"><span data-stu-id="934a5-134">The string format consists of three concatenated parts: (1) YYMMDD; (2) HHMM or HHMMSS (both are acceptable); and (3) "Z" to indicate that the time given is Greenwich Mean Time (GMT), or "+/-HHMM" to indicate that the time given is local time with the given differential from GMT.</span></span> <span data-ttu-id="934a5-135">La diferencia se basa en la fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="934a5-135">The differential is based on the formula: GMT=Local+differential.</span></span>

> [!Note]  
> <span data-ttu-id="934a5-136">Los dos primeros dígitos del año no se almacenan en esta cadena.</span><span class="sxs-lookup"><span data-stu-id="934a5-136">The first two digits of the year are not stored in this string.</span></span>

 

<span data-ttu-id="934a5-137">Algunos ejemplos de valores válidos son "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503 + 0130".</span><span class="sxs-lookup"><span data-stu-id="934a5-137">Some examples of legal values are "9101311455Z", "910131145503Z", "9101314455-0500", "910131145503+0130".</span></span> <span data-ttu-id="934a5-138">Esta cadena se almacena como caracteres ASCII de un solo byte y no se almacena ningún número de página de códigos.</span><span class="sxs-lookup"><span data-stu-id="934a5-138">This string is stored as single-byte ASCII characters, and no code page number is stored with it.</span></span>

<span data-ttu-id="934a5-139">Aunque se admite la ordenación, solo se realiza como una ordenación de cadenas sin distinción entre mayúsculas y minúsculas ASCII, no interpretando correctamente el significado de las cadenas.</span><span class="sxs-lookup"><span data-stu-id="934a5-139">Although ordering is supported, it is done only as an ASCII case-insensitive string sort, not by properly interpreting the meaning of the strings.</span></span>

<span data-ttu-id="934a5-140">Se acepta cualquier valor de cadena válido.</span><span class="sxs-lookup"><span data-stu-id="934a5-140">Any valid string value is accepted.</span></span> <span data-ttu-id="934a5-141">No se realiza ningún intento para asegurarse de que la cadena contiene una cadena de hora válida.</span><span class="sxs-lookup"><span data-stu-id="934a5-141">No attempt is made to ensure that the string contains a valid time string.</span></span>

## <a name="generalized-time"></a><span data-ttu-id="934a5-142">Tiempo generalizado</span><span class="sxs-lookup"><span data-stu-id="934a5-142">Generalized Time</span></span>


```VB
Syntax Type: ADSTYPE_UTC_TIME
```



<span data-ttu-id="934a5-143">Si se está definiendo un nuevo atributo para almacenar valores de hora, se debe usar la sintaxis de GeneralizedTime.</span><span class="sxs-lookup"><span data-stu-id="934a5-143">If a new attribute to store time values is being defined, the GeneralizedTime syntax should be used.</span></span> <span data-ttu-id="934a5-144">La sintaxis GeneralizedTime usa cuatro caracteres para representar el año en lugar de dos como con UTCTime.</span><span class="sxs-lookup"><span data-stu-id="934a5-144">GeneralizedTime syntax uses four characters to represent the year instead of two as with UTCTime.</span></span>

<span data-ttu-id="934a5-145">El formato de la sintaxis de GeneralizedTime es "AAAAMMDDHHMMSS. 0Z".</span><span class="sxs-lookup"><span data-stu-id="934a5-145">The format for the GeneralizedTime syntax is "YYYYMMDDHHMMSS.0Z".</span></span> <span data-ttu-id="934a5-146">Un ejemplo de un valor aceptable es "20010928060000.0 Z".</span><span class="sxs-lookup"><span data-stu-id="934a5-146">An example of an acceptable value is "20010928060000.0Z".</span></span> <span data-ttu-id="934a5-147">La "Z" no indica ninguna diferencia horaria.</span><span class="sxs-lookup"><span data-stu-id="934a5-147">The "Z" indicates no time differential.</span></span> <span data-ttu-id="934a5-148">Active Directory almacena la fecha y hora como hora del meridiano de Greenwich (GMT).</span><span class="sxs-lookup"><span data-stu-id="934a5-148">Active Directory stores date/time as Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="934a5-149">Si no se especifica ninguna diferencia horaria, GMT es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="934a5-149">If no time differential is specified, GMT is the default.</span></span>

<span data-ttu-id="934a5-150">Si se especifica la hora en una zona horaria distinta de GMT, la diferencia entre la zona horaria y GMT se anexa a la cadena en lugar de a "Z" en la forma "aaaammddhhmmss. 0 \[ +/- \] hhmm".</span><span class="sxs-lookup"><span data-stu-id="934a5-150">If the time is specified in a time zone other than GMT, the differential between the time zone and GMT is appended to the string instead of "Z" in the form "YYYYMMDDHHMMSS.0\[+/-\]HHMM".</span></span> <span data-ttu-id="934a5-151">Un ejemplo de un valor aceptable es "20010928060000.0 + 0200".</span><span class="sxs-lookup"><span data-stu-id="934a5-151">An example of an acceptable value is "20010928060000.0+0200".</span></span>

<span data-ttu-id="934a5-152">La diferencia se basa en la fórmula: GMT = local + diferencial.</span><span class="sxs-lookup"><span data-stu-id="934a5-152">The differential is based on the formula: GMT=Local+differential.</span></span>

## <a name="boolean"></a><span data-ttu-id="934a5-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="934a5-153">Boolean</span></span>


```VB
Syntax Type: ADSTYPE_BOOLEAN
```



<span data-ttu-id="934a5-154">Active Directory solo acepta un valor de 32 bits con signo para esta sintaxis.</span><span class="sxs-lookup"><span data-stu-id="934a5-154">Active Directory accepts only a signed 32-bit value for this syntax.</span></span> <span data-ttu-id="934a5-155">Trata cero como **false** y todos los valores distintos de cero como **true**.</span><span class="sxs-lookup"><span data-stu-id="934a5-155">It handles zero as **FALSE** and all nonzero values as **TRUE**.</span></span>

## <a name="integer"></a><span data-ttu-id="934a5-156">Entero</span><span class="sxs-lookup"><span data-stu-id="934a5-156">Integer</span></span>


```VB
Syntax Type: ADSTYPE_INTEGER
```



<span data-ttu-id="934a5-157">Valor numérico con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="934a5-157">A 32-bit signed numeric value.</span></span>

## <a name="large-integer"></a><span data-ttu-id="934a5-158">Entero grande</span><span class="sxs-lookup"><span data-stu-id="934a5-158">Large Integer</span></span>


```VB
Syntax Type: ADSTYPE_LARGE_INTEGER
```



<span data-ttu-id="934a5-159">Valor numérico con signo de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="934a5-159">A 64-bit signed numeric value.</span></span> <span data-ttu-id="934a5-160">Los enteros grandes se implementan realmente como objetos COM en la interfaz [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) .</span><span class="sxs-lookup"><span data-stu-id="934a5-160">Large integers are actually implemented as COM objects on the [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger) interface.</span></span> <span data-ttu-id="934a5-161">Los métodos **HighPart** y **LowPart** se usan para tener acceso a las mitades de 2 32 bits del valor entero grande.</span><span class="sxs-lookup"><span data-stu-id="934a5-161">The **HighPart** and **LowPart** methods are used to access the two 32-bit halves of the large integer value.</span></span>

<span data-ttu-id="934a5-162">Ejemplo:</span><span class="sxs-lookup"><span data-stu-id="934a5-162">Example:</span></span>


```VB
Dim x as IADsLargeInteger
Set o = GetObject("LDAP://DC=Fabrikam,DC=com")
Set x = o.Get("UsnCreated")
Debug.Print x.HighPart
Debug.Print x.LowPart
```



## <a name="octet-string"></a><span data-ttu-id="934a5-163">Cadena de octeto</span><span class="sxs-lookup"><span data-stu-id="934a5-163">Octet String</span></span>


```VB
Syntax Type: ADSTYPE_OCTET_STRING
```



<span data-ttu-id="934a5-164">Una cadena de octeto se devuelve como una matriz de bytes variante de bytes.</span><span class="sxs-lookup"><span data-stu-id="934a5-164">An octet string is returned as a variant array of bytes.</span></span> <span data-ttu-id="934a5-165">Se compone de un recuento de tamaño (número de octetos) seguido de una serie de octetos.</span><span class="sxs-lookup"><span data-stu-id="934a5-165">This consists of a size count (number of octets) followed by a series of octets.</span></span> <span data-ttu-id="934a5-166">Un octeto es un byte de 8 bits, por lo que una serie de octetos es una cadena de datos binarios.</span><span class="sxs-lookup"><span data-stu-id="934a5-166">An octet is an 8-bit byte, so a series of octets is a string of binary data.</span></span>

## <a name="object-class"></a><span data-ttu-id="934a5-167">Clase de objeto</span><span class="sxs-lookup"><span data-stu-id="934a5-167">Object Class</span></span>


```VB
Syntax Type: ADSTYPE_CASE_IGNORE_STRING
```



<span data-ttu-id="934a5-168">La clase de objeto es un identificador de objeto único para una clase de esquema determinada.</span><span class="sxs-lookup"><span data-stu-id="934a5-168">Object Class is a unique object identifier for a given schema class.</span></span> <span data-ttu-id="934a5-169">La clase de cada instancia de objeto se identifica mediante el atributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="934a5-169">The class of each object instance is identified by the **objectClass** attribute.</span></span> <span data-ttu-id="934a5-170">Cuando se crea, nunca se puede cambiar una clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="934a5-170">When created, you can never change an object class.</span></span> <span data-ttu-id="934a5-171">**objectClass** es un atributo con valores múltiples.</span><span class="sxs-lookup"><span data-stu-id="934a5-171">**objectClass** is a multiple valued attribute.</span></span> <span data-ttu-id="934a5-172">Muestra la clase específica del objeto y las clases de todas las clases estructurales o abstractas de las que se deriva la clase específica.</span><span class="sxs-lookup"><span data-stu-id="934a5-172">It lists the specific class of the object, and the classes of all structural or abstract classes from which the specific class was derived.</span></span> <span data-ttu-id="934a5-173">Esto incluye la parte superior, la clase de la que se derivan todas las demás clases.</span><span class="sxs-lookup"><span data-stu-id="934a5-173">This includes Top, the class from which all other classes are ultimately derived.</span></span> <span data-ttu-id="934a5-174">Active Directory no enumera las clases auxiliares en el atributo **objectClass** .</span><span class="sxs-lookup"><span data-stu-id="934a5-174">Active Directory does not list auxiliary classes in the **objectClass** attribute.</span></span>

## <a name="security-descriptor"></a><span data-ttu-id="934a5-175">Descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="934a5-175">Security Descriptor</span></span>


```VB
Syntax Type: ADSTYPE_NT_SECURITY_DESCRIPTOR
```



<span data-ttu-id="934a5-176">Los derechos de acceso definen qué capacidades tiene una entidad de seguridad cuando intenta realizar una operación en un objeto de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="934a5-176">Access rights define what abilities a security principal has when it attempts to perform an operation on an Active Directory object.</span></span> <span data-ttu-id="934a5-177">Un descriptor de seguridad describe la información de control de acceso asociada a un objeto.</span><span class="sxs-lookup"><span data-stu-id="934a5-177">A security descriptor describes the access control information associated with an object.</span></span>

<span data-ttu-id="934a5-178">El descriptor de seguridad se almacena como una propiedad de un objeto de directorio en la propiedad **nTSecurityDescriptor** .</span><span class="sxs-lookup"><span data-stu-id="934a5-178">The security descriptor is stored as a property of a directory object in the **nTSecurityDescriptor** property.</span></span> <span data-ttu-id="934a5-179">Cuando un usuario autenticado intenta tener acceso a un objeto de directorio, el servidor de directorio determina el acceso concedido o denegado al usuario basándose en el descriptor de seguridad del objeto.</span><span class="sxs-lookup"><span data-stu-id="934a5-179">When an authenticated user attempts to access a directory object, the directory server determines the access granted or denied to the user based on the object security descriptor.</span></span>

<span data-ttu-id="934a5-180">La enumeración de enumeración de [**\_ \_ control \_ SD de ADS**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) especifica las marcas de control de un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="934a5-180">The [**ADS\_SD\_CONTROL\_ENUM**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum) enumeration specifies control flags for a security descriptor.</span></span>

<span data-ttu-id="934a5-181">En el ejemplo de código siguiente se muestra cómo obtener un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="934a5-181">The following code example shows how to obtain a security descriptor.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="934a5-182">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="934a5-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="934a5-183">Sintaxis para atributos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="934a5-183">Syntaxes for Active Directory Attributes</span></span>](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)
</dt> <dt>

[<span data-ttu-id="934a5-184">Elección de una sintaxis</span><span class="sxs-lookup"><span data-stu-id="934a5-184">Choosing a Syntax</span></span>](/windows/desktop/AD/choosing-a-syntax)
</dt> <dt>

[<span data-ttu-id="934a5-185">Cómo especificar valores de comparación</span><span class="sxs-lookup"><span data-stu-id="934a5-185">How to Specify Comparison Values</span></span>](/windows/desktop/AD/how-to-specify-comparison-values)
</dt> </dl>

 

 