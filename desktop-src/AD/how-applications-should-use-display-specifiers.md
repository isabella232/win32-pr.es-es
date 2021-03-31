---
title: Cómo deben usar las aplicaciones los especificadores de presentación
description: Para mostrar Dominio de Active Directory objetos de servicio, utilice especificadores de presentación para obtener los datos de presentación localizados de los objetos de clase y atributo.
ms.assetid: 2ba62906-47ae-4aab-8cb1-a5734eae5984
ms.tgt_platform: multiple
keywords:
- Cómo deben usar las aplicaciones los especificadores de presentación AD
- especificadores de presentación AD, cómo las aplicaciones deben usar especificadores de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f7045b03da282a9c64b216031e3da03a427268
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797265"
---
# <a name="how-applications-should-use-display-specifiers"></a><span data-ttu-id="bfaae-105">Cómo deben usar las aplicaciones los especificadores de presentación</span><span class="sxs-lookup"><span data-stu-id="bfaae-105">How Applications Should Use Display Specifiers</span></span>

<span data-ttu-id="bfaae-106">Para mostrar Dominio de Active Directory objetos de servicio, utilice especificadores de presentación para obtener los datos de presentación localizados de los objetos de clase y atributo.</span><span class="sxs-lookup"><span data-stu-id="bfaae-106">To display Active Directory Domain Service objects, use display specifiers to obtain localized display data for class and attribute objects.</span></span> <span data-ttu-id="bfaae-107">Esto permite usar iconos y nombres para mostrar localizados y evitar la localización innecesaria de los datos para mostrar.</span><span class="sxs-lookup"><span data-stu-id="bfaae-107">This enables localized display names and icons to be used and avoids unnecessary localization of the display data.</span></span>

## <a name="display-names"></a><span data-ttu-id="bfaae-108">Nombres para mostrar</span><span class="sxs-lookup"><span data-stu-id="bfaae-108">Display Names</span></span>

<span data-ttu-id="bfaae-109">Las propiedades **classDisplayName** y **attributeDisplayNames** de los objetos de especificador de presentación para la configuración regional adecuada deben usarse para obtener el texto para mostrar de los nombres de clase y atributo.</span><span class="sxs-lookup"><span data-stu-id="bfaae-109">The **classDisplayName** and **attributeDisplayNames** properties of the display specifier objects for the appropriate locale should be used to obtain display text for class and attribute names.</span></span> <span data-ttu-id="bfaae-110">No use las propiedades **CN**, **classDisplayName** o **LDAPDisplayName** de los objetos **ClassSchema** o **attributeSchema** para obtener etiquetas de texto de visualización porque estos valores no están localizados.</span><span class="sxs-lookup"><span data-stu-id="bfaae-110">Do not use the **cn**, **classDisplayName** or **ldapDisplayName** properties of the **classSchema** or **attributeSchema** objects to obtain display text labels because these values are not localized.</span></span> <span data-ttu-id="bfaae-111">Para obtener más información sobre cómo recuperar el texto localizado de un objeto de clase, vea el siguiente código de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="bfaae-111">For more information about how to retrieve localized text for a class object, see the following sample code.</span></span>

## <a name="icons"></a><span data-ttu-id="bfaae-112">Iconos</span><span class="sxs-lookup"><span data-stu-id="bfaae-112">Icons</span></span>

<span data-ttu-id="bfaae-113">La propiedad **iconPath** de los objetos de especificador de presentación para la configuración regional adecuada debe usarse para obtener el icono que se va a mostrar para un objeto de clase.</span><span class="sxs-lookup"><span data-stu-id="bfaae-113">The **iconPath** property of the display specifier objects for the appropriate locale should be used to obtain the icon to display for a class object.</span></span> <span data-ttu-id="bfaae-114">Para obtener más información, vea [iconos de clase](class-icons.md).</span><span class="sxs-lookup"><span data-stu-id="bfaae-114">For more information, see [Class Icons](class-icons.md).</span></span> <span data-ttu-id="bfaae-115">Si no se especifica ningún icono localizado para un objeto de clase, se debe mostrar un icono predeterminado para el elemento.</span><span class="sxs-lookup"><span data-stu-id="bfaae-115">If no localized icon is specified for a class object, a default icon should be displayed for the item.</span></span>

## <a name="creating-new-objects"></a><span data-ttu-id="bfaae-116">Crear nuevos objetos</span><span class="sxs-lookup"><span data-stu-id="bfaae-116">Creating New Objects</span></span>

<span data-ttu-id="bfaae-117">Cuando sea posible, use los asistentes de creación de objetos adecuados para crear nuevos objetos.</span><span class="sxs-lookup"><span data-stu-id="bfaae-117">When possible, use the appropriate object creation wizards to create new objects.</span></span> <span data-ttu-id="bfaae-118">Para obtener más información, vea [invocación de los asistentes para creación desde la aplicación](invoking-creation-wizards-from-your-application.md).</span><span class="sxs-lookup"><span data-stu-id="bfaae-118">For more information, see [Invoking Creation Wizards from Your Application](invoking-creation-wizards-from-your-application.md).</span></span>


<span data-ttu-id="bfaae-119">En el ejemplo de código siguiente se muestra cómo obtener el texto para mostrar de una clase y un atributo de una clase.</span><span class="sxs-lookup"><span data-stu-id="bfaae-119">The following code example shows how to obtain the display text for a class and an attribute of a class.</span></span>


