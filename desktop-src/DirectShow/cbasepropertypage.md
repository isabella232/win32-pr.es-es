---
description: La clase CBasePropertyPage es una clase abstracta para implementar una página de propiedades. Utilice esta clase si está escribiendo un filtro (u otro objeto) que admita páginas de propiedades.
ms.assetid: 80e77827-ed2f-426e-aa6f-c2aa90031751
title: Clase CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 168b2d450ec8efc30851286120d47ba6247fe6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671256"
---
# <a name="cbasepropertypage-class"></a><span data-ttu-id="ecbcf-104">Clase CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="ecbcf-104">CBasePropertyPage class</span></span>

![jerarquía de clases cbasepropertypage](images/cprop01.png)

<span data-ttu-id="ecbcf-106">La `CBasePropertyPage` clase es una clase abstracta para implementar una página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-106">The `CBasePropertyPage` class is an abstract class for implementing a property page.</span></span> <span data-ttu-id="ecbcf-107">Utilice esta clase si está escribiendo un filtro (u otro objeto) que admita páginas de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-107">Use this class if you are writing a filter (or other object) that supports property pages.</span></span>



| <span data-ttu-id="ecbcf-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="ecbcf-108">Protected Member Variables</span></span>                                             | <span data-ttu-id="ecbcf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbcf-109">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ecbcf-110">**m \_ bDirty**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-110">**m\_bDirty**</span></span>](cbasepropertypage-m-bdirty.md)                        | <span data-ttu-id="ecbcf-111">Indica si alguna de las propiedades ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-111">Indicates whether any of the properties have changed.</span></span>                                                                             |
| [<span data-ttu-id="ecbcf-112">**m \_ DialogId**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-112">**m\_DialogId**</span></span>](cbasepropertypage-m-dialogid.md)                    | <span data-ttu-id="ecbcf-113">Identificador de recurso del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-113">Resource identifier for the dialog.</span></span>                                                                                               |
| [<span data-ttu-id="ecbcf-114">**m \_ Dlg**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-114">**m\_Dlg**</span></span>](cbasepropertypage-m-dlg.md)                              | <span data-ttu-id="ecbcf-115">Identificador de la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-115">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="ecbcf-116">**m \_ hWnd**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-116">**m\_hwnd**</span></span>](cbasepropertypage-m-hwnd.md)                            | <span data-ttu-id="ecbcf-117">Identificador de la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-117">Handle to the dialog window.</span></span>                                                                                                      |
| [<span data-ttu-id="ecbcf-118">**m \_ pPageSite**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-118">**m\_pPageSite**</span></span>](cbasepropertypage-m-ppagesite.md)                  | <span data-ttu-id="ecbcf-119">Puntero a la interfaz **IPropertyPageSite** del sitio de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-119">Pointer to the **IPropertyPageSite** interface of the property page site.</span></span>                                                         |
| [<span data-ttu-id="ecbcf-120">**c \_ idcargo**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-120">**m\_TitleId**</span></span>](cbasepropertypage-m-titleid.md)                      | <span data-ttu-id="ecbcf-121">Identificador de recurso de una cadena que contiene el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-121">Resource identifier for a string that contains the dialog title.</span></span>                                                                  |
| <span data-ttu-id="ecbcf-122">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="ecbcf-122">Public Methods</span></span>                                                         | <span data-ttu-id="ecbcf-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbcf-123">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="ecbcf-124">**CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-124">**CBasePropertyPage**</span></span>](cbasepropertypage-cbasepropertypage.md)       | <span data-ttu-id="ecbcf-125">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-125">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="ecbcf-126">**~ CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-126">**~CBasePropertyPage**</span></span>](cbasepropertypage--cbasepropertypage.md)     | <span data-ttu-id="ecbcf-127">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-127">Destructor method.</span></span> <span data-ttu-id="ecbcf-128">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-128">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="ecbcf-129">**OnActivate**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-129">**OnActivate**</span></span>](cbasepropertypage-onactivate.md)                     | <span data-ttu-id="ecbcf-130">Se le llama cuando se activa la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-130">Called when the property page is activated.</span></span> <span data-ttu-id="ecbcf-131">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-131">Virtual.</span></span>                                                                              |
| [<span data-ttu-id="ecbcf-132">**OnApplyChanges**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-132">**OnApplyChanges**</span></span>](cbasepropertypage-onapplychanges.md)             | <span data-ttu-id="ecbcf-133">Se llama cuando el usuario aplica los cambios a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-133">Called when the user applies changes to the property page.</span></span> <span data-ttu-id="ecbcf-134">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-134">Virtual.</span></span>                                                               |
| [<span data-ttu-id="ecbcf-135">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-135">**OnConnect**</span></span>](cbasepropertypage-onconnect.md)                       | <span data-ttu-id="ecbcf-136">Proporciona un puntero **IUnknown** al objeto asociado a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-136">Provides an **IUnknown** pointer to the object associated with the property page.</span></span> <span data-ttu-id="ecbcf-137">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-137">Virtual.</span></span>                                        |
| [<span data-ttu-id="ecbcf-138">**Desactivar**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-138">**OnDeactivate**</span></span>](cbasepropertypage-ondeactivate.md)                 | <span data-ttu-id="ecbcf-139">Se llama cuando se destruye la ventana del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-139">Called when the dialog box window is destroyed.</span></span> <span data-ttu-id="ecbcf-140">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-140">Virtual.</span></span>                                                                          |
| [<span data-ttu-id="ecbcf-141">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-141">**OnDisconnect**</span></span>](cbasepropertypage-ondisconnect.md)                 | <span data-ttu-id="ecbcf-142">Se llama cuando la página de propiedades debe liberar el objeto asociado.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-142">Called when the property page should release the associated object.</span></span> <span data-ttu-id="ecbcf-143">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-143">Virtual.</span></span>                                                      |
| [<span data-ttu-id="ecbcf-144">**OnReceiveMessage**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-144">**OnReceiveMessage**</span></span>](cbasepropertypage-onreceivemessage.md)         | <span data-ttu-id="ecbcf-145">Se llama cuando el cuadro de diálogo recibe un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-145">Called when the dialog box receives a message.</span></span> <span data-ttu-id="ecbcf-146">Virtualiza.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-146">Virtual.</span></span>                                                                           |
| <span data-ttu-id="ecbcf-147">Métodos IPropertyPage</span><span class="sxs-lookup"><span data-stu-id="ecbcf-147">IPropertyPage Methods</span></span>                                                  | <span data-ttu-id="ecbcf-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="ecbcf-148">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="ecbcf-149">**Activar**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-149">**Activate**</span></span>](cbasepropertypage-activate.md)                         | <span data-ttu-id="ecbcf-150">Crea la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-150">Creates the dialog box window.</span></span>                                                                                                    |
| [<span data-ttu-id="ecbcf-151">**Aplicar**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-151">**Apply**</span></span>](cbasepropertypage-apply.md)                               | <span data-ttu-id="ecbcf-152">Aplica los valores de la página de propiedades actual al objeto asociado a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-152">Applies the current property page values to the object associated with the property page</span></span>                                          |
| [<span data-ttu-id="ecbcf-153">**Desactivación**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-153">**Deactivate**</span></span>](cbasepropertypage-deactivate.md)                     | <span data-ttu-id="ecbcf-154">Destruye la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-154">Destroys the dialog window.</span></span>                                                                                                       |
| [<span data-ttu-id="ecbcf-155">**GetPageInfo**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-155">**GetPageInfo**</span></span>](cbasepropertypage-getpageinfo.md)                   | <span data-ttu-id="ecbcf-156">Recupera información sobre la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-156">Retrieves information about the property page.</span></span>                                                                                    |
| [<span data-ttu-id="ecbcf-157">**Ayuda**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-157">**Help**</span></span>](cbasepropertypage-help.md)                                 | <span data-ttu-id="ecbcf-158">Invoca la ayuda de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-158">Invokes the property page help.</span></span>                                                                                                   |
| [<span data-ttu-id="ecbcf-159">**IsPageDirty**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-159">**IsPageDirty**</span></span>](cbasepropertypage-ispagedirty.md)                   | <span data-ttu-id="ecbcf-160">Indica si la página de propiedades ha cambiado desde que se activó o desde la llamada más reciente a **IPropertyPage:: Apply**.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-160">Indicates whether the property page has changed since it was activated or since the most recent call to **IPropertyPage::Apply**.</span></span> |
| [<span data-ttu-id="ecbcf-161">**Move**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-161">**Move**</span></span>](cbasepropertypage-move.md)                                 | <span data-ttu-id="ecbcf-162">Coloca y cambia el tamaño del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-162">Positions and resizes the dialog box.</span></span>                                                                                             |
| [<span data-ttu-id="ecbcf-163">**SetObjects**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-163">**SetObjects**</span></span>](cbasepropertypage-setobjects.md)                     | <span data-ttu-id="ecbcf-164">Proporciona punteros **IUnknown** para los objetos asociados a la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-164">Provides **IUnknown** pointers for the objects associated with the property page.</span></span>                                                 |
| [<span data-ttu-id="ecbcf-165">**SetPageSite**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-165">**SetPageSite**</span></span>](cbasepropertypage-setpagesite.md)                   | <span data-ttu-id="ecbcf-166">Inicializa la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-166">Initializes the property page.</span></span>                                                                                                    |
| [<span data-ttu-id="ecbcf-167">**Feria**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-167">**Show**</span></span>](cbasepropertypage-show.md)                                 | <span data-ttu-id="ecbcf-168">Muestra u oculta el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-168">Shows or hides the dialog box.</span></span>                                                                                                    |
| [<span data-ttu-id="ecbcf-169">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="ecbcf-169">**TranslateAccelerator**</span></span>](cbasepropertypage-translateaccelerator.md) | <span data-ttu-id="ecbcf-170">Indica a la página de propiedades que procese una pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-170">Instructs the property page to process a keystroke.</span></span>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ecbcf-171">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecbcf-171">Remarks</span></span>

<span data-ttu-id="ecbcf-172">Una página de propiedades es un objeto COM, por lo que debe generar un GUID para el identificador de clase (CLSID) y proporcionar una entrada en la matriz [**CFactoryTemplate**](cfactorytemplate.md) .</span><span class="sxs-lookup"><span data-stu-id="ecbcf-172">A property page is a COM object, so you must generate a GUID for the class identifier (CLSID) and provide an entry in the [**CFactoryTemplate**](cfactorytemplate.md) array.</span></span> <span data-ttu-id="ecbcf-173">Para obtener más información, vea [DirectShow y com](directshow-and-com.md).</span><span class="sxs-lookup"><span data-stu-id="ecbcf-173">For more information, see [DirectShow and COM](directshow-and-com.md).</span></span> <span data-ttu-id="ecbcf-174">En el ejemplo siguiente se muestra una entrada de generador de clases típica:</span><span class="sxs-lookup"><span data-stu-id="ecbcf-174">The following example shows a typical class factory entry:</span></span>


```
CFactoryTemplate g_Templates[] =
{   
    { 
        L"My Property Page",
        &CLSID_MyPropPage,
        CMyProp::CreateInstance,
        NULL,
        NULL
    },
    /* Also include the template for your filter (not shown). */
};

```



<span data-ttu-id="ecbcf-175">El filtro debe exponer la interfaz **ISpecifyPropertyPages** .</span><span class="sxs-lookup"><span data-stu-id="ecbcf-175">Your filter must expose the **ISpecifyPropertyPages** interface.</span></span> <span data-ttu-id="ecbcf-176">Esta interfaz contiene un método único, **GetPages**, que devuelve el CLSID de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-176">This interface contains a single method, **GetPages**, which returns the CLSID of the property page.</span></span> <span data-ttu-id="ecbcf-177">En el ejemplo siguiente se muestra cómo implementar este método:</span><span class="sxs-lookup"><span data-stu-id="ecbcf-177">The following example shows how to implement this method:</span></span>


```
STDMETHODIMP CMyFilter::GetPages(CAUUID *pPages)
{
    if (!pPages) return E_POINTER;

    pPages->cElems = 1;
    pPages->pElems = reinterpret_cast<GUID*>(CoTaskMemAlloc(sizeof(GUID)));
    if (pPages->pElems == NULL) 
    {
        return E_OUTOFMEMORY;
    }
    *(pPages->pElems) = CLSID_MyPropPage;
    return S_OK;
} 
```



<span data-ttu-id="ecbcf-178">No olvide reemplazar también el método **NonDelegatingQueryInterface** del filtro.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-178">Remember to override the filter's **NonDelegatingQueryInterface** method as well.</span></span> <span data-ttu-id="ecbcf-179">Para obtener más información, vea [DirectShow y com](directshow-and-com.md) y [**INonDelegatingUnknown**](inondelegatingunknown.md).</span><span class="sxs-lookup"><span data-stu-id="ecbcf-179">For more information, see [DirectShow and COM](directshow-and-com.md) and [**INonDelegatingUnknown**](inondelegatingunknown.md).</span></span>

<span data-ttu-id="ecbcf-180">A continuación, cree el cuadro de diálogo como un recurso en el proyecto y cree un recurso de cadena que contenga el título del cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-180">Next, create the dialog as a resource in your project, and create a string resource that holds the dialog title.</span></span> <span data-ttu-id="ecbcf-181">Ambos identificadores de recursos son parámetros para el constructor **CBasePropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="ecbcf-181">Both of these resource IDs are parameters to the **CBasePropertyPage** constructor.</span></span> <span data-ttu-id="ecbcf-182">Mantener la cadena de título en un recurso facilita la localización de la página de propiedades.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-182">Keeping the title string in a resource makes it easier to localize your property page.</span></span>

<span data-ttu-id="ecbcf-183">La clase **CBasePropertyPage** proporciona un marco para la interfaz **IPropertyPage** .</span><span class="sxs-lookup"><span data-stu-id="ecbcf-183">The **CBasePropertyPage** class provides a framework for the **IPropertyPage** interface.</span></span> <span data-ttu-id="ecbcf-184">Este marco de trabajo llama a una serie de métodos virtuales, entre los que se incluyen [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md), etc.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-184">This framework calls a number of virtual methods, including [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md), [**CBasePropertyPage::OnApplyChanges**](cbasepropertypage-onapplychanges.md), and so on.</span></span> <span data-ttu-id="ecbcf-185">En la clase base, estos métodos simplemente devuelven los valores \_ correctos.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-185">In the base class, these methods simply return S\_OK.</span></span> <span data-ttu-id="ecbcf-186">La clase derivada deberá invalidar algunos o todos estos métodos virtuales.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-186">Your derived class will need to override some or all of these virtual methods.</span></span> <span data-ttu-id="ecbcf-187">Para obtener más información, vea los comentarios de los métodos individuales.</span><span class="sxs-lookup"><span data-stu-id="ecbcf-187">For details, see the remarks for the individual methods.</span></span>

<span data-ttu-id="ecbcf-188">Para obtener un ejemplo de cómo usar esta clase para crear una página de propiedades, vea [crear una página de propiedades de filtro](creating-a-filter-property-page.md).</span><span class="sxs-lookup"><span data-stu-id="ecbcf-188">For an extended example of how to use this class to create a property page, see [Creating a Filter Property Page](creating-a-filter-property-page.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecbcf-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecbcf-189">Requirements</span></span>



| <span data-ttu-id="ecbcf-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecbcf-190">Requirement</span></span> | <span data-ttu-id="ecbcf-191">Value</span><span class="sxs-lookup"><span data-stu-id="ecbcf-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecbcf-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecbcf-192">Header</span></span><br/>  | <dl> <span data-ttu-id="ecbcf-193"><dt>Cprop. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ecbcf-193"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ecbcf-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ecbcf-194">Library</span></span><br/> | <dl> <span data-ttu-id="ecbcf-195"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ecbcf-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




