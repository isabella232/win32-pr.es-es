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
# <a name="using-display-attributes"></a>Usar atributos para mostrar

Text Services Framework (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto. Esto permite que una aplicación muestre comentarios visuales adicionales. Por ejemplo, un servicio de texto corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo. Los atributos de presentación que se pueden proporcionar se definen mediante la estructura [ \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) de TF e incluyen el color de texto, el color de fondo del texto, el estilo de subrayado, el color de subrayado y el peso del subrayado.

Al representar texto, una aplicación debe obtener los atributos para mostrar del texto dibujado y usar los atributos para modificar cómo se dibuja el texto. Complete los pasos siguientes para obtener los atributos de visualización.

1.  Obtenga un objeto de propiedad para GUID \_ PROP ATTRIBUTE llamando a \_ [ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty).
2.  Obtenga el valor de GUID PROP ATTRIBUTE para el intervalo especificado mediante una llamada \_ \_ a [ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue). Esto proporciona un [valor TfGuidAtom.](tfguidatom.md)
3.  Convierta el [valor de TfGuidAtom](tfguidatom.md) en un GUID mediante una llamada a [ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid).
4.  Cree un [objeto ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para el atributo display llamando a [ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).
5.  Obtenga la información del atributo para mostrar llamando a [ITfDisplayAttributeInfo::GetAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo).

En el ejemplo de código siguiente se muestra una función que obtiene los atributos de presentación de un contexto, un intervalo y una cookie de edición proporcionados.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfContext::GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[ITfReadOnlyProperty::GetValue](/windows/desktop/api/Msctf/nf-msctf-itfreadonlyproperty-getvalue)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::GetGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

 ITfDisplayAttributeInfo::GetAttributeInfo 
</dt> </dl>

 

 




