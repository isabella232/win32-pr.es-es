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
# <a name="binding-to-an-object-using-a-sid"></a>Enlazar a un objeto mediante un SID

En Windows Server 2003, es posible enlazar a un objeto mediante el identificador de seguridad de objeto (SID) y un GUID. El SID del objeto se almacena en el atributo **objectSid** . El enlace a un SID no funciona en Windows 2000.

El proveedor LDAP de Active Directory Domain Services proporciona un método para enlazar a un objeto mediante el SID del objeto. El formato de la cadena de enlace es:


```C++
LDAP://servername/<SID=XXXXX>
```



En este ejemplo, "ServerName" es el nombre del servidor de directorio y "XXXXX" es la representación de cadena del valor hexadecimal del SID. "ServerName" es opcional. La cadena SID se especifica en un formulario en el que cada carácter de la cadena es la representación hexadecimal de cada byte del SID. Por ejemplo, si la matriz es:


```C++
0xAB 0x14 0xE2
```



la cadena de enlace del SID sería " &lt; SID = AB14E2 &gt; ". La función [**ADsEncodeBinaryData**](/windows/desktop/api/adshlp/nf-adshlp-adsencodebinarydata) no debe usarse para convertir la matriz de SID en una cadena porque precede cada carácter de byte con una barra diagonal inversa, que no es un formato de cadena de enlace válido.

La cadena SID también puede tener la forma " &lt; SID = S-x-x-XX-xxxxxxxxxx-xxxxxxxxxx-XXXXXXXXX-XXX &gt; ", donde la parte "S-X-x-XX-XXXXXXXXXX-xxxxxxxxxx-XXXXXXXXX-xxx" es la misma que la cadena devuelta por la función [**ConvertSidToStringSid**](/windows/desktop/api/sddl/nf-sddl-convertsidtostringsida) .

Al enlazar con el SID del objeto, no se admiten algunos métodos y propiedades de [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) . Las siguientes propiedades de **IADs** no son compatibles con los objetos obtenidos mediante el enlace mediante el SID del objeto:

-   [**ADsPath**](/windows/desktop/ADSI/iads-property-methods)
-   [**Name**](/windows/desktop/ADSI/iads-property-methods)
-   [**Parent**](/windows/desktop/ADSI/iads-property-methods)

Los métodos **IADsContainer** siguientes no son compatibles con los objetos obtenidos mediante el enlace mediante el SID del objeto:

-   [**GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [**A**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [**Elimínelos**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [**CopyHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [**MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

Para usar estos métodos y propiedades después de enlazar a un objeto mediante el SID del objeto, use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el nombre distintivo del objeto y, a continuación, use el nombre distintivo para enlazarlo de nuevo al objeto.

En el ejemplo de código siguiente se muestra cómo convertir un **objectSid** en una cadena enlazable.


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



 

 