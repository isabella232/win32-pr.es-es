---
description: Especifica si una transformación Media Foundation datos (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: MFPKEY_EXATTRIBUTE_SUPPORTED propiedad (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468638"
---
# <a name="mfpkey_exattribute_supported-property"></a>Propiedad MFPKEY \_ EXATTRIBUTE \_ SUPPORTED

Especifica si una transformación Media Foundation datos (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.



Tipo de datos

Tipo PROPVARIANT (vt)

Miembro de PROPVARIANT

**VARIANT \_ BOOL**

VT \_ BOOL

**boolVal**



## <a name="remarks"></a>Observaciones

Este atributo puede tener los siguientes valores.



| Value              | Descripción                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANT \_ TRUE**  | MFT copia los atributos de los ejemplos de entrada a los ejemplos de salida.                                                                                 |
| **VARIANT \_ FALSE** | La sesión multimedia copia los atributos de los ejemplos de entrada a los ejemplos de salida. No sobrescribe ningún atributo que MFT establece en los ejemplos de salida. |



 

Para obtener este atributo, llame **a QueryInterface** en MFT para la **interfaz IPropertyStore.**

El valor predeterminado es **VARIANT \_ FALSE.** Si el MFT no expone la **interfaz IPropertyStore** o si no se establece esta propiedad, trate el valor **como VARIANT \_ FALSE.**

Esta propiedad es de solo lectura.

> [!NOTE] 
> Este atributo no se aplica a las MTA asincrónicas. Los atributos no se copiarán de los ejemplos de entrada a los ejemplos de salida para las MTA asincrónicas, independientemente del valor de este atributo.

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



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




