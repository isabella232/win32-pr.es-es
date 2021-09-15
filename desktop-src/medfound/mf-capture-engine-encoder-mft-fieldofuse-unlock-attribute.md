---
description: Permite que el motor de captura use un codificador que tenga restricciones de campo de uso.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474222"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a>Atributo \_ del atributo \_ \_ \_ MFT \_ FIELDOFUSE UNLOCK DEL CODIFICADOR DEL \_ MOTOR DE CAPTURA \_ DE MF

Permite que el motor de captura use un codificador que tenga restricciones de campo de uso.

## <a name="data-type"></a>Tipo de datos

**IUnknown\***

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [**IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) implementada por el autor de la llamada. Se espera que la implementación del autor de la llamada de esta interfaz realice un protocolo de enlace con el codificador, como se describe en [Restricciones de campo de uso](field-of-use-restrictions.md). Microsoft Media Foundation no define el protocolo de enlace; normalmente, implicaría algún tipo de intercambio criptográfico.

Internamente, el motor de captura establece el puntero [**DE TIPO IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) en el codificador estableciendo el atributo de atributo [ \_ MFT FIELDOFUSE \_ UNLOCK \_ del](mft-fieldofuse-unlock-attribute.md) codificador.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Encabezado<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




