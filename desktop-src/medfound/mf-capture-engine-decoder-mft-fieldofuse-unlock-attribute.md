---
description: Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f586325f883595e1336ed946611850b3c51d5443dbd9f6e68830502284a64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061086"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>Atributo MF \_ CAPTURE \_ ENGINE DECODER \_ \_ MFT \_ FIELDOFUSE \_ UNLOCK \_

Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Comentarios

El valor de este atributo es un puntero a la interfaz [**IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) implementada por el autor de la llamada. Se espera que la implementación del autor de la llamada de esta interfaz realice un protocolo de enlace con el descodificador, como se describe en [Restricciones de campo de uso](field-of-use-restrictions.md). Microsoft Media Foundation no define el protocolo de enlace; normalmente, implicaría algún tipo de intercambio criptográfico.

Internamente, el motor de captura establece el puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) en el descodificador estableciendo el atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ Attribute](mft-fieldofuse-unlock-attribute.md) del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




