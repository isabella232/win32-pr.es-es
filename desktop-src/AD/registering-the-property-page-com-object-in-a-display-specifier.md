---
title: Registrar el objeto COM de la página de propiedades en un especificador de presentación
description: En este tema se muestra cómo registrar un archivo DLL de extensión que contiene una Active Directory hoja de propiedades con el registro de Windows y Active Directory.
ms.assetid: e2d6142b-c2fe-4435-b4af-83f7cd45218b
ms.tgt_platform: multiple
keywords:
- Registrar el objeto COM de la página de propiedades en un especificador de presentación Active Directory
- objeto COM de la página de propiedades Active Directory, registrar en un especificador de presentación
- especificadores de presentación Active Directory, registrando el objeto COM de la página de propiedades en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5b08ac0ea6329026a6d367e71064bde917b1a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149167"
---
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a>Registrar el objeto COM de la página de propiedades en un especificador de presentación

Cuando se usa COM para crear un archivo DLL de extensión de hoja de propiedades para Active Directory Domain Services, también se debe registrar la extensión con el registro de Windows y Active Directory Domain Services. El registro de la extensión permite que el Active Directory complementos de MMC administrativos y el shell de Windows reconozcan la extensión.

## <a name="registering-in-the-windows-registry"></a>Registro en el registro de Windows

Al igual que todos los servidores COM, se debe registrar una extensión de la hoja de propiedades en el registro de Windows. La extensión se registra con la siguiente clave.

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*<clsid>* es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . En la *<clsid>* clave, hay una clave **InProcServer32** que identifica el objeto como servidor de 32 bits en proceso. En la clave **InProcServer32** , la ubicación del archivo dll se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el valor **ThreadingModel** . Todas las extensiones de la hoja de propiedades deben usar el modelo de subprocesos "Apartamento".

## <a name="registering-with-active-directory-domain-services"></a>Registro con Active Directory Domain Services

El registro de la extensión de la hoja de propiedades es específico de una configuración regional. Si la extensión de la hoja de propiedades se aplica a todas las configuraciones regionales, debe registrarse en el objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la clase de objeto en todos los subcontenedores de la configuración regional en el contenedor de especificadores de presentación. Si la extensión de la hoja de propiedades está localizada para una configuración regional determinada, regístrela en el objeto **displaySpecifier** del subcontenedor de la configuración regional. Para obtener más información sobre el contenedor de especificadores de presentación y configuraciones regionales, vea [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).

Hay tres atributos de especificador de presentación en los que se puede registrar una extensión de hoja de propiedades. Son [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)y [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).

El atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifica las páginas de propiedades administrativas que se mostrarán en Active Directory complementos administrativos. La página de propiedades aparece cuando el usuario ve las propiedades de los objetos de la clase adecuada en una de las Active Directory complementos de MMC administrativos.

El atributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifica las páginas de propiedades del usuario final que se van a mostrar en el shell de Windows. La página de propiedades aparece cuando el usuario ve las propiedades de los objetos de la clase adecuada en el explorador de Windows. A partir de los sistemas operativos Windows Server 2003, el shell de Windows ya no muestra los objetos de Active Directory Domain Services.

[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) solo está disponible en los sistemas operativos Windows Server 2003. La página de propiedades aparece cuando el usuario ve las propiedades de más de un objeto de la clase adecuada en una de las Active Directory complementos administrativos de MMC.

Todos estos atributos tienen varios valores.

Los valores de los atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) y [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) requieren el formato siguiente.


```C++
<order number>,<clsid>,<optional data>
```



Los valores para el atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) requieren el formato siguiente.


```C++
<order number>,<clsid>
```



El " &lt; número de pedido &gt; " es un número sin signo que representa la posición de la página en la hoja. Cuando se muestra una hoja de propiedades, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; . Si hay más de un valor con el mismo " &lt; número de orden &gt; ", esos objetos com de la página de propiedades se cargan en el orden en que se leen desde el servidor de Active Directory. Si es posible, debe usar un " &lt; número de pedido" no existente &gt; ; es decir, uno no utilizado por otros valores de la propiedad. No hay ninguna posición de inicio prescrita y se permiten huecos en la &lt; secuencia "número de pedido &gt; ".

" &lt; CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

