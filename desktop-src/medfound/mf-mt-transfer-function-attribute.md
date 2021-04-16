---
description: Especifica la función de conversión de RGB a RGB para un tipo de medio de vídeo.
ms.assetid: c64c2135-f588-4d7a-9ca8-ae4f7b290572
title: MF_MT_TRANSFER_FUNCTION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d175a0e40d0aba45b4ec664d71e236e077e09a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716152"
---
# <a name="mf_mt_transfer_function-attribute"></a>MF \_ MT \_ Transfer ( \_ atributo de función)

Especifica la función de conversión de RGB a R'G'B ' para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFVideoTransferFunction**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideotransferfunction) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

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

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Información de color ampliada](extended-color-information.md)
</dt> </dl>

 

 




