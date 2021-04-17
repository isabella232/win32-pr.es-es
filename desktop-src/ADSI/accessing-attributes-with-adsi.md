---
title: Obtener acceso a atributos con ADSI
description: Los métodos IADs. get y IADs. GetEx se usan para recuperar los valores de atributo con nombre.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Atributos, acceso con ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656398"
---
# <a name="accessing-attributes-with-adsi"></a>Obtener acceso a atributos con ADSI

Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) se usan para recuperar los valores de atributo con nombre. Ambos métodos devuelven un valor [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Estos métodos solo están disponibles para los directorios que admiten un esquema. Al tener acceso a objetos en un directorio sin un esquema, se deben usar las interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) y [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) para manipular los valores de atributo.

Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelven una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que puede ser, o no, una matriz de **variantes** en función del número de valores devueltos por el servidor. Por ejemplo, si solo se devuelve un valor del servidor, independientemente de si se trata de un atributo único o con varios valores, el método devuelve una sola **variante**. Por el contrario, si se devuelven varios valores, se devuelve una matriz **Variant** . Si se devuelve una matriz **Variant** , el miembro **VT** de la estructura **Variant** contiene las marcas de **\_ matriz/vbArray** de **VT \_ /vbVariant** y VT.

Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) también pueden devolver un objeto com mediante la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . En este caso, el miembro **VT** de la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene la marca de **distribución de VT \_ /vbObject** . Para tener acceso al objeto COM, llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IDispatch** para obtener la interfaz deseada.

Otro tipo de datos devuelto por los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) es datos binarios. En este caso, los datos se proporcionan como una matriz de bytes contigua y el miembro **VT** de la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contendrá las marcas de **\_ matriz/vbArray** de **VT \_ UI1/vbByte** y VT.

> [!Note]  
> Microsoft Visual Basic, Scripting Edition [**solo admite matrices Variant y**](/windows/win32/api/oaidl/ns-oaidl-variant) **Variant.** Por este motivo, no se puede usar VBScript para leer valores de propiedad binarios.

 

Muchas interfaces ADSI definen propiedades específicas de la interfaz. Por ejemplo, la interfaz [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define la propiedad [**Location**](iadscomputer-property-methods.md) . Estas propiedades definidas por la interfaz pueden contener datos idénticos a uno de los atributos con nombre, pero las propiedades son específicas del tipo de objeto al que hace referencia la interfaz. En los lenguajes que admiten la automatización, se puede tener acceso a estas propiedades definidas por la interfaz mediante la notación de puntos, tal y como se muestra en el ejemplo de código siguiente.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo obtener acceso a la propiedad ADsPath en la interfaz IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



En los lenguajes que no son de automatización, se deben usar los métodos de acceso de propiedad para tener acceso a las propiedades definidas por la interfaz. Por ejemplo, el método [**IADsComputer:: get \_ Location**](iadscomputer-property-methods.md) se usa para recuperar la propiedad **IADsComputer. Location** .

En el ejemplo de código de C++ siguiente se muestra cómo utilizar el método de acceso de propiedad en C++ para recuperar el ADsPath de un usuario.


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



Para obtener más información acerca de cómo obtener acceso a los atributos con ADSI, consulte:

-   [El método get](the-get-method.md)
-   [El método GetEx](the-getex-method.md)
-   [El método GetInfo](the-getinfo-method.md)
-   [Optimización mediante GetInfoEx](optimization-using-getinfoex.md)
-   [Acceso a atributos con la interfaz IDirectoryObject](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Código de ejemplo para leer atributos](example-code-for-reading-attributes.md)

 

 