Los " &lt; datos opcionales &gt; " son valores de cadena que no son necesarios. Este valor se puede recuperar mediante el objeto COM de la página de propiedades mediante el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pasado a su método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) . El objeto COM de la página de propiedades obtiene estos datos llamando a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con el formato del portapapeles de [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) . Esto proporciona un **HGLOBAL** que contiene una estructura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) . la estructura **DSPROPERTYPAGEINFO** contiene una cadena Unicode que contiene los " &lt; datos &gt; opcionales". &lt; &gt; No se permite "datos opcionales" con el atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) . En el siguiente ejemplo de código de C/C++ se muestra cómo recuperar los " &lt; datos opcionales &gt; ".


```C++
fe.cfFormat = RegisterClipboardFormat(CFSTR_DSPROPERTYPAGEINFO);
fe.ptd = NULL;
fe.dwAspect = DVASPECT_CONTENT;
fe.lindex = -1;
fe.tymed = TYMED_HGLOBAL;
hr = pDataObj->GetData(&fe, &stm);
if(SUCCEEDED(hr))
{
    DSPROPERTYPAGEINFO *pPageInfo;
    
    pPageInfo = (DSPROPERTYPAGEINFO*)GlobalLock(stm.hGlobal);
    if(pPageInfo)
    {
        LPWSTR  pwszData;

        pwszData = (LPWSTR)((LPBYTE)pPageInfo + pPageInfo->offsetString);
        pwszData = NULL;
        
        GlobalUnlock(stm.hGlobal);
    }

    ReleaseStgMedium(&stm);
}
```



Una extensión de la hoja de propiedades puede implementar más de una página de propiedades. un uso posible de los " &lt; datos opcionales &gt; " es el nombre de las páginas que se van a mostrar. Esto proporciona la flexibilidad de elegir la implementación de varios objetos COM, uno para cada página o un solo objeto COM para administrar varias páginas.

El ejemplo de código siguiente es un valor de ejemplo que se puede usar para los atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)o [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> En el shell de Windows, los datos del especificador de presentación se recuperan en el inicio de sesión de usuario y se almacenan en caché para la sesión de usuario. En el caso de los complementos administrativos, los datos del especificador de presentación se recuperan cuando se carga el complemento y se almacenan en memoria caché mientras dure el proceso. En el caso del shell de Windows, esto indica que los cambios en los especificadores de presentación surten efecto después de que un usuario cierre la sesión y vuelva a iniciarla. En el caso de los complementos administrativos, los cambios surten efecto cuando se carga el archivo de consola o el complemento.

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a>Agregar un valor a los atributos de extensión de la hoja de propiedades

En el procedimiento siguiente se describe cómo registrar una extensión de la hoja de propiedades en uno de los atributos de extensión de la hoja de propiedades.

**Registrar una extensión de la hoja de propiedades en uno de los atributos de extensión de la hoja de propiedades**

1.  Asegúrese de que la extensión todavía no existe en los valores de atributo.
2.  Agregue el nuevo valor al final de la lista de ordenación de páginas de propiedades. Esto establece la parte " &lt; número &gt; de pedido" del valor del atributo en el valor siguiente después del número de pedido existente más alto.
3.  El método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) se utiliza para agregar el nuevo valor al atributo. El parámetro *lnControlCode* debe establecerse en **la \_ propiedad ADS \_ Append** para que el nuevo valor se anexe a los valores existentes y, por lo tanto, sobrescriba los valores existentes. Se debe llamar al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) después para confirmar el cambio en el directorio.

Tenga en cuenta que se puede registrar la misma extensión de hoja de propiedades para más de una clase de objeto.

El método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) se utiliza para agregar el nuevo valor al atributo. El parámetro *lnControlCode* debe establecerse en **la \_ propiedad ADS \_ Append** para que el nuevo valor se anexe a los valores existentes y, por lo tanto, sobrescriba los valores existentes. Se debe llamar al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) después de para confirmar el cambio en el directorio.

