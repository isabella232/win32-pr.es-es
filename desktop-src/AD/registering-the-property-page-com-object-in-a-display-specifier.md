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
# <a name="registering-the-property-page-com-object-in-a-display-specifier"></a><span data-ttu-id="c12ae-106">Registrar el objeto COM de la página de propiedades en un especificador de presentación</span><span class="sxs-lookup"><span data-stu-id="c12ae-106">Registering the Property Page COM Object in a Display Specifier</span></span>

<span data-ttu-id="c12ae-107">Cuando se usa COM para crear un archivo DLL de extensión de hoja de propiedades para Active Directory Domain Services, también se debe registrar la extensión con el registro de Windows y Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c12ae-107">When you use COM to create a property sheet extension DLL for Active Directory Domain Services, you must also register the extension with the Windows registry and Active Directory Domain Services.</span></span> <span data-ttu-id="c12ae-108">El registro de la extensión permite que el Active Directory complementos de MMC administrativos y el shell de Windows reconozcan la extensión.</span><span class="sxs-lookup"><span data-stu-id="c12ae-108">Registering the extension enables the Active Directory administrative MMC snap-ins and the Windows shell to recognize the extension.</span></span>

## <a name="registering-in-the-windows-registry"></a><span data-ttu-id="c12ae-109">Registro en el registro de Windows</span><span class="sxs-lookup"><span data-stu-id="c12ae-109">Registering in the Windows Registry</span></span>

<span data-ttu-id="c12ae-110">Al igual que todos los servidores COM, se debe registrar una extensión de la hoja de propiedades en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="c12ae-110">Like all COM servers, a property sheet extension must be registered in the Windows registry.</span></span> <span data-ttu-id="c12ae-111">La extensión se registra con la siguiente clave.</span><span class="sxs-lookup"><span data-stu-id="c12ae-111">The extension is registered under the following key.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

<span data-ttu-id="c12ae-112">*<clsid>* es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-112">*<clsid>* is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span> <span data-ttu-id="c12ae-113">En la *<clsid>* clave, hay una clave **InProcServer32** que identifica el objeto como servidor de 32 bits en proceso.</span><span class="sxs-lookup"><span data-stu-id="c12ae-113">Under the *<clsid>* key, there is an **InProcServer32** key that identifies the object as a 32-bit in-proc server.</span></span> <span data-ttu-id="c12ae-114">En la clave **InProcServer32** , la ubicación del archivo dll se especifica en el valor predeterminado y el modelo de subprocesos se especifica en el valor **ThreadingModel** .</span><span class="sxs-lookup"><span data-stu-id="c12ae-114">Under the **InProcServer32** key, the location of the DLL is specified in the default value and the threading model is specified in the **ThreadingModel** value.</span></span> <span data-ttu-id="c12ae-115">Todas las extensiones de la hoja de propiedades deben usar el modelo de subprocesos "Apartamento".</span><span class="sxs-lookup"><span data-stu-id="c12ae-115">All property sheet extensions must use the "Apartment" threading model.</span></span>

## <a name="registering-with-active-directory-domain-services"></a><span data-ttu-id="c12ae-116">Registro con Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="c12ae-116">Registering with Active Directory Domain Services</span></span>

<span data-ttu-id="c12ae-117">El registro de la extensión de la hoja de propiedades es específico de una configuración regional.</span><span class="sxs-lookup"><span data-stu-id="c12ae-117">Property sheet extension registration is specific to one locale.</span></span> <span data-ttu-id="c12ae-118">Si la extensión de la hoja de propiedades se aplica a todas las configuraciones regionales, debe registrarse en el objeto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) de la clase de objeto en todos los subcontenedores de la configuración regional en el contenedor de especificadores de presentación.</span><span class="sxs-lookup"><span data-stu-id="c12ae-118">If the property sheet extension applies to all locales, it must be registered in the object class [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) object in all of the locale subcontainers in the Display Specifiers container.</span></span> <span data-ttu-id="c12ae-119">Si la extensión de la hoja de propiedades está localizada para una configuración regional determinada, regístrela en el objeto **displaySpecifier** del subcontenedor de la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="c12ae-119">If the property sheet extension is localized for a certain locale, register it in the **displaySpecifier** object in that locale subcontainer.</span></span> <span data-ttu-id="c12ae-120">Para obtener más información sobre el contenedor de especificadores de presentación y configuraciones regionales, vea [especificadores de pantalla](display-specifiers.md) y [contenedor de DisplaySpecifiers](displayspecifiers-container.md).</span><span class="sxs-lookup"><span data-stu-id="c12ae-120">For more information about the Display Specifiers container and locales, see [Display Specifiers](display-specifiers.md) and [DisplaySpecifiers Container](displayspecifiers-container.md).</span></span>

