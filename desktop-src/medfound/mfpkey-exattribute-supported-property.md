---
description: Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED propiedad (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 248609828df3ef977112058ffe0d169104e68c181fa455ef27f2adcea0220aaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663514"
---
# <a name="mfpkey_exattribute_supported-property"></a>Propiedad MFPKEY \_ EXATTRIBUTE \_ SUPPORTED

Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Comentarios

Este atributo puede tener los siguientes valores.



| Valor              | Descripción                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | MFT copia los atributos de los ejemplos de entrada a los ejemplos de salida.                                                                                 |
| **VARIANT \_ FALSE** | La sesión multimedia copia los atributos de los ejemplos de entrada a los ejemplos de salida. No sobrescribe ningún atributo que MFT establece en los ejemplos de salida. |



 

Para obtener este atributo, llame **a QueryInterface** en MFT para la **interfaz IPropertyStore.**

El valor predeterminado es **VARIANT \_ FALSE.** Si MFT no expone la interfaz **IPropertyStore** o si no se establece esta propiedad, trate el valor **como VARIANT \_ FALSE.**

Esta propiedad es de solo lectura.

> [!NOTE] 
> Este atributo no se aplica a las MTA asincrónicas. Los atributos no se copiarán de los ejemplos de entrada a los ejemplos de salida para MTA asincrónicos, independientemente del valor de este atributo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se devuelve VARIANT \_ TRUE si un MFT copia atributos de ejemplo.


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




