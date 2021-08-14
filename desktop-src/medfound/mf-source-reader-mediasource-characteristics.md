---
description: Obtiene las características del origen de medios del Lector de origen.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739990"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>Atributo MF \_ SOURCE \_ READER \_ MEDIASOURCE \_ CHARACTERISTICS

Obtiene las características del origen de medios del Lector [de origen.](source-reader.md)

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es un OR bit a bit **de** marcas de la [**enumeración MFMEDIASOURCE \_ CHARACTERISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)

## <a name="remarks"></a>Observaciones

Para obtener este atributo, llame al [**método IMFSourceReader::GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) en el lector de origen. Establezca el *parámetro dwStreamIndex* en **MF SOURCE READER \_ \_ \_ MEDIASOURCE** y el parámetro *guidAttribute* en MF \_ SOURCE READER \_ \_ \_ MEDIASOURCE CHARACTERISTICS.

El **tipo PROPVARIANT** para este atributo es **VT \_ UI4.**

## <a name="examples"></a>Ejemplos


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