<span data-ttu-id="c12ae-121">Hay tres atributos de especificador de presentación en los que se puede registrar una extensión de hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c12ae-121">There are three display specifier attributes that a property sheet extension can be registered under.</span></span> <span data-ttu-id="c12ae-122">Son [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)y [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span><span class="sxs-lookup"><span data-stu-id="c12ae-122">These are [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), and [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages).</span></span>

<span data-ttu-id="c12ae-123">El atributo [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) identifica las páginas de propiedades administrativas que se mostrarán en Active Directory complementos administrativos. La página de propiedades aparece cuando el usuario ve las propiedades de los objetos de la clase adecuada en una de las Active Directory complementos de MMC administrativos.</span><span class="sxs-lookup"><span data-stu-id="c12ae-123">The [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) attribute identifies administrative property pages to display in Active Directory administrative snap-ins. The property page appears when the user views properties for objects of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="c12ae-124">El atributo [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) identifica las páginas de propiedades del usuario final que se van a mostrar en el shell de Windows.</span><span class="sxs-lookup"><span data-stu-id="c12ae-124">The [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attribute identifies end-user property pages to display in the Windows shell.</span></span> <span data-ttu-id="c12ae-125">La página de propiedades aparece cuando el usuario ve las propiedades de los objetos de la clase adecuada en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="c12ae-125">The property page appears when the user views the properties for objects of the appropriate class in the Windows Explorer.</span></span> <span data-ttu-id="c12ae-126">A partir de los sistemas operativos Windows Server 2003, el shell de Windows ya no muestra los objetos de Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="c12ae-126">Beginning with the Windows Server 2003 operating systems, the Windows shell no longer displays objects from Active Directory Domain Services.</span></span>

<span data-ttu-id="c12ae-127">[**AdminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) solo está disponible en los sistemas operativos Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c12ae-127">The [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) is only available on the Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c12ae-128">La página de propiedades aparece cuando el usuario ve las propiedades de más de un objeto de la clase adecuada en una de las Active Directory complementos administrativos de MMC.</span><span class="sxs-lookup"><span data-stu-id="c12ae-128">The property page appears when the user views properties for more than one object of the appropriate class in one of the Active Directory administrative MMC snap-ins.</span></span>

<span data-ttu-id="c12ae-129">Todos estos atributos tienen varios valores.</span><span class="sxs-lookup"><span data-stu-id="c12ae-129">All of these attributes are multi-valued.</span></span>

<span data-ttu-id="c12ae-130">Los valores de los atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) y [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) requieren el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="c12ae-130">The values for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages) and [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages) attributes require the following format.</span></span>


```C++
<order number>,<clsid>,<optional data>
```



<span data-ttu-id="c12ae-131">Los valores para el atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) requieren el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="c12ae-131">The values for the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute require the following format.</span></span>


```C++
<order number>,<clsid>
```



<span data-ttu-id="c12ae-132">El " &lt; número de pedido &gt; " es un número sin signo que representa la posición de la página en la hoja.</span><span class="sxs-lookup"><span data-stu-id="c12ae-132">The "&lt;order number&gt;" is an unsigned number that represents the page position in the sheet.</span></span> <span data-ttu-id="c12ae-133">Cuando se muestra una hoja de propiedades, los valores se ordenan mediante una comparación de "número de &lt; pedido" de cada valor &gt; .</span><span class="sxs-lookup"><span data-stu-id="c12ae-133">When a property sheet is displayed, the values are sorted using a comparison of each value's "&lt;order number&gt;".</span></span> <span data-ttu-id="c12ae-134">Si hay más de un valor con el mismo " &lt; número de orden &gt; ", esos objetos com de la página de propiedades se cargan en el orden en que se leen desde el servidor de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c12ae-134">If more than one value has the same "&lt;order number&gt;", those property page COM objects are loaded in the order they are read from the Active Directory server.</span></span> <span data-ttu-id="c12ae-135">Si es posible, debe usar un " &lt; número de pedido" no existente &gt; ; es decir, uno no utilizado por otros valores de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c12ae-135">If possible, you should use a non-existing "&lt;order number&gt;"; that is, one not used by other values in the property.</span></span> <span data-ttu-id="c12ae-136">No hay ninguna posición de inicio prescrita y se permiten huecos en la &lt; secuencia "número de pedido &gt; ".</span><span class="sxs-lookup"><span data-stu-id="c12ae-136">There is no prescribed starting position, and gaps are allowed in the "&lt;order number&gt;" sequence.</span></span>

