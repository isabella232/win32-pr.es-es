---
title: Contenedor DisplaySpecifiers
description: Los especificadores de presentación se almacenan, por configuración regional, en el contenedor DisplaySpecifiers del contenedor de configuración. Dado que el contenedor de configuración se replica en todo el bosque, los especificadores de presentación se propagan por todos los dominios de un bosque.
ms.assetid: d7647c50-f95c-41ef-8d67-dc72542cae5a
ms.tgt_platform: multiple
keywords:
- Contenedor DisplaySpecifiers
- Contenedor, especificadores de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 406258a6c9983581491420a49621e3d10df4601e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487455"
---
# <a name="displayspecifiers-container"></a>Contenedor DisplaySpecifiers

Los especificadores de presentación se almacenan, por configuración regional, en el contenedor DisplaySpecifiers del contenedor de configuración. Dado que el contenedor de configuración se replica en todo el bosque, los especificadores de presentación se propagan por todos los dominios de un bosque.

El contenedor de configuración almacena el contenedor DisplaySpecifiers, que almacena los contenedores que corresponden a cada configuración regional. Estos contenedores de configuración regional se denominan mediante la representación hexadecimal del identificador de configuración regional. Por ejemplo, el contenedor de configuración regional de EE. UU./inglés se denomina 409, el contenedor de la configuración regional alemana se denomina 407 y el contenedor de la configuración regional en japonés se denomina 411. Para obtener más información y una lista de los identificadores de idioma posibles, consulte [constantes y cadenas de identificador de idioma](/windows/desktop/Intl/language-identifier-constants-and-strings).

Cada contenedor de configuración regional almacena objetos de la clase [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) .

Para enumerar todos los especificadores de presentación de una configuración regional, enumere todos los objetos [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) en el contenedor de configuración regional especificado dentro del contenedor DisplaySpecifiers.

El ejemplo de código siguiente contiene una función que se enlaza al contenedor del especificador de presentación para la configuración regional especificada:


```C++
/**********
This function returns a pointer to the display specifier container 
for the specified locale.

If locale is NULL, use default system locale and then return the 
locale in the locale parameter.
***********/
HRESULT BindToDisplaySpecifiersContainerByLocale(
    LCID *locale,
    IADs **ppDispSpecCont)
{
HRESULT hr = E_FAIL;
 
if ((!ppDispSpecCont)||(!locale))
    return E_POINTER;
 
// If no locale is specified, use the default system locale.
if (!(*locale))
{
    *locale = GetSystemDefaultLCID();
    if (!(*locale))
        return E_FAIL;
}
 
// Be sure that the locale is valid.
if (!IsValidLocale(*locale, LCID_SUPPORTED))
    return E_INVALIDARG;
 
LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
IADs *pObj = NULL;
VARIANT var;
 
hr = ADsOpenObject(L"LDAP://rootDSE",
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)&pObj);
 
if (SUCCEEDED(hr))
{
    // Get the DN to the configuration container.
    hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
    if (SUCCEEDED(hr))
    {
        // Build the string to bind to the container for the
        // specified locale in the DisplaySpecifiers container.
        swprintf_s(
            szPath, 
            L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", 
            *locale, 
            var.bstrVal);

        // Bind to the container.
        *ppDispSpecCont = NULL;
        hr = ADsOpenObject(szPath,
                     NULL,
                     NULL,
                     ADS_SECURE_AUTHENTICATION,
                     IID_IADs,
                     (void**)ppDispSpecCont);
 
        if(FAILED(hr))
        {
            if ((*ppDispSpecCont))
            {
                (*ppDispSpecCont)->Release();
                (*ppDispSpecCont) = NULL;
            }
        }
    }
}
 
// Cleanup.
VariantClear(&var);
if (pObj)
    pObj->Release();
 
return hr;
}
```



 

 