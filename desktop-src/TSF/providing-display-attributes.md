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
# <a name="providing-display-attributes"></a>Proporcionar atributos para mostrar

El marco de trabajo de servicios de texto (TSF) permite que un servicio de texto proporcione atributos de presentación para el texto. Esto permite proporcionar información visual adicional al usuario. Por ejemplo, un servicio de texto de corrector ortográfico puede resaltar una palabra mal escrita con un subrayado rojo. Los atributos de visualización que se proporcionan se definen en la estructura [TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute) e incluyen el color de texto, el color de fondo del texto, el estilo de subrayado, el color de subrayado y el grosor

Los clientes que usan esta información de atributos de pantalla suelen ser aplicaciones, pero también pueden incluir servicios de texto. El administrador de TSF media entre el proveedor de atributos de presentación y el cliente de y realiza un seguimiento del proveedor de atributos de presentación de los atributos de presentación específicos.

Para proporcionar atributos para mostrar, un servicio de texto debe hacer lo siguiente.

1.  Registre el servicio de texto como un proveedor de atributos para mostrar llamando a [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con el identificador de clase del servicio de texto para el primer parámetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para el segundo parámetro y el identificador de clase del servicio de texto de nuevo para el tercer parámetro.
2.  Implemente [ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider) y haga que esté disponible en el generador de clases.
3.  Implemente [IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo) y haga que esté disponible en [ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo).
4.  Implemente un objeto [ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo) para cada tipo de atributo de presentación que proporciona el servicio de texto.

## <a name="applying-the-display-attributes"></a>Aplicar los atributos para mostrar

El servicio de texto debe aplicar el atributo display a un intervalo de texto. Un servicio de texto solo puede modificar el valor de la propiedad durante una sesión de edición de lectura/escritura.

Suponiendo que se encuentre en una sesión de edición de lectura/escritura, se aplicará un atributo de visualización de la siguiente manera.

1.  Obtenga un objeto [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) que abarque el texto al que se aplicará el atributo de visualización.
2.  Obtenga un objeto [ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty) para los atributos de texto mediante una llamada a [ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty) con el \_ atributo prop de GUID \_ .
3.  Cree un [TfGuidAtom](tfguidatom.md) a partir del **GUID** del identificador de atributo de presentación definido por el servicio de texto mediante una llamada a [ITfCategoryMgr:: RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).
4.  Inicialice una variable VARIANT en VT \_ I4 y establezca el miembro **lVal** en el **TfGuidAtom** creado en el paso anterior.
5.  Aplique el atributo display al intervalo mediante una llamada a [ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue) con la cookie de edición de lectura/escritura, el intervalo y la variante inicializada en el paso anterior.


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



## <a name="supplying-the-display-attribute-information-object"></a>Proporcionar el objeto de información de atributo para mostrar

Un cliente obtiene un objeto **ITfDisplayAttributeInfo** de una de estas dos maneras.

1.  El cliente llama a [ITfDisplayAttributeMgr:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo) con el identificador **GUID** del atributo display. La primera vez que el cliente llama a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo**, el administrador de TSF creará una instancia del proveedor de atributos de visualización llamando a CoCreateInstance con el identificador de clase pasado como primer parámetro a **ITfCategoryMgr:: RegisterCategory**. Las llamadas subsiguientes a **ITfDisplayAttributeMgr:: GetDisplayAttributeInfo** volverán a usar el objeto de proveedor de atributos de presentación.

    Después, el administrador de TSF llama a [ITfDisplayAttributeProvider:: GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo) con el **GUID** del atributo de visualización para obtener el objeto **ITfDisplayAttributeInfo** .

    A continuación, el administrador de TSF vuelve a pasar el objeto **ITfDisplayAttributeInfo** al cliente.

2.  El cliente llama a [ITfDisplayAttributeMgr:: EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo) para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos de presentación proporcionados por todos los proveedores de atributos de presentación. El administrador de TSF enumera cada proveedor de atributos de visualización y crea una instancia de cada proveedor llamando a CoCreateInstance con el identificador de clase pasado como el tercer parámetro a **ITfCategoryMgr:: RegisterCategory**.

    Después, el administrador de TSF llama a **ITfDisplayAttributeProvider:: EnumDisplayAttributeInfo** de cada proveedor para obtener un objeto **IEnumTfDisplayAttributeInfo** que contiene todos los atributos de presentación proporcionados por el proveedor.

    A continuación, el administrador de TSF llama al método [IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next) del proveedor, agregando cada objeto **ITfDisplayAttributeInfo** obtenido al propio enumerador del administrador, hasta que se alcance el final de la enumeración del proveedor.

    Cuando todos los objetos **ITfDisplayAttributeInfo** de todos los proveedores de atributos de presentación se agregan al enumerador del administrador de TSF, el administrador devuelve el enumerador al cliente. Después, el cliente llama a **IEnumTfDisplayAttributeInfo:: Next** una o más veces para obtener los objetos **ITfDisplayAttributeInfo** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TF \_ DISPLAYATTRIBUTE](/windows/desktop/api/Msctf/ns-msctf-tf_displayattribute)
</dt> <dt>

[ITfCategoryMgr::RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory)
</dt> <dt>

[ITfDisplayAttributeProvider](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeprovider)
</dt> <dt>

[IEnumTfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-ienumtfdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-enumdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeInfo](/windows/desktop/api/Msctf/nn-msctf-itfdisplayattributeinfo)
</dt> <dt>

[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)
</dt> <dt>

[ITfProperty](/windows/desktop/api/Msctf/nn-msctf-itfproperty)
</dt> <dt>

[ITfContext:: GetProperty](/windows/desktop/api/Msctf/nf-msctf-itfcontext-getproperty)
</dt> <dt>

[TfGuidAtom](tfguidatom.md)
</dt> <dt>

[ITfCategoryMgr::RegisterGUID](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> <dt>

[ITfProperty:: SetValue](/windows/desktop/api/Msctf/nf-msctf-itfproperty-setvalue)
</dt> <dt>

[ITfDisplayAttributeMgr::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeProvider::GetDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributeprovider-getdisplayattributeinfo)
</dt> <dt>

[ITfDisplayAttributeMgr::EnumDisplayAttributeInfo](/windows/desktop/api/Msctf/nf-msctf-itfdisplayattributemgr-enumdisplayattributeinfo)
</dt> <dt>

 IEnumTfDisplayAttributeInfo 
</dt> <dt>

 ITfDisplayAttributeProvider::EnumDisplayAttributeInfo 
</dt> <dt>

[IEnumTfDisplayAttributeInfo:: Next](/windows/desktop/api/Msctf/nf-msctf-ienumtfdisplayattributeinfo-next)
</dt> </dl>

 

 




