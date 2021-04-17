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
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="c2278-104">Obtener acceso a atributos con ADSI</span><span class="sxs-lookup"><span data-stu-id="c2278-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="c2278-105">Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) se usan para recuperar los valores de atributo con nombre.</span><span class="sxs-lookup"><span data-stu-id="c2278-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="c2278-106">Ambos métodos devuelven un valor [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="c2278-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="c2278-107">Estos métodos solo están disponibles para los directorios que admiten un esquema.</span><span class="sxs-lookup"><span data-stu-id="c2278-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="c2278-108">Al tener acceso a objetos en un directorio sin un esquema, se deben usar las interfaces [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) y [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) para manipular los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="c2278-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="c2278-109">Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) devuelven una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) que puede ser, o no, una matriz de **variantes** en función del número de valores devueltos por el servidor.</span><span class="sxs-lookup"><span data-stu-id="c2278-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="c2278-110">Por ejemplo, si solo se devuelve un valor del servidor, independientemente de si se trata de un atributo único o con varios valores, el método devuelve una sola **variante**.</span><span class="sxs-lookup"><span data-stu-id="c2278-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="c2278-111">Por el contrario, si se devuelven varios valores, se devuelve una matriz **Variant** .</span><span class="sxs-lookup"><span data-stu-id="c2278-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="c2278-112">Si se devuelve una matriz **Variant** , el miembro **VT** de la estructura **Variant** contiene las marcas de **\_ matriz/vbArray** de **VT \_ /vbVariant** y VT.</span><span class="sxs-lookup"><span data-stu-id="c2278-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="c2278-113">Los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) también pueden devolver un objeto com mediante la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c2278-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c2278-114">En este caso, el miembro **VT** de la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contiene la marca de **distribución de VT \_ /vbObject** .</span><span class="sxs-lookup"><span data-stu-id="c2278-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="c2278-115">Para tener acceso al objeto COM, llame al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IDispatch** para obtener la interfaz deseada.</span><span class="sxs-lookup"><span data-stu-id="c2278-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="c2278-116">Otro tipo de datos devuelto por los métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) es datos binarios.</span><span class="sxs-lookup"><span data-stu-id="c2278-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="c2278-117">En este caso, los datos se proporcionan como una matriz de bytes contigua y el miembro **VT** de la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) contendrá las marcas de **\_ matriz/vbArray** de **VT \_ UI1/vbByte** y VT.</span><span class="sxs-lookup"><span data-stu-id="c2278-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="c2278-118">Microsoft Visual Basic, Scripting Edition [**solo admite matrices Variant y**](/windows/win32/api/oaidl/ns-oaidl-variant) **Variant.**</span><span class="sxs-lookup"><span data-stu-id="c2278-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="c2278-119">Por este motivo, no se puede usar VBScript para leer valores de propiedad binarios.</span><span class="sxs-lookup"><span data-stu-id="c2278-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="c2278-120">Muchas interfaces ADSI definen propiedades específicas de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c2278-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="c2278-121">Por ejemplo, la interfaz [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) define la propiedad [**Location**](iadscomputer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c2278-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="c2278-122">Estas propiedades definidas por la interfaz pueden contener datos idénticos a uno de los atributos con nombre, pero las propiedades son específicas del tipo de objeto al que hace referencia la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c2278-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="c2278-123">En los lenguajes que admiten la automatización, se puede tener acceso a estas propiedades definidas por la interfaz mediante la notación de puntos, tal y como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="c2278-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="c2278-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c2278-124">Examples</span></span>

<span data-ttu-id="c2278-125">En el ejemplo de código siguiente se muestra cómo obtener acceso a la propiedad ADsPath en la interfaz IADs.</span><span class="sxs-lookup"><span data-stu-id="c2278-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="c2278-126">En los lenguajes que no son de automatización, se deben usar los métodos de acceso de propiedad para tener acceso a las propiedades definidas por la interfaz.</span><span class="sxs-lookup"><span data-stu-id="c2278-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="c2278-127">Por ejemplo, el método [**IADsComputer:: get \_ Location**](iadscomputer-property-methods.md) se usa para recuperar la propiedad **IADsComputer. Location** .</span><span class="sxs-lookup"><span data-stu-id="c2278-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="c2278-128">En el ejemplo de código de C++ siguiente se muestra cómo utilizar el método de acceso de propiedad en C++ para recuperar el ADsPath de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c2278-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


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



<span data-ttu-id="c2278-129">Para obtener más información acerca de cómo obtener acceso a los atributos con ADSI, consulte:</span><span class="sxs-lookup"><span data-stu-id="c2278-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="c2278-130">El método get</span><span class="sxs-lookup"><span data-stu-id="c2278-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="c2278-131">El método GetEx</span><span class="sxs-lookup"><span data-stu-id="c2278-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="c2278-132">El método GetInfo</span><span class="sxs-lookup"><span data-stu-id="c2278-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="c2278-133">Optimización mediante GetInfoEx</span><span class="sxs-lookup"><span data-stu-id="c2278-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="c2278-134">Acceso a atributos con la interfaz IDirectoryObject</span><span class="sxs-lookup"><span data-stu-id="c2278-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="c2278-135">Código de ejemplo para leer atributos</span><span class="sxs-lookup"><span data-stu-id="c2278-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 