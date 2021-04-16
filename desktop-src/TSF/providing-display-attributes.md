---
title: Proporcionar atributos para mostrar
description: El marco de trabajo de servicios de texto (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Text Services Framework (TSF), Mostrar atributos
- TSF (marco de trabajo de servicios de texto), Mostrar atributos
- servicios de texto, atributos para mostrar
- atributos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f59bb64ef4f06df020a40189d273c703768d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685530"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="17897-107">Proporcionar atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="17897-107">Providing Display Attributes</span></span>

<span data-ttu-id="17897-108">El marco de trabajo de servicios de texto (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.</span><span class="sxs-lookup"><span data-stu-id="17897-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="17897-109">Esto permite proporcionar información visual adicional al usuario.</span><span class="sxs-lookup"><span data-stu-id="17897-109">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="17897-110">Por ejemplo, un servicio de texto de corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo.</span><span class="sxs-lookup"><span data-stu-id="17897-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="17897-111">Los atributos de visualización que se proporcionan se definen en la estructura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluyen el color de texto, el color de fondo del texto, el estilo de subrayado, el color de subrayado y el grosor</span><span class="sxs-lookup"><span data-stu-id="17897-111">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="17897-112">Los clientes que usan esta información de atributos de pantalla suelen ser aplicaciones, pero también pueden incluir servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="17897-112">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="17897-113">El administrador de TSF media entre el proveedor de atributos de presentación y el cliente de y realiza un seguimiento del proveedor de atributos de presentación de los atributos de presentación específicos.</span><span class="sxs-lookup"><span data-stu-id="17897-113">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="17897-114">Para proporcionar atributos para mostrar, un servicio de texto debe hacer lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="17897-114">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="17897-115">Registre el servicio de texto como un proveedor de atributos para mostrar llamando a [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con el identificador de clase del servicio de texto para el primer parámetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para el segundo parámetro y el identificador de clase del servicio de texto de nuevo para el tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="17897-115">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="17897-116">Implemente [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) y haga que esté disponible en el generador de clases.</span><span class="sxs-lookup"><span data-stu-id="17897-116">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="17897-117">Implemente [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) y haga que esté disponible en [ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="17897-117">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="17897-118">Implemente un objeto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para cada tipo de atributo de presentación que proporciona el servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="17897-118">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="17897-119">Aplicar los atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="17897-119">Applying the Display Attributes</span></span>

<span data-ttu-id="17897-120">El servicio de texto debe aplicar el atributo display a un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="17897-120">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="17897-121">Un servicio de texto solo puede modificar el valor de la propiedad durante una sesión de edición de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="17897-121">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="17897-122">Suponiendo que se encuentre en una sesión de edición de lectura/escritura, se aplicará un atributo de visualización de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="17897-122">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="17897-123">Obtenga un objeto [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) que abarque el texto al que se aplicará el atributo de visualización.</span><span class="sxs-lookup"><span data-stu-id="17897-123">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="17897-124">Obtenga un objeto [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) para los atributos de texto mediante una llamada a [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con el \_ atributo prop de GUID \_ .</span><span class="sxs-lookup"><span data-stu-id="17897-124">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="17897-125">Cree un [TfGuidAtom](tfguidatom.md) a partir del **GUID** del identificador de atributo de presentación definido por el servicio de texto mediante una llamada a [ITfCategoryMgr:: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="17897-125">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="17897-126">Inicialice una variable VARIANT en VT \_ I4 y establezca el miembro **lVal** en el **TfGuidAtom** creado en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="17897-126">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="17897-127">Aplique el atributo display al intervalo mediante una llamada a [ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con la cookie de edición de lectura/escritura, el intervalo y la variante inicializada en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="17897-127">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


```C++
STDAPI CEditSession::DoEditSession(TfEditCookie ec)
{
    HRESULT hr;
    ITfCategoryMgr *pCategoryMgr;
    TfGuidAtom  gaDisplayAttribute = TF_INVALID_GUIDATOM;

    //Create a TfGuidAtom for the display attribute identifier. 
    hr = CoCreateInstance(CLSID_TF_CategoryMgr,
                         NULL, 
                         CLSCTX_INPROC_SERVER, 
                         IID_ITfCategoryMgr, 
                         (void**)&pCategoryMgr);
    
    if(SUCCEEDED(hr))
    {
        hr = pCategoryMgr->RegisterGUID(guidDisplayAttribute, &gaDisplayAttribute);

        pCategoryMgr->Release();
    }
    
    //Apply the display attribute to the selected text. 
    if(TF_INVALID_GUIDATOM != gaDisplayAttribute)
    {
        TF_SELECTION tfSel;
        ULONG cFetched;

        //Get the selection. 
        hr = m_pContext->GetSelection(ec, TF_DEFAULT_SELECTION, 1, &tfSel, &cFetched);
        if(SUCCEEDED(hr) && cFetched)
        {
            ITfProperty *pDisplayAttributeProperty;

            //Get the display attribute property. 
            hr = m_pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pDisplayAttributeProperty);
            if(SUCCEEDED(hr))
            {
                VARIANT var;

                VariantInit(&var);

                //All display attributes are TfGuidAtoms and TfGuidAtoms are VT_I4. 
                var.vt = VT_I4; 
                var.lVal = gaDisplayAttribute;

                //Set the display attribute value over the range. 
                hr = pDisplayAttributeProperty->SetValue(ec, tfSel.range, &var);

                pDisplayAttributeProperty->Release();
            }

            tfSel.range->Release();
        }
    }

    return S_OK;
}
```



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="17897-128">Proporcionar el objeto de información de atributo para mostrar</span><span class="sxs-lookup"><span data-stu-id="17897-128">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="17897-129">Un cliente obtiene un objeto **ITfDisplayAttributeInfo** de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="17897-129">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="17897-130">El cliente llama a [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) con el identificador **GUID** del atributo display.</span><span class="sxs-lookup"><span data-stu-id="17897-130">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="17897-131">La primera vez que el cliente llama a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo**, el administrador de TSF creará una instancia del proveedor de atributos de visualización llamando a CoCreateInstance con el identificador de clase pasado como primer parámetro a **ITfCategoryMgr:: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="17897-131">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="17897-132">Las llamadas subsiguientes a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo** volverán a usar el objeto de proveedor de atributos de presentación.</span><span class="sxs-lookup"><span data-stu-id="17897-132">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="17897-133">Después, el administrador de TSF llama a [ITfDisplayAttributeProvider:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con el **GUID** del atributo de visualización para obtener el objeto **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="17897-133">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="17897-134">A continuación, el administrador de TSF vuelve a pasar el objeto **ITfDisplayAttributeInfo** al cliente.</span><span class="sxs-lookup"><span data-stu-id="17897-134">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="17897-135">El cliente llama a [ITfDisplayAttributeMgr:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos de presentación proporcionados por todos los proveedores de atributos de presentación.</span><span class="sxs-lookup"><span data-stu-id="17897-135">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="17897-136">El administrador de TSF enumera cada proveedor de atributos de visualización y crea una instancia de cada proveedor llamando a CoCreateInstance con el identificador de clase pasado como el tercer parámetro a **ITfCategoryMgr:: RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="17897-136">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="17897-137">Después, el administrador de TSF llama a **ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo** de cada proveedor para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos de presentación proporcionados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="17897-137">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="17897-138">A continuación, el administrador de TSF llama al método [IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del proveedor, agregando cada objeto **ITfDisplayAttributeInfo** obtenido al propio enumerador del administrador, hasta que se alcance el final de la enumeración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="17897-138">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="17897-139">Cuando todos los objetos **ITfDisplayAttributeInfo** de todos los proveedores de atributos de presentación se agregan al enumerador del administrador de TSF, el administrador devuelve el enumerador al cliente.</span><span class="sxs-lookup"><span data-stu-id="17897-139">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="17897-140">Después, el cliente llama a **IEnumTfDisplayAttributeInfo:: Next** una o más veces para obtener los objetos **ITfDisplayAttributeInfo** .</span><span class="sxs-lookup"><span data-stu-id="17897-140">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17897-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17897-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17897-142">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="17897-142">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="17897-143">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="17897-143">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="17897-144">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="17897-144">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="17897-145">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-145">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="17897-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-146">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="17897-147">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-147">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="17897-148">ITfRange</span><span class="sxs-lookup"><span data-stu-id="17897-148">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="17897-149">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="17897-149">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="17897-150">ITfContext:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="17897-150">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="17897-151">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="17897-151">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="17897-152">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="17897-152">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="17897-153">ITfProperty:: SetValue</span><span class="sxs-lookup"><span data-stu-id="17897-153">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="17897-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-154">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="17897-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-155">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="17897-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-156">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="17897-157">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-157">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="17897-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="17897-158">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="17897-159">IEnumTfDisplayAttributeInfo:: Next</span><span class="sxs-lookup"><span data-stu-id="17897-159">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




