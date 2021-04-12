---
title: Enlazar a un objeto mediante un SID
description: En Windows Server 2003, es posible enlazar a un objeto mediante el identificador de seguridad de objeto (SID) y un GUID. El SID del objeto se almacena en el atributo objectSID. El enlace a un SID no funciona en Windows 2000.
ms.assetid: 18b4613c-eb93-4204-96f2-0f91d7900587
ms.tgt_platform: multiple
keywords:
- Enlazar a un objeto con un SID AD
- Active Directory, usar, enlazar y enlazar a un objeto mediante un SID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad4ecf2d6faa385ab8085730e4f1cb0689e403
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487507"
---
# <a name="binding-to-an-object-using-a-sid"></a><span data-ttu-id="f766e-107">Enlazar a un objeto mediante un SID</span><span class="sxs-lookup"><span data-stu-id="f766e-107">Binding to an Object Using a SID</span></span>

<span data-ttu-id="f766e-108">En Windows Server 2003, es posible enlazar a un objeto mediante el identificador de seguridad de objeto (SID) y un GUID.</span><span class="sxs-lookup"><span data-stu-id="f766e-108">In Windows Server 2003, it is possible to bind to an object using the object Security Identifier (SID) as well as a GUID.</span></span> <span data-ttu-id="f766e-109">El SID del objeto se almacena en el atributo **objectSid** .</span><span class="sxs-lookup"><span data-stu-id="f766e-109">The object SID is stored in the **objectSID** attribute.</span></span> <span data-ttu-id="f766e-110">El enlace a un SID no funciona en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="f766e-110">Binding to an SID does not work on Windows 2000.</span></span>

<span data-ttu-id="f766e-111">El proveedor LDAP de Active Directory Domain Services proporciona un método para enlazar a un objeto mediante el SID del objeto.</span><span class="sxs-lookup"><span data-stu-id="f766e-111">The LDAP provider for Active Directory Domain Services provides a method to bind to an object using the object SID.</span></span> <span data-ttu-id="f766e-112">El formato de la cadena de enlace es:</span><span class="sxs-lookup"><span data-stu-id="f766e-112">The binding string format is:</span></span>


```C++
LDAP://servername/<SID=XXXXX>
```



<span data-ttu-id="f766e-113">En este ejemplo, "ServerName" es el nombre del servidor de directorio y "XXXXX" es la representación de cadena del valor hexadecimal del SID.</span><span class="sxs-lookup"><span data-stu-id="f766e-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the SID.</span></span> <span data-ttu-id="f766e-114">"ServerName" es opcional.</span><span class="sxs-lookup"><span data-stu-id="f766e-114">The "servername" is optional.</span></span> <span data-ttu-id="f766e-115">La cadena SID se especifica en un formulario en el que cada carácter de la cadena es la representación hexadecimal de cada byte del SID.</span><span class="sxs-lookup"><span data-stu-id="f766e-115">The SID string is specified in a form where each character in the string is the hexadecimal representation of each byte of the SID.</span></span> <span data-ttu-id="f766e-116">Por ejemplo, si la matriz es:</span><span class="sxs-lookup"><span data-stu-id="f766e-116">For example, if the array is:</span></span>


```C++
0xAB 0x14 0xE2
```



<span data-ttu-id="f766e-117">la cadena de enlace del SID sería " &lt; SID = AB14E2 &gt; ".</span><span class="sxs-lookup"><span data-stu-id="f766e-117">the SID binding string would be "&lt;SID=AB14E2&gt;".</span></span> <span data-ttu-id="f766e-118">La función [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) no debe usarse para convertir la matriz de SID en una cadena porque precede cada carácter de byte con una barra diagonal inversa, que no es un formato de cadena de enlace válido.</span><span class="sxs-lookup"><span data-stu-id="f766e-118">The [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) function should not be used to convert the SID array into a string because it precedes each byte character with a backslash, which is not a valid bind string format.</span></span>

