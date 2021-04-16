---
description: Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.
ms.assetid: EDE6D207-FD84-4DEB-9BF5-0952C454B00F
title: MF_CAPTURE_ENGINE_DECODER_MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d858d4382b669621f6dc43cbfee77b62e9d1124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715654"
---
# <a name="mf_capture_engine_decoder_mft_fieldofuse_unlock_attribute-attribute"></a>\_Módulo de captura MF \_ \_ descodificador de \_ MFT \_ FIELDOFUSE \_ Unlock \_ Attribute atributo

Permite que el motor de captura use un descodificador que tenga restricciones de campo de uso.

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [_ *IMFFieldOfUseMFTUnlock* *](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implementada por el llamador. Se espera que la implementación del llamador de esta interfaz realice un protocolo de enlace con el descodificador, tal y como se describe en el [campo de restricciones de uso](field-of-use-restrictions.md). Microsoft Media Foundation no define el protocolo de enlace, normalmente implicaría algún tipo de intercambio criptográfico.

Internamente, el motor de captura establece el puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) en el descodificador estableciendo el atributo [MFT \_ FIELDOFUSE \_ Unlock \_](mft-fieldofuse-unlock-attribute.md) del descodificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




