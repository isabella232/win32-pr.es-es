---
title: Acceso a atributos con ADSI
description: Los métodos IADs.Get e IADs.GetEx se usan para recuperar valores de atributo con nombre.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Atributos, acceso con ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024133"
---
# <a name="accessing-attributes-with-adsi"></a>Acceso a atributos con ADSI

Los [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) se usan para recuperar valores de atributo con nombre. Ambos métodos devuelven [**un valor VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) Estos métodos solo están disponibles para los directorios que admiten un esquema. Al obtener acceso a objetos de un directorio sin un esquema, las [**interfaces IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) deben usarse para manipular los valores de atributo.

Los [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelven una [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) que puede ser, o no, una matriz **VARIANT** en función del número de valores devueltos por el servidor. Por ejemplo, si solo se devuelve un valor del servidor, independientemente de si es un atributo único o con varios valores, el método devuelve una **única VARIANT**. Por el contrario, si se devuelven varios valores, se **devuelve una matriz VARIANT.** Si se **devuelve una matriz VARIANT,** el miembro **vt** de la estructura **VARIANT** contiene las marcas **\_ VT VARIANT/vbVariant** y **VT \_ ARRAY/vbArray.**

Los [**métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) también pueden devolver un objeto COM mediante la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) En este caso, el **miembro vt** de la [**estructura VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene la marca VT **\_ DISPATCH/vbObject.** Para acceder al objeto COM, llame al [**método QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la **interfaz IDispatch** para obtener la interfaz deseada.

Otro tipo de datos devuelto por [**los métodos IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) [**e IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) son datos binarios. En este caso, los datos se proporcionan como una matriz contigua de bytes y el miembro **vt** de la estructura [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) contendrá las marcas **VT \_ UI1/vbByte** y **VT \_ ARRAY/vbArray.**

> [!Note]  
> Microsoft Visual Basic, Scripting Edition solo admite [**matrices VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) y **VARIANT.** Debido a esto, VBScript no se puede usar para leer valores de propiedad binarios.

 

Muchas interfaces ADSI definen propiedades específicas de la interfaz. Por ejemplo, la [**interfaz IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define la [**propiedad Location.**](iadscomputer-property-methods.md) Estas propiedades definidas por la interfaz pueden contener datos idénticos a uno de los atributos con nombre, pero las propiedades son específicas del tipo de objeto al que hace referencia la interfaz. En los lenguajes que admiten la automatización, se puede acceder a estas propiedades definidas por la interfaz mediante la notación de puntos, como se muestra en el ejemplo de código siguiente.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo acceder a la propiedad ADsPath en la interfaz IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



En lenguajes que no son de automatización, los métodos de acceso de propiedad deben usarse para tener acceso a las propiedades definidas por la interfaz. Por ejemplo, el [**método IADsComputer::get \_ Location**](iadscomputer-property-methods.md) se usa para recuperar la **propiedad IADsComputer.Location.**

En el siguiente ejemplo de código de C++ se muestra cómo usar el método de acceso de propiedad en C++ para recuperar el ADsPath de un usuario.


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



Para obtener más información sobre el acceso a atributos con ADSI, consulte:

-   [El método Get](the-get-method.md)
-   [El método GetEx](the-getex-method.md)
-   [El método GetInfo](the-getinfo-method.md)
-   [Optimización mediante GetInfoEx](optimization-using-getinfoex.md)
-   [Acceso a atributos con la interfaz IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Código de ejemplo para leer atributos](example-code-for-reading-attributes.md)

 

 