<span data-ttu-id="f766e-119">La cadena SID también puede tener la forma " &lt; SID = S-x-x-XX-xxxxxxxxxx-xxxxxxxxxx-XXXXXXXXX-XXX &gt; ", donde la parte "S-X-x-XX-XXXXXXXXXX-xxxxxxxxxx-XXXXXXXXX-xxx" es la misma que la cadena devuelta por la función [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .</span><span class="sxs-lookup"><span data-stu-id="f766e-119">The SID string can also take the form "&lt;SID=S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX&gt;", where the "S-X-X-XX-XXXXXXXXXX-XXXXXXXXXX-XXXXXXXXX-XXX" portion is the same as the string returned by the [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) function.</span></span>

<span data-ttu-id="f766e-120">Al enlazar con el SID del objeto, no se admiten algunos métodos y propiedades de [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="f766e-120">When binding using the object SID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="f766e-121">Las siguientes propiedades de **IADs** no son compatibles con los objetos obtenidos mediante el enlace mediante el SID del objeto:</span><span class="sxs-lookup"><span data-stu-id="f766e-121">The following **IADs** properties are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="f766e-122">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="f766e-122">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="f766e-123">**Name**</span><span class="sxs-lookup"><span data-stu-id="f766e-123">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="f766e-124">**Parent**</span><span class="sxs-lookup"><span data-stu-id="f766e-124">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="f766e-125">Los métodos **IADsContainer** siguientes no son compatibles con los objetos obtenidos mediante el enlace mediante el SID del objeto:</span><span class="sxs-lookup"><span data-stu-id="f766e-125">The following **IADsContainer** methods are not supported by objects obtained by binding using the object SID:</span></span>

-   [<span data-ttu-id="f766e-126">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="f766e-126">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="f766e-127">**A**</span><span class="sxs-lookup"><span data-stu-id="f766e-127">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="f766e-128">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="f766e-128">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="f766e-129">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="f766e-129">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="f766e-130">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="f766e-130">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="f766e-131">Para usar estos métodos y propiedades después de enlazar a un objeto mediante el SID del objeto, use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el nombre distintivo del objeto y, a continuación, use el nombre distintivo para enlazarlo de nuevo al objeto.</span><span class="sxs-lookup"><span data-stu-id="f766e-131">To use these methods and properties after binding to an object using the object SID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="f766e-132">En el ejemplo de código siguiente se muestra cómo convertir un **objectSid** en una cadena enlazable.</span><span class="sxs-lookup"><span data-stu-id="f766e-132">The following code example shows how to convert an **objectSid** into a bindable string.</span></span>


```C++
HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes);

/********

    GetSIDBindStringFromVariant()

    Converts a SID in VARIANT form, such as an objectSid value, and 
    converts it into a bindable string in the form:

    LDAP://<SID=xxxxxxx...>

    The returned string is allocated with AllocADsMem and must be 
    freed by the caller with FreeADsMem.

*********/

LPWSTR GetSIDBindStringFromVariant(VARIANT vSID)
{
    LPWSTR pwszReturn = NULL;

    if(VT_ARRAY & vSID.vt) 
    {
        HRESULT hr;
        LPBYTE pByte;
        DWORD dwBytes = 0;

        hr = VariantArrayToBytes(vSID, &pByte, &dwBytes);
        if(S_OK == hr)
        {
            // Convert the BYTE array into a string of hex 
            // characters.
            CComBSTR sbstrTemp = "LDAP://<SID=";

            for(DWORD i = 0; i < dwBytes; i++)
            {
                WCHAR wszByte[3];

                swprintf_s(wszByte, L"%02x", pByte[i]);
                sbstrTemp += wszByte;
            }

            sbstrTemp += ">";
            pwszReturn = 
               (LPWSTR)AllocADsMem((sbstrTemp.Length() + 1) * 
                sizeof(WCHAR));
            if(pwszReturn)
            {
                wcscpy_s(pwszReturn, sbstrTemp.m_str);
            }

            FreeADsMem(pByte);
        }
    }

    return pwszReturn;
}

/*********

    VariantArrayToBytes()

    This function converts a VARIANT array into an array of BYTES. 
    This function allocates the buffer using AllocADsMem. The 
    caller must free this memory with FreeADsMem when it is no 
    longer required.

**********/

HRESULT VariantArrayToBytes(VARIANT Variant, 
    LPBYTE *ppBytes, 
    DWORD *pdwBytes)
{
    if(!(Variant.vt & VT_ARRAY) ||
        !Variant.parray ||
        !ppBytes ||
        !pdwBytes)
    {
        return E_INVALIDARG;
    }

    *ppBytes = NULL;
    *pdwBytes = 0;

    HRESULT hr = E_FAIL;
    SAFEARRAY *pArrayVal = NULL;
    CHAR HUGEP *pArray = NULL;
    
    // Retrieve the safe array.
    pArrayVal = Variant.parray;
    DWORD dwBytes = pArrayVal->rgsabound[0].cElements;
    *ppBytes = (LPBYTE)AllocADsMem(dwBytes);
    if(NULL == *ppBytes) 
    {
        return E_OUTOFMEMORY;
    }

    hr = SafeArrayAccessData(pArrayVal, (void HUGEP * FAR *) &pArray);
    if(SUCCEEDED(hr))
    {
        // Copy the bytes to the safe array.
        CopyMemory(*ppBytes, pArray, dwBytes);
        SafeArrayUnaccessData( pArrayVal );
        *pdwBytes = dwBytes;
    }
    
    return hr;
}
```



 

 