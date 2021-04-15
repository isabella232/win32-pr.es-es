---
description: Obtiene las características del origen multimedia del lector de origen.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361941"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>\_Atributo de \_ \_ características MEDIASOURCE del lector de origen MF \_

Obtiene las características del origen multimedia del lector de [origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es **una operación OR bit a bit** de marcas de la enumeración de [**\_ características de MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="remarks"></a>Observaciones

Para obtener este atributo, llame al método [**IMFSourceReader:: GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) en el lector de origen. Establezca el parámetro *dwStreamIndex* en el parámetro del **\_ lector de código fuente \_ \_ MF** y el parámetro *guidAttribute* en las \_ características de MediaSource del lector de código fuente MF \_ \_ \_ .

El tipo **PROPVARIANT** para este atributo es **VT \_ UI4**.

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
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> </dl>

 

 




