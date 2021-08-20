---
description: Especifica cuándo se modificó por última vez una presentación.
ms.assetid: 12990de2-7656-4781-943b-c46f42a0e38d
title: MF_PD_LAST_MODIFIED_TIME atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b906b867db0b96b96927a8c21ee62e944fcbe3369f852811536d75f63862b807
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691777"
---
# <a name="mf_pd_last_modified_time-attribute"></a>Atributo MF \_ PD \_ LAST MODIFIED \_ \_ TIME

Especifica cuándo se modificó por última vez una presentación.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Comentarios

Los orígenes multimedia pueden establecer este atributo en un descriptor de presentación. El valor del atributo es una **estructura FILETIME,** que se documenta en el SDK Windows.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Atributos del descriptor de presentación](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




