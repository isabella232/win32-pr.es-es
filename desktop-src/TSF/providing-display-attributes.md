---
title: Proporcionar atributos para mostrar
description: Obtenga información sobre cómo proporcionar atributos para mostrar. Text Services Framework (TSF) permite que un servicio de texto proporcione atributos para mostrar para el texto.
ms.assetid: 5809f5b8-0396-4abd-b5fe-61ecc8cd0914
keywords:
- Text Services Framework (TSF), mostrar atributos
- TSF (Text Services Framework), mostrar atributos
- servicios de texto, mostrar atributos
- atributos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780cc191e39d5b1d0c3329bab87af5267e4a6c73
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406118"
---
# <a name="providing-display-attributes"></a><span data-ttu-id="33c57-108">Proporcionar atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="33c57-108">Providing Display Attributes</span></span>

<span data-ttu-id="33c57-109">Text Services Framework (TSF) permite que un servicio de texto proporcione atributos para mostrar para el texto.</span><span class="sxs-lookup"><span data-stu-id="33c57-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="33c57-110">Esto permite proporcionar comentarios visuales adicionales al usuario.</span><span class="sxs-lookup"><span data-stu-id="33c57-110">This enables additional visual feedback to be supplied to the user.</span></span> <span data-ttu-id="33c57-111">Por ejemplo, un servicio de texto de corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo.</span><span class="sxs-lookup"><span data-stu-id="33c57-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="33c57-112">Los atributos de presentación proporcionados se definen mediante la estructura [ \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) de TF e incluyen color de texto, color de fondo de texto, estilo de subrayado, color de subrayado y peso del subrayado.</span><span class="sxs-lookup"><span data-stu-id="33c57-112">The display attributes provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="33c57-113">Los clientes que usan esta información de atributo para mostrar suelen ser aplicaciones, pero también pueden incluir servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="33c57-113">Clients that use this display attribute information will most often be applications, but can also include text services.</span></span> <span data-ttu-id="33c57-114">El administrador de TSF media entre el proveedor de atributos para mostrar y el cliente y realiza un seguimiento del proveedor de atributos para mostrar de los atributos de presentación específicos.</span><span class="sxs-lookup"><span data-stu-id="33c57-114">The TSF manager mediates between the display attribute provider and the client and tracks the display attribute provider of the specific display attributes.</span></span>

<span data-ttu-id="33c57-115">Para proporcionar atributos para mostrar, un servicio de texto debe hacer lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="33c57-115">To provide display attributes, a text service must do the following.</span></span>

