---
description: Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: Propiedad MFPKEY_EXATTRIBUTE_SUPPORTED (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908778"
---
# <a name="mfpkey_exattribute_supported-property"></a>\_Propiedad compatible con el MFPKEY EXattribute \_

Especifica si una transformación de Media Foundation (MFT) copia los atributos de los ejemplos de entrada a los ejemplos de salida.



Tipo de datos

Tipo PROPVARIANT (VT)

Miembro de PROPVARIANT

**VARIANTE \_ bool**

VT \_ bool

**boolVal**



## <a name="remarks"></a>Observaciones

Este atributo puede tener los valores siguientes.



| Value              | Descripción                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VARIANTE \_ true**  | MFT copia los atributos de los ejemplos de entrada a los ejemplos de salida.                                                                                 |
| **VARIANTE \_ false** | La sesión multimedia copia los atributos de los ejemplos de entrada a los ejemplos de salida. No sobrescribe ningún atributo que el MFT establezca en los ejemplos de salida. |



 

Para obtener este atributo, llame a **QueryInterface** en la MFT para la interfaz **IPropertyStore** .

El valor predeterminado es **Variant \_ false**. Si MFT no expone la interfaz **IPropertyStore** o si no se establece esta propiedad, trate el valor como **variante \_ false**.

Esta propiedad es de solo lectura.

> [!NOTE] 
> Este atributo no se aplica a MFTs asincrónicos. Los atributos no se copiarán de los ejemplos de entrada a los ejemplos de salida de MFTs asincrónicos, independientemente del valor de este atributo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se devuelve VARIANT \_ true si una MFT copia los atributos de ejemplo.


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Atributos de ejemplo](sample-attributes.md)
</dt> <dt>

[**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




