---
description: Deshabilita la conversión de velocidad de fotogramas en el MFT del procesador de vídeo.
ms.assetid: 98AA7B3A-281C-427D-805E-5C4EE1EFAE21
title: MF_XVP_DISABLE_FRC atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e82c60438a91111ffce6cc80c71fa76231b8e00d85644f4f56f1b496202d62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119940335"
---
# <a name="mf_xvp_disable_frc-attribute"></a>Atributo MF \_ XVP \_ DISABLE \_ FRC

Deshabilita la conversión de velocidad de fotogramas en [**el MFT del procesador de vídeo.**](video-processor-mft.md)

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE,** el procesador de vídeo no realizará la conversión de velocidad de fotogramas. De forma predeterminada, el procesador de vídeo convertirá la velocidad de fotogramas para que coincida con el tipo de medio de salida.

Para establecer este atributo:

1.  Llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) en el procesador de vídeo.
2.  Llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




