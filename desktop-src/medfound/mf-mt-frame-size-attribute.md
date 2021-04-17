---
description: Ancho y alto de un fotograma de vídeo, en píxeles.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: MF_MT_FRAME_SIZE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659983"
---
# <a name="mf_mt_frame_size-attribute"></a>\_Atributo de \_ tamaño de marco MF MT \_

Ancho y alto de un fotograma de vídeo, en píxeles.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Los 32 bits superiores contienen el ancho y los bits inferiores 32 contienen el alto.

Para establecer este atributo, utilice la función [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) . Para obtener este atributo, utilice la función [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="examples"></a>Ejemplos


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