<span data-ttu-id="c12ae-137">" &lt; CLSID &gt; " es la representación de cadena del CLSID tal y como la produce la función [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-137">The "&lt;clsid&gt;" is the string representation of the CLSID as produced by the [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) function.</span></span>

<span data-ttu-id="c12ae-138">Los " &lt; datos opcionales &gt; " son valores de cadena que no son necesarios.</span><span class="sxs-lookup"><span data-stu-id="c12ae-138">The "&lt;optional data&gt;" is a string value that is not required.</span></span> <span data-ttu-id="c12ae-139">Este valor se puede recuperar mediante el objeto COM de la página de propiedades mediante el puntero [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pasado a su método [**IShellExtInit:: Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-139">This value can be retrieved by the property page COM object using the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) pointer passed to its [**IShellExtInit::Initialize**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize) method.</span></span> <span data-ttu-id="c12ae-140">El objeto COM de la página de propiedades obtiene estos datos llamando a [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) con el formato del portapapeles de [**CFSTR \_ DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-140">The property page COM object obtains this data by calling [**IDataObject::GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) with the [**CFSTR\_DSPROPERTYPAGEINFO**](cfstr-dspropertypageinfo.md) clipboard format.</span></span> <span data-ttu-id="c12ae-141">Esto proporciona un **HGLOBAL** que contiene una estructura [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) . la estructura **DSPROPERTYPAGEINFO** contiene una cadena Unicode que contiene los " &lt; datos &gt; opcionales".</span><span class="sxs-lookup"><span data-stu-id="c12ae-141">This provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure The **DSPROPERTYPAGEINFO** structure contains a Unicode string that contains the "&lt;optional data&gt;".</span></span> <span data-ttu-id="c12ae-142">&lt; &gt; No se permite "datos opcionales" con el atributo [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-142">The "&lt;optional data&gt;" is not allowed with the [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attribute.</span></span> <span data-ttu-id="c12ae-143">En el siguiente ejemplo de código de C/C++ se muestra cómo recuperar los " &lt; datos opcionales &gt; ".</span><span class="sxs-lookup"><span data-stu-id="c12ae-143">The following C/C++ code example shows how to retrieve the "&lt;optional data&gt;".</span></span>


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



<span data-ttu-id="c12ae-144">Una extensión de la hoja de propiedades puede implementar más de una página de propiedades. un uso posible de los " &lt; datos opcionales &gt; " es el nombre de las páginas que se van a mostrar.</span><span class="sxs-lookup"><span data-stu-id="c12ae-144">A property sheet extension can implement more than one property page; one possible use of the "&lt;optional data&gt;" is to name the pages to display.</span></span> <span data-ttu-id="c12ae-145">Esto proporciona la flexibilidad de elegir la implementación de varios objetos COM, uno para cada página o un solo objeto COM para administrar varias páginas.</span><span class="sxs-lookup"><span data-stu-id="c12ae-145">This provides the flexibility of choosing to implement multiple COM objects, one for each page, or a single COM object to handle multiple pages.</span></span>

<span data-ttu-id="c12ae-146">El ejemplo de código siguiente es un valor de ejemplo que se puede usar para los atributos [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages)o [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) .</span><span class="sxs-lookup"><span data-stu-id="c12ae-146">The following code example is an example value that can be used for the [**adminPropertyPages**](/windows/desktop/ADSchema/a-adminpropertypages), [**shellPropertyPages**](/windows/desktop/ADSchema/a-shellpropertypages), or [**adminMultiselectPropertyPages**](/windows/desktop/ADSchema/a-adminmultiselectpropertypages) attributes.</span></span>


```C++
1,{6dfe6485-a212-11d0-bcd5-00c04fd8d5b6}
```



> [!IMPORTANT]
> <span data-ttu-id="c12ae-147">En el shell de Windows, los datos del especificador de presentación se recuperan en el inicio de sesión de usuario y se almacenan en caché para la sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="c12ae-147">For the Windows shell, display specifier data is retrieved at user logon, and cached for the user session.</span></span> <span data-ttu-id="c12ae-148">En el caso de los complementos administrativos, los datos del especificador de presentación se recuperan cuando se carga el complemento y se almacenan en memoria caché mientras dure el proceso.</span><span class="sxs-lookup"><span data-stu-id="c12ae-148">For administrative snap-ins, the display specifier data is retrieved when the snap-in is loaded, and is cached for the lifetime of the process.</span></span> <span data-ttu-id="c12ae-149">En el caso del shell de Windows, esto indica que los cambios en los especificadores de presentación surten efecto después de que un usuario cierre la sesión y vuelva a iniciarla.</span><span class="sxs-lookup"><span data-stu-id="c12ae-149">For the Windows shell, this indicates that changes to display specifiers take effect after a user logs off and then logs on again.</span></span> <span data-ttu-id="c12ae-150">En el caso de los complementos administrativos, los cambios surten efecto cuando se carga el archivo de consola o el complemento.</span><span class="sxs-lookup"><span data-stu-id="c12ae-150">For the administrative snap-ins, changes take effect when the snap-in or console file is loaded.</span></span>

 

## <a name="adding-a-value-to-the-property-sheet-extension-attributes"></a><span data-ttu-id="c12ae-151">Agregar un valor a los atributos de extensión de la hoja de propiedades</span><span class="sxs-lookup"><span data-stu-id="c12ae-151">Adding a Value to the Property Sheet Extension Attributes</span></span>

<span data-ttu-id="c12ae-152">En el procedimiento siguiente se describe cómo registrar una extensión de la hoja de propiedades en uno de los atributos de extensión de la hoja de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c12ae-152">The following procedure describes how to register a property sheet extension under one of the property sheet extension attributes.</span></span>

<span data-ttu-id="c12ae-153">**Registrar una extensión de la hoja de propiedades en uno de los atributos de extensión de la hoja de propiedades**</span><span class="sxs-lookup"><span data-stu-id="c12ae-153">**Registering a property sheet extension under one of the property sheet extension attributes**</span></span>

1.  <span data-ttu-id="c12ae-154">Asegúrese de que la extensión todavía no existe en los valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="c12ae-154">Ensure that the extension does not already exist in the attribute values.</span></span>
2.  <span data-ttu-id="c12ae-155">Agregue el nuevo valor al final de la lista de ordenación de páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="c12ae-155">Add the new value at the end of the property page ordering list.</span></span> <span data-ttu-id="c12ae-156">Esto establece la parte " &lt; número &gt; de pedido" del valor del atributo en el valor siguiente después del número de pedido existente más alto.</span><span class="sxs-lookup"><span data-stu-id="c12ae-156">That is set the "&lt;order number&gt;" portion of the attribute value to the next value after the highest existing order number.</span></span>
3.  <span data-ttu-id="c12ae-157">El método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) se utiliza para agregar el nuevo valor al atributo.</span><span class="sxs-lookup"><span data-stu-id="c12ae-157">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="c12ae-158">El parámetro *lnControlCode* debe establecerse en **la \_ propiedad ADS \_ Append** para que el nuevo valor se anexe a los valores existentes y, por lo tanto, sobrescriba los valores existentes.</span><span class="sxs-lookup"><span data-stu-id="c12ae-158">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND** so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="c12ae-159">Se debe llamar al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) después para confirmar el cambio en el directorio.</span><span class="sxs-lookup"><span data-stu-id="c12ae-159">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called afterward to commit the change to the directory.</span></span>

<span data-ttu-id="c12ae-160">Tenga en cuenta que se puede registrar la misma extensión de hoja de propiedades para más de una clase de objeto.</span><span class="sxs-lookup"><span data-stu-id="c12ae-160">Be aware that the same property sheet extension can be registered for more than one object class.</span></span>

<span data-ttu-id="c12ae-161">El método [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) se utiliza para agregar el nuevo valor al atributo.</span><span class="sxs-lookup"><span data-stu-id="c12ae-161">The [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) method is used to add the new value to the attribute.</span></span> <span data-ttu-id="c12ae-162">El parámetro *lnControlCode* debe establecerse en **la \_ propiedad ADS \_ Append** para que el nuevo valor se anexe a los valores existentes y, por lo tanto, sobrescriba los valores existentes.</span><span class="sxs-lookup"><span data-stu-id="c12ae-162">The *lnControlCode* parameter must be set to **ADS\_PROPERTY\_APPEND**, so that the new value is appended to the existing values and does not, therefore, overwrite the existing values.</span></span> <span data-ttu-id="c12ae-163">Se debe llamar al método [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) después de para confirmar el cambio en el directorio.</span><span class="sxs-lookup"><span data-stu-id="c12ae-163">The [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) method must be called after to commit the change to the directory.</span></span>

<span data-ttu-id="c12ae-164">En el ejemplo de código siguiente se agrega una extensión de la hoja de propiedades a la clase Group de la configuración regional predeterminada del equipo.</span><span class="sxs-lookup"><span data-stu-id="c12ae-164">The following code example adds a property sheet extension to the group class in the computer's default locale.</span></span> <span data-ttu-id="c12ae-165">Tenga en cuenta que la función **AddPropertyPageToDisplaySpecifier** comprueba el CLSID de la extensión de la hoja de propiedades en los valores existentes, obtiene el número de orden más alto y agrega el valor de la página de propiedades mediante [**IADs::P Utex**](/windows/desktop/api/iads/nf-iads-iads-putex) con la **propiedad de ADS \_ \_ anexar** código de control.</span><span class="sxs-lookup"><span data-stu-id="c12ae-165">Be aware that the **AddPropertyPageToDisplaySpecifier** function verifies the property sheet extension CLSID in the existing values, gets the highest order number, and adds the value for the property page using [**IADs::PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) with the **ADS\_PROPERTY\_APPEND** control code.</span></span>


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



 

 