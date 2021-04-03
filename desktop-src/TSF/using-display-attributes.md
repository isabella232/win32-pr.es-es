---
title: Usar atributos para mostrar
description: El marco de trabajo de servicios de texto (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Text Services Framework (TSF), Mostrar atributos
- TSF (marco de trabajo de servicios de texto), Mostrar atributos
- Aplicaciones habilitadas para TSF, atributos para mostrar
- atributos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc725f67fab904db23f6232ac5efb5d63c62c26
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773879"
---
# <a name="using-display-attributes"></a><span data-ttu-id="805f1-107">Usar atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="805f1-107">Using Display Attributes</span></span>

<span data-ttu-id="805f1-108">El marco de trabajo de servicios de texto (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.</span><span class="sxs-lookup"><span data-stu-id="805f1-108">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="805f1-109">Esto permite que una aplicación muestre comentarios visuales adicionales.</span><span class="sxs-lookup"><span data-stu-id="805f1-109">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="805f1-110">Por ejemplo, un servicio de texto de corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo.</span><span class="sxs-lookup"><span data-stu-id="805f1-110">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="805f1-111">Los atributos de visualización que se pueden proporcionar se definen mediante la estructura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluyen el color de texto, el color de fondo del texto, el estilo de subrayado, el color de subrayado y el grosor del subrayado.</span><span class="sxs-lookup"><span data-stu-id="805f1-111">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="805f1-112">Al representar texto, una aplicación debe obtener los atributos de presentación del texto dibujado y usar los atributos para modificar el modo en que se dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="805f1-112">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="805f1-113">Complete los pasos siguientes para obtener los atributos de visualización.</span><span class="sxs-lookup"><span data-stu-id="805f1-113">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="805f1-114">Obtenga un objeto de propiedad para el atributo prop de GUID llamando \_ \_ a [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span><span class="sxs-lookup"><span data-stu-id="805f1-114">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="805f1-115">Obtenga el valor del \_ atributo prop GUID \_ para el intervalo especificado mediante una llamada a [ITfReadOnlyProperty:: GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="805f1-115">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="805f1-116">Esto proporciona un valor de [TfGuidAtom](tfguidatom.md) .</span><span class="sxs-lookup"><span data-stu-id="805f1-116">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="805f1-117">Convierta el valor de [TfGuidAtom](tfguidatom.md) en un GUID llamando a [ITfCategoryMgr:: GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="805f1-117">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="805f1-118">Cree un objeto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para el atributo de visualización llamando a [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="805f1-118">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="805f1-119">Obtenga la información del atributo de visualización llamando a [ITfDisplayAttributeInfo:: GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="805f1-119">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="805f1-120">En el ejemplo de código siguiente se muestra una función que obtiene los atributos de presentación de un contexto, un intervalo y una cookie de edición proporcionados.</span><span class="sxs-lookup"><span data-stu-id="805f1-120">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


```C++
HRESULT GetDispAttrFromRange(   ITfContext *pContext, 
                                ITfRange *pRange, 
                                TfEditCookie ec, 
                                TF_DISPLAYATTRIBUTE *pDispAttr)
{
    HRESULT     hr;
    
    //Create the category manager. 
    ITfCategoryMgr  *pCategoryMgr;
    hr = CoCreateInstance(  CLSID_TF_CategoryMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfCategoryMgr, 
                            (LPVOID*)&pCategoryMgr);
    if(FAILED(hr))
    {
        return hr;
    }

    //Create the display attribute manager. 
    ITfDisplayAttributeMgr  *pDispMgr;
    hr = CoCreateInstance(  CLSID_TF_DisplayAttributeMgr,
                            NULL, 
                            CLSCTX_INPROC_SERVER, 
                            IID_ITfDisplayAttributeMgr, 
                            (LPVOID*)&pDispMgr);
    if(FAILED(hr))
    {
        pCategoryMgr->Release();
        return hr;
    }
    
    //Get the display attribute property. 
    ITfProperty *pProp;
    hr = pContext->GetProperty(GUID_PROP_ATTRIBUTE, &pProp);
    if(SUCCEEDED(hr))
    {
        VARIANT var;

        VariantInit(&var);
        hr = pProp->GetValue(ec, pRange, &var);
        if(S_OK == hr)  //Returns S_FALSE if the range is not completely covered by the property.  
        {
            if(VT_I4 == var.vt)
            {
                //The property is a guidatom. 
                GUID    guid;

                //Convert the guidatom into a GUID. 
                hr = pCategoryMgr->GetGUID((TfGuidAtom)var.lVal, &guid);
                if(SUCCEEDED(hr))
                {
                    ITfDisplayAttributeInfo *pDispInfo;

                    //Get the display attribute info object for this attribute. 
                    hr = pDispMgr->GetDisplayAttributeInfo(guid, &pDispInfo, NULL);
                    if(SUCCEEDED(hr))
                    {
                        //Get the display attribute info. 
                        hr = pDispInfo->GetAttributeInfo(pDispAttr);

                        pDispInfo->Release();
                    }
                }
            }
            else
            {
                //An error occurred; GUID_PROP_ATTRIBUTE must always be VT_I4. 
                hr = E_FAIL;
            }
            VariantClear(&var);
        }
    pProp->Release();
    }

    pCategoryMgr->Release();
    pDispMgr->Release();

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="805f1-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="805f1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="805f1-122">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="805f1-122">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="805f1-123">ITfContext:: GetProperty</span><span class="sxs-lookup"><span data-stu-id="805f1-123">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="805f1-124">ITfReadOnlyProperty:: GetValue</span><span class="sxs-lookup"><span data-stu-id="805f1-124">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="805f1-125">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="805f1-125">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="805f1-126">ITfCategoryMgr:: GetGUID</span><span class="sxs-lookup"><span data-stu-id="805f1-126">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="805f1-127">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="805f1-127">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="805f1-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="805f1-128">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="805f1-129">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="805f1-129">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