En el ejemplo de código siguiente se agrega una extensión de la hoja de propiedades a la clase Group de la configuración regional predeterminada del equipo. Tenga en cuenta que la función **AddPropertyPageToDisplaySpecifier** comprueba el CLSID de la extensión de la hoja de propiedades en los valores existentes, obtiene el número de orden más alto y agrega el valor de la página de propiedades mediante [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con la **propiedad de ADS \_ \_ anexar** código de control.


```C++
//  Add msvcrt.dll to the project.
//  Add activeds.lib to the project.
//  Add adsiid.lib to the project.

#include "stdafx.h"
#include <wchar.h>
#include <objbase.h>
#include <activeds.h>
#include "atlbase.h"

HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of the class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         );

HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                 );

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject);

//  Entry point for the application.
void wmain(int argc, wchar_t *argv[ ])
{

    wprintf(L"This program adds a sample property page to the display specifier for group class in the local computer's default locale.\n");

    // Initialize COM.
    CoInitialize(NULL);
    HRESULT hr = S_OK;

    //  Class ID for the sample property page.
    LPOLESTR szCLSID = L"{D9FCE809-8A10-11d2-A7E7-00C04F79DC0F}";
    LPOLESTR szClass = L"group";
    CLSID clsid;
    //  Convert to GUID.
    hr = CLSIDFromString(
        szCLSID,  //  Pointer to the string representation of the CLSID.
        &clsid    //  Pointer to the CLSID.
        );

    hr = AddPropertyPageToDisplaySpecifier(szClass, //  ldapDisplayName of the class.
                                           &clsid //  CLSID of property page COM object.
                                          );
    if (S_OK == hr)
        wprintf(L"Property page registered successfully\n");
    else if (S_FALSE == hr)
        wprintf(L"Property page was not added because it was already registered.\n");
    else
        wprintf(L"Property page was not added. HR: %x.\n");

    //  Uninitialize COM.
    CoUninitialize();
    return;
}

//  Adds a property page to Active Directory admin snap-ins.
HRESULT AddPropertyPageToDisplaySpecifier(LPOLESTR szClassName, //  ldapDisplayName of class.
                                          CLSID *pPropPageCLSID //  CLSID of property page COM object.
                                         )
{
    HRESULT hr = E_FAIL;
    IADsContainer *pContainer = NULL;
    LPOLESTR szDispSpec = new OLECHAR[MAX_PATH];
    IADs *pObject = NULL;
    VARIANT var;
    CComBSTR sbstrProperty = L"adminPropertyPages";
    LCID locale = NULL;
    //  Get the display specifier container using default system locale.
    //  When adding a property page COM object, specify the locale
    //  because the registration is locale-specific.
    //  This means if you created a property page
    //  for German, explicitly add it to the 407 container,
    //  so that it will be used when a computer is running with locale
    //  set to German and not the locale set on the
    //  computer where this application is running.
    hr = BindToDisplaySpecifiersContainerByLocale(&locale,
                                                  &pContainer
                                                 );
    //  Handle fail case where dispspec object
    //  is not found and give option to create one.

    if (SUCCEEDED(hr))
    {
        //  Bind to display specifier object for the specified class.
        //  Build the display specifier name.
#ifdef _MBCS
        wcscpy_s(szDispSpec, szClassName);
        wcscat_s(szDispSpec, L"-Display");
        hr = GetDisplaySpecifier(pContainer, szDispSpec, &pObject);
#endif _MBCS#endif _MBCS
        if (SUCCEEDED(hr))
        {
            //  Convert GUID to string.
            LPOLESTR szDSGUID = new WCHAR [39];
            ::StringFromGUID2(*pPropPageCLSID, szDSGUID, 39); 

            //  Get the adminPropertyPages property.
            hr = pObject->GetEx(sbstrProperty, &var);
            if (SUCCEEDED(hr))
            {
                LONG lstart, lend;
                SAFEARRAY *sa = V_ARRAY(&var);
                VARIANT varItem;
                //  Get the lower and upper bound.
                hr = SafeArrayGetLBound(sa, 1, &lstart);
                if (SUCCEEDED(hr))
                {
                    hr = SafeArrayGetUBound(sa, 1, &lend);
                }
                if (SUCCEEDED(hr))
                {
                    //  Iterate the values to verify if the prop page CLSID
                    //  is already registered.
                    VariantInit(&varItem);
                    BOOL bExists = FALSE;
                    UINT uiLastItem = 0;
                    UINT uiTemp = 0;
                    INT iOffset = 0;
                    LPOLESTR szMainStr = new OLECHAR[MAX_PATH];
                    LPOLESTR szItem = new OLECHAR[MAX_PATH];
                    LPOLESTR szStr = NULL;
                    for (long idx=lstart; idx <= lend; idx++)
                    {
                        hr = SafeArrayGetElement(sa, &idx, &varItem);
                        if (SUCCEEDED(hr))
                        {
#ifdef _MBCS
                            //  Verify that the specified CLSID is already registered.
                            wcscpy_s(szMainStr,varItem.bstrVal);
                            if (wcsstr(szMainStr,szDSGUID))
                                bExists = TRUE;
                            //  Get the index which is the number before the first comma.
                            szStr = wcschr(szMainStr, ',');
                            iOffset = (int)(szStr - szMainStr);
                            wcsncpy_s(szItem, szMainStr, iOffset);
                            szItem[iOffset]=0L;
                            uiTemp = _wtoi(szItem);
                            if (uiTemp > uiLastItem)
                                uiLastItem = uiTemp;
                            VariantClear(&varItem);
#endif _MBCS
                        }
                    }
                    //  If the CLSID is not registered, add it.
                    if (!bExists)
                    {
                        //  Build the value to add.
                        LPOLESTR szValue = new OLECHAR[MAX_PATH];
                        //  Next index to add at end of list.
#ifdef _MBCS
                        uiLastItem++;
                        _itow_s(uiLastItem, szValue, 10);   
                        wcscat_s(szValue,L",");
                        //  Add the class ID for the property page.
                        wcscat_s(szValue,szDSGUID);
                        wprintf(L"Value to add: %s\n", szValue);
#endif _MBCS

                        VARIANT varAdd;
                        //  Only one value to add
                        LPOLESTR pszAddStr[1];
                        pszAddStr[0]=szValue;
                        ADsBuildVarArrayStr(pszAddStr, 1, &varAdd);

                        hr = pObject->PutEx(ADS_PROPERTY_APPEND, sbstrProperty, varAdd);
                        if (SUCCEEDED(hr))
                        {
                            //  Commit the change.
                            hr = pObject->SetInfo();
                        }
                    }
                    else
                        hr = S_FALSE;
                }
            }
            VariantClear(&var);
        }
        if (pObject)
            pObject->Release();
    }

    return hr;
}

//  This function returns a pointer to the display specifier container 
//  for the specified locale.
//  If locale is NULL, use the default system locale and then return the locale in the locale param.
HRESULT BindToDisplaySpecifiersContainerByLocale(LCID *locale,
                                                 IADsContainer **ppDispSpecCont
                                                )
{
    HRESULT hr = E_FAIL;

    if ((!ppDispSpecCont)||(!locale))
        return E_POINTER;

    //  If no locale is specified, use the default system locale.
    if (!(*locale))
    {
        *locale = GetSystemDefaultLCID();
        if (!(*locale))
            return E_FAIL;
    }

    //  Verify that it is a valid locale.
    if (!IsValidLocale(*locale, LCID_SUPPORTED))
        return E_INVALIDARG;

    LPOLESTR szPath = new OLECHAR[MAX_PATH*2];
    IADs *pObj = NULL;
    VARIANT var;

    hr = ADsOpenObject(L"LDAP://rootDSE",
                       NULL,
                       NULL,
                       ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                       IID_IADs,
                       (void**)&pObj);

    if (SUCCEEDED(hr))
    {
        //  Get the DN to the config container.
        hr = pObj->Get(CComBSTR("configurationNamingContext"), &var);
        if (SUCCEEDED(hr))
        {
#ifdef _MBCS
            //  Build the string to bind to the DisplaySpecifiers container.
            swprintf_s(szPath,L"LDAP://cn=%x,cn=DisplaySpecifiers,%s", *locale, var.bstrVal);
            //  Bind to the DisplaySpecifiers container.
            *ppDispSpecCont = NULL;
            hr = ADsOpenObject(szPath,
                               NULL,
                               NULL,
                               ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                               IID_IADsContainer,
                               (void**)ppDispSpecCont);
#endif _MBCS

            if(FAILED(hr))
            {
                if (*ppDispSpecCont)
                {
                    (*ppDispSpecCont)->Release();
                    (*ppDispSpecCont) = NULL;
                }
            }
        }
    }
    //   Cleanup.
    VariantClear(&var);
    if (pObj)
        pObj->Release();

    return hr;
}

HRESULT GetDisplaySpecifier(IADsContainer *pContainer, LPOLESTR szDispSpec, IADs **ppObject)
{
    HRESULT hr = E_FAIL;
    CComBSTR sbstrDSPath;
    IDispatch *pDisp = NULL;

    if (!pContainer)
    {
        hr = E_POINTER;
        return hr;
    }

    //  Verify other pointers.
    //  Initialize the output pointer.
    (*ppObject) = NULL;

    //  Build relative path to the display specifier object.
    sbstrDSPath = "CN=";
    sbstrDSPath += szDispSpec;

    //  Use child object binding with IADsContainer::GetObject.
    hr = pContainer->GetObject(CComBSTR("displaySpecifier"),
        sbstrDSPath,
        &pDisp);
    if (SUCCEEDED(hr))
    {
        hr = pDisp->QueryInterface(IID_IADs, (void**)ppObject);
        if (FAILED(hr))
        {
            //  Clean up.
            if (*ppObject)
                (*ppObject)->Release();
        }
    }

    if (pDisp)
        pDisp->Release();

    return hr;

}
```



 

 