```C++
#include <atlbase.h>

/**************************************************************************

    GetClassDisplaySpecifierContainer()

**************************************************************************/

HRESULT GetClassDisplaySpecifierContainer(LPWSTR pwszClass, 
                                          LCID locale, 
                                          IADs **ppads)
{
    if((NULL == pwszClass) || (NULL == ppads))
    {
        return E_INVALIDARG;
    }

    *ppads = NULL;
    
    // If no locale is specified, use the default system locale.
    if(0 == locale)
    {
        locale = GetSystemDefaultLCID();
        if(0 == locale)
        {
            return E_FAIL;
        }
    }
 
    // Verify that it is a valid locale.
    if(!IsValidLocale(locale, LCID_SUPPORTED))
    {
        return E_INVALIDARG;
    }
 
    HRESULT hr;
    IADs *padsRoot = NULL;
 
    hr = ADsOpenObject( L"LDAP://rootDSE",
                        NULL,
                        NULL,
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADs,
                        (void**)&padsRoot);
 
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the DN to the configuration container.
        hr = padsRoot->Get(CComBSTR(L"configurationNamingContext"), &var);
        
        if(SUCCEEDED(hr))
        {
            WCHAR wszPath[MAX_PATH * 2];

            // Build the string to bind to the container for the
            // specified locale in the DisplaySpecifiers container.
            swprintf_s(wszPath, 
                L"LDAP://cn=%s-Display,cn=%x,cn=DisplaySpecifiers,%s", 
                pwszClass, 
                locale, 
                var.bstrVal);

            VariantClear(&var);
            
            // Bind to the container.
            hr = ADsOpenObject( wszPath,
                                NULL,
                                NULL,
                                ADS_SECURE_AUTHENTICATION,
                                IID_IADs,
                                (void**)ppads);
 
        }

        padsRoot->Release();
    }

    return hr;
}

/**************************************************************************

    GetClassDisplayLabel()

**************************************************************************/

HRESULT GetClassDisplayLabel(LPWSTR pwszClass, 
                             LCID locale, 
                             BSTR *pbstrClassLabel)
{
    if((NULL == pwszClass) || (NULL == pbstrClassLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrClassLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the classDisplayName property value.
        hr = padsDispSpec->Get(CComBSTR(L"classDisplayName"), &var);
        
        if(SUCCEEDED(hr))
        {
            if(VT_BSTR == var.vt)
            {
                // Do not free the BSTR. The caller will handle it.
                *pbstrClassLabel = var.bstrVal;
            }
            else
            {
                VariantClear(&var);
                hr = E_FAIL;
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

/**************************************************************************

    GetAttributeDisplayLabel()

**************************************************************************/

HRESULT GetAttributeDisplayLabel(LPWSTR pwszClass, 
                                 LPWSTR pwszAttribute, 
                                 LCID locale, 
                                 BSTR *pbstrAttributeLabel)
{
    if( (NULL == pwszClass) || 
        (NULL == pwszAttribute) || 
        (NULL == pbstrAttributeLabel))
    {
        return E_INVALIDARG;
    }

    *pbstrAttributeLabel = NULL;
    
    HRESULT hr;
    IADs *padsDispSpec;
    hr = GetClassDisplaySpecifierContainer(pwszClass, locale, &padsDispSpec);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);

        // Get the attributeDisplayNames property values
        hr = padsDispSpec->GetEx(CComBSTR(L"attributeDisplayNames"), &var);
        
        if(SUCCEEDED(hr))
        {
            LONG        lStart, 
                        lEnd,
                        i;
            SAFEARRAY   *psa;
            VARIANT     varItem;

            VariantInit(&varItem);

            psa = V_ARRAY(&var);

            // Get the lower and upper bound.
            hr = SafeArrayGetLBound(psa, 1, &lStart);
            hr = SafeArrayGetUBound(psa, 1, &lEnd);

            /*
            The attributeDisplayNames values take the form 
            "<attribute name>,<display name>". Enumerate the values, looking 
            for the one that begins with the specified attribute name.
            */
            for(i = lStart; i <= lEnd; i++)
            {
                hr = SafeArrayGetElement(psa, &i, &varItem);
                if(SUCCEEDED(hr))
                {
                    WCHAR   wszTemp[MAX_PATH];

                    wcsncpy_s(wszTemp, 
                        V_BSTR(&varItem), 
                        lstrlenW(pwszAttribute) + 1);
                
                    if(0 == lstrcmpiW(pwszAttribute, wszTemp))
                    {
                        LPWSTR  pwszDisplayLabel;

                        /*
                        The proper value was found. Now, parse the value, looking 
                        for the first comma, which delimits the attribute name 
                        from the display name.
                        */
                        for(    pwszDisplayLabel = V_BSTR(&varItem); 
                                *pwszDisplayLabel; 
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel))
                        {
                            if(',' == *pwszDisplayLabel)
                            {
                                /*
                                The delimiter was found. Set the string 
                                pointer to the next character, which is the 
                                first character of the display name.
                                */
                                pwszDisplayLabel = CharNextW(pwszDisplayLabel);
                                break;
                            }
                        }
                        
                        if(*pwszDisplayLabel)
                        {
                            // Copy the display name to the output.
                            *pbstrAttributeLabel = CComBSTR(pwszDisplayLabel).Detach();

                            hr = S_OK;
                        }

                        /*
                        Release the item variant because the break prevents 
                        it from getting released by the VariantClear call below.
                        */
                        VariantClear(&varItem);

                        break;
                    }

                    VariantClear(&varItem);
                }
            }
        }
        
        padsDispSpec->Release();
    }

    return hr;
}

```



 

 




