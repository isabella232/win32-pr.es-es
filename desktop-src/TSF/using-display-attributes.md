---
title: Usar atributos para mostrar
description: Lea cómo usar los atributos para mostrar. Text Services Framework (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.
ms.assetid: b0f6e8e8-586a-4b51-a498-fb22bd36161f
keywords:
- Text Services Framework (TSF), mostrar atributos
- TSF (Text Services Framework), mostrar atributos
- Aplicaciones habilitadas para TSF, atributos para mostrar
- atributos de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3c576064ab22571b5a7822f5e6ff143add55d03
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406138"
---
# <a name="using-display-attributes"></a><span data-ttu-id="648ca-108">Usar atributos para mostrar</span><span class="sxs-lookup"><span data-stu-id="648ca-108">Using Display Attributes</span></span>

<span data-ttu-id="648ca-109">Text Services Framework (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto.</span><span class="sxs-lookup"><span data-stu-id="648ca-109">Text Services Framework (TSF) enables a text service to provide display attributes for text.</span></span> <span data-ttu-id="648ca-110">Esto permite que una aplicación muestre comentarios visuales adicionales.</span><span class="sxs-lookup"><span data-stu-id="648ca-110">This enables an application to display additional visual feedback.</span></span> <span data-ttu-id="648ca-111">Por ejemplo, un servicio de texto corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo.</span><span class="sxs-lookup"><span data-stu-id="648ca-111">For example, a spelling checker text service can highlight a misspelled word with a red underline.</span></span> <span data-ttu-id="648ca-112">Los atributos de presentación que se pueden proporcionar se definen mediante la estructura [ \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) de TF e incluyen el color de texto, el color de fondo del texto, el estilo de subrayado, el color de subrayado y el peso del subrayado.</span><span class="sxs-lookup"><span data-stu-id="648ca-112">The display attributes that can be provided are defined by the [TF\_DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) structure and include text color, text background color, underline style, underline color, and underline weight.</span></span>

<span data-ttu-id="648ca-113">Al representar texto, una aplicación debe obtener los atributos para mostrar del texto dibujado y usar los atributos para modificar cómo se dibuja el texto.</span><span class="sxs-lookup"><span data-stu-id="648ca-113">When rendering text, an application should obtain the display attributes for the text drawn and use the attributes to modify how the text is drawn.</span></span> <span data-ttu-id="648ca-114">Complete los pasos siguientes para obtener los atributos de visualización.</span><span class="sxs-lookup"><span data-stu-id="648ca-114">Complete the following steps to obtain display attributes.</span></span>

1.  <span data-ttu-id="648ca-115">Obtenga un objeto de propiedad para GUID \_ PROP ATTRIBUTE llamando a \_ [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span><span class="sxs-lookup"><span data-stu-id="648ca-115">Obtain a property object for GUID\_PROP\_ATTRIBUTE by calling [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).</span></span>
2.  <span data-ttu-id="648ca-116">Obtenga el valor de GUID PROP ATTRIBUTE para el intervalo especificado mediante una llamada \_ \_ a [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span><span class="sxs-lookup"><span data-stu-id="648ca-116">Obtain the value of the GUID\_PROP\_ATTRIBUTE for the specified range by calling [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue).</span></span> <span data-ttu-id="648ca-117">Esto proporciona un [valor TfGuidAtom.](tfguidatom.md)</span><span class="sxs-lookup"><span data-stu-id="648ca-117">This supplies a [TfGuidAtom](tfguidatom.md) value.</span></span>
3.  <span data-ttu-id="648ca-118">Convierta el [valor de TfGuidAtom](tfguidatom.md) en un GUID mediante una llamada a [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span><span class="sxs-lookup"><span data-stu-id="648ca-118">Convert the [TfGuidAtom](tfguidatom.md) value into a GUID by calling [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).</span></span>
4.  <span data-ttu-id="648ca-119">Cree un [objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para el atributo display llamando a [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="648ca-119">Create an [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) object for the display attribute by calling [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>
5.  <span data-ttu-id="648ca-120">Obtenga la información del atributo para mostrar llamando a [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span><span class="sxs-lookup"><span data-stu-id="648ca-120">Obtain the display attribute information by calling [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).</span></span>

<span data-ttu-id="648ca-121">En el ejemplo de código siguiente se muestra una función que obtiene los atributos de presentación de un contexto, un intervalo y una cookie de edición proporcionados.</span><span class="sxs-lookup"><span data-stu-id="648ca-121">The following code example demonstrates a function that obtains the display attributes from a supplied context, range, and edit cookie.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="648ca-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="648ca-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="648ca-123">TF \_ DISPLAYATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="648ca-123">TF\_DISPLAYATTRIBUTE</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[<span data-ttu-id="648ca-124">ITfContext::GetProperty</span><span class="sxs-lookup"><span data-stu-id="648ca-124">ITfContext::GetProperty</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[<span data-ttu-id="648ca-125">ITfReadOnlyProperty::GetValue</span><span class="sxs-lookup"><span data-stu-id="648ca-125">ITfReadOnlyProperty::GetValue</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[<span data-ttu-id="648ca-126">TfGuidAtom</span><span class="sxs-lookup"><span data-stu-id="648ca-126">TfGuidAtom</span></span>](tfguidatom.md)
</dt> <dt>

[<span data-ttu-id="648ca-127">ITfCategoryMgr::GetGUID</span><span class="sxs-lookup"><span data-stu-id="648ca-127">ITfCategoryMgr::GetGUID</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="648ca-128">ITfDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="648ca-128">ITfDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[<span data-ttu-id="648ca-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="648ca-129">ITfDisplayAttributeMgr::GetDisplayAttributeInfo</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 <span data-ttu-id="648ca-130">ITfDisplayAttributeInfo::GetAttributeInfo</span><span class="sxs-lookup"><span data-stu-id="648ca-130">ITfDisplayAttributeInfo::GetAttributeInfo</span></span> 
</dt> </dl>

 

 




