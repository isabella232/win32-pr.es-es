---
description: Especifica si una Media Foundation transformación (MFT) admite Microsoft Direct3D 11.
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: MF_SA_D3D11_AWARE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59a996493ace387d1c6e93c734110772274986c6e5490b9e0e08567024d47c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955405"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>Atributo MF \_ SA \_ D3D11 \_ AWARE

Especifica si una Media Foundation transformación (MFT) admite Microsoft Direct3D 11.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo solo se aplica a las MFP de vídeo. Para consultar este atributo, llame [**a IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) para obtener el almacén de atributos MFT. Si **GetAttributes se** realiza correctamente, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

-   Si el atributo es distinto de cero, el cliente puede dar al MFT un puntero a la interfaz [**DEGDXGIDeviceManager antes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) de que se inicie el streaming. Para ello, el cliente envía el [**mensaje MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) al MFT. No es necesario que el cliente envíe este mensaje.
-   Si este atributo es cero **(FALSE),** MFT no admite Direct3D 11 y el cliente no debe enviar el mensaje [**MFT \_ MESSAGE SET \_ \_ D3D \_ MANAGER**](mft-message-set-d3d-manager.md) al MFT.

El valor predeterminado de este atributo es **FALSE.** Trate este atributo como de solo lectura. No cambie el valor; MFT omitirá los cambios en el valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Compatibilidad con la decodificación de vídeo de Direct3D 11 en Media Foundation](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