1.  <span data-ttu-id="33c57-116">Registre el servicio de texto como proveedor de atributos para mostrar llamando a [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con el identificador de clase del servicio de texto para el primer parámetro, GUID \_ TFCAT DISPLAYATTRIBUTEPROVIDER para el segundo parámetro y el identificador de clase del servicio de texto de nuevo para el \_ tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="33c57-116">Register the text service as a display attribute provider by calling [ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) with the class identifier of the text service for the first parameter, GUID\_TFCAT\_DISPLAYATTRIBUTEPROVIDER for the second parameter and the class identifier of the text service again for the third parameter.</span></span>
2.  <span data-ttu-id="33c57-117">Implemente [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) y haga que esté disponible desde el generador de clases.</span><span class="sxs-lookup"><span data-stu-id="33c57-117">Implement [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) and make it available from the class factory.</span></span>
3.  <span data-ttu-id="33c57-118">Implemente [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) y haga que esté disponible desde [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="33c57-118">Implement [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) and make it available from [ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).</span></span>
4.  <span data-ttu-id="33c57-119">Implemente [un objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para cada tipo de atributo de presentación que proporciona el servicio de texto.</span><span class="sxs-lookup"><span data-stu-id="33c57-119">Implement an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for each type of display attribute that the text service provides.</span></span>

## <a name="applying-the-display-attributes"></a><span data-ttu-id="33c57-120">Aplicación de los atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="33c57-120">Applying the Display Attributes</span></span>

<span data-ttu-id="33c57-121">El servicio de texto debe aplicar el atributo de presentación a un intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="33c57-121">The text service must apply the display attribute to a range of text.</span></span> <span data-ttu-id="33c57-122">Un servicio de texto solo puede modificar el valor de propiedad durante una sesión de edición de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="33c57-122">A text service can only modify the property value during a read/write edit session.</span></span>

<span data-ttu-id="33c57-123">Suponiendo que esto se encuentra dentro de una sesión de edición de lectura y escritura, se aplica un atributo para mostrar de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="33c57-123">Assuming this is within a read/write edit session, a display attribute is applied in the following manner.</span></span>

1.  <span data-ttu-id="33c57-124">Obtenga un [objeto ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) que cubre el texto al que se aplicará el atributo para mostrar.</span><span class="sxs-lookup"><span data-stu-id="33c57-124">Obtain an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) object that covers the text that the display attribute will be applied to.</span></span>
2.  <span data-ttu-id="33c57-125">Obtenga un [objeto ITfProperty para](/windows/desktop/api/Msctf/nn-msctf-itfproperty) los atributos de texto mediante una llamada [a ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con GUID \_ PROP \_ ATTRIBUTE.</span><span class="sxs-lookup"><span data-stu-id="33c57-125">Obtain an [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) object for the text attributes by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) with GUID\_PROP\_ATTRIBUTE.</span></span>
3.  <span data-ttu-id="33c57-126">Cree un [TfGuidAtom a partir](tfguidatom.md) del **GUID** del atributo para mostrar definido por el servicio de texto llamando a [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="33c57-126">Create a [TfGuidAtom](tfguidatom.md) from the text service-defined display attribute identifier **GUID** by calling [ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>
4.  <span data-ttu-id="33c57-127">Inicialice una variable VARIANT en VT I4 y establezca el miembro lVal en el \_ **tfguidAtom** creado en el paso anterior. </span><span class="sxs-lookup"><span data-stu-id="33c57-127">Initialize a VARIANT variable to VT\_I4 and set the **lVal** member to the **TfGuidAtom** created in the previous step.</span></span>
5.  <span data-ttu-id="33c57-128">Aplique el atributo display al intervalo mediante una llamada a [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con la cookie de edición de lectura/escritura, el intervalo y variant inicializados en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="33c57-128">Apply the display attribute to the range by calling [ITfProperty::SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) with the read/write edit cookie, the range and the VARIANT initialized in the previous step.</span></span>


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



## <a name="supplying-the-display-attribute-information-object"></a><span data-ttu-id="33c57-129">Proporcionar el objeto display attribute information</span><span class="sxs-lookup"><span data-stu-id="33c57-129">Supplying the Display Attribute Information Object</span></span>

<span data-ttu-id="33c57-130">Un cliente obtiene un **objeto ITfDisplayAttributeInfo** de una de estas dos maneras.</span><span class="sxs-lookup"><span data-stu-id="33c57-130">A client obtains an **ITfDisplayAttributeInfo** object in one of two ways.</span></span>

1.  <span data-ttu-id="33c57-131">El cliente llama [a ITfDisplayAttributeMgr::GetDisplayAttributeInfo con](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) el **identificador GUID** del atributo para mostrar.</span><span class="sxs-lookup"><span data-stu-id="33c57-131">The client calls [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) with the **GUID** identifier of the display attribute.</span></span> <span data-ttu-id="33c57-132">La primera vez que el cliente llama a **ITfDisplayAttributeMgr::GetDisplayAttributeInfo,** el administrador de TSF creará una instancia del proveedor de atributos para mostrar llamando a CoCreateInstance con el identificador de clase pasado como primer parámetro a **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="33c57-132">The first time the client calls **ITfDisplayAttributeMgr::GetDisplayAttributeInfo**, the TSF manager will create an instance of the display attribute provider by calling CoCreateInstance with the class identifier passed as the first parameter to **ITfCategoryMgr::RegisterCategory**.</span></span> <span data-ttu-id="33c57-133">Las llamadas posteriores **a ITfDisplayAttributeMgr::GetDisplayAttributeInfo** reutilizarán el objeto del proveedor de atributos para mostrar.</span><span class="sxs-lookup"><span data-stu-id="33c57-133">Subsequent calls to **ITfDisplayAttributeMgr::GetDisplayAttributeInfo** will reuse the display attribute provider object.</span></span>

    <span data-ttu-id="33c57-134">A continuación, el administrador de TSF llama a [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con el **GUID** del atributo para mostrar para obtener el **objeto ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="33c57-134">The TSF manager then calls [ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) with the display attribute **GUID** to obtain the **ITfDisplayAttributeInfo** object.</span></span>

    <span data-ttu-id="33c57-135">A continuación, el administrador de TSF devuelve el **objeto ITfDisplayAttributeInfo** al cliente.</span><span class="sxs-lookup"><span data-stu-id="33c57-135">The TSF manager then passes the **ITfDisplayAttributeInfo** object back to the client.</span></span>

2.  <span data-ttu-id="33c57-136">El cliente llama a [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos para mostrar proporcionados por todos los proveedores de atributos para mostrar.</span><span class="sxs-lookup"><span data-stu-id="33c57-136">The client calls [ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by all of the display attribute providers.</span></span> <span data-ttu-id="33c57-137">El administrador de TSF enumera cada proveedor de atributos para mostrar y crea una instancia de cada proveedor mediante una llamada a CoCreateInstance con el identificador de clase pasado como tercer parámetro a **ITfCategoryMgr::RegisterCategory**.</span><span class="sxs-lookup"><span data-stu-id="33c57-137">The TSF manager enumerates each display attribute provider and creates an instance of each provider by calling CoCreateInstance with the class identifier passed as the third parameter to **ITfCategoryMgr::RegisterCategory**.</span></span>

    <span data-ttu-id="33c57-138">A continuación, el administrador de TSF llama a **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** de cada proveedor para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos para mostrar proporcionados por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="33c57-138">The TSF manager then calls each provider's **ITfDisplayAttributeProvider::EnumDisplayAttributeInfo** to obtain an **IEnumTfDisplayAttributeInfo** object that contains all of the display attributes provided by the provider.</span></span>

    <span data-ttu-id="33c57-139">A continuación, el administrador de TSF llama al método [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del proveedor y agrega cada objeto **ITfDisplayAttributeInfo** obtenido al enumerador propio del administrador, hasta que se alcanza el final de la enumeración del proveedor.</span><span class="sxs-lookup"><span data-stu-id="33c57-139">The TSF manager then calls the provider's [IEnumTfDisplayAttributeInfo::Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) method, adding each **ITfDisplayAttributeInfo** object obtained to the manager's own enumerator, until the end of the provider's enumeration is reached.</span></span>

    <span data-ttu-id="33c57-140">Cuando todos los objetos **ITfDisplayAttributeInfo** de todos los proveedores de atributos para mostrar se agregan al enumerador del administrador de TSF, el administrador devuelve su enumerador al cliente.</span><span class="sxs-lookup"><span data-stu-id="33c57-140">When all of the **ITfDisplayAttributeInfo** objects for all of the display attribute providers are added to the TSF manager's enumerator, the manager returns its enumerator to the client.</span></span> <span data-ttu-id="33c57-141">A continuación, el cliente llama a **IEnumTfDisplayAttributeInfo::Next** una o varias veces para obtener los **objetos ITfDisplayAttributeInfo.**</span><span class="sxs-lookup"><span data-stu-id="33c57-141">The client then calls **IEnumTfDisplayAttributeInfo::Next** one or more times to obtain the **ITfDisplayAttributeInfo** objects.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33c57-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="33c57-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33c57-143">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="33c57-143">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="33c57-144">ITfCategoryMgr::RegisterCategory</span><span class="sxs-lookup"><span data-stu-id="33c57-144">ITfCategoryMgr::RegisterCategory</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[<span data-ttu-id="33c57-145">ITfDisplayAttributeProvider</span><span class="sxs-lookup"><span data-stu-id="33c57-145">ITfDisplayAttributeProvider</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[<span data-ttu-id="33c57-146">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-146">IEnumTfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="33c57-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-147">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="33c57-148">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-148">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="33c57-149">ITfRange</span><span class="sxs-lookup"><span data-stu-id="33c57-149">ITfRange</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[<span data-ttu-id="33c57-150">ITfProperty</span><span class="sxs-lookup"><span data-stu-id="33c57-150">ITfProperty</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[<span data-ttu-id="33c57-151">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="33c57-151">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="33c57-152">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="33c57-152">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="33c57-153">ITfCategoryMgr::RegisterGUID</span><span class="sxs-lookup"><span data-stu-id="33c57-153">ITfCategoryMgr::RegisterGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[<span data-ttu-id="33c57-154">ITfProperty::SetValue</span><span class="sxs-lookup"><span data-stu-id="33c57-154">ITfProperty::SetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[<span data-ttu-id="33c57-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-155">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="33c57-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-156">ITfDisplayAttributeProvider::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="33c57-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-157">ITfDisplayAttributeMgr::EnumDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="33c57-158">IEnumTfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-158">IEnumTfDisplayAttributeInfo</span></span> 
</dt> <dt>

 <span data-ttu-id="33c57-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="33c57-159">ITfDisplayAttributeProvider::EnumDisplayAttributeInfo</span></span> 
</dt> <dt>

[<span data-ttu-id="33c57-160">IEnumTfDisplayAttributeInfo::Next</span><span class="sxs-lookup"><span data-stu-id="33c57-160">IEnumTfDisplayAttributeInfo::Next</span></span>](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




