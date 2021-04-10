---
description: Establece un puntero al Administrador de dispositivos de DXGI en el motor de captura.
ms.assetid: 1DFDE7AB-7DFF-4C39-9460-E42E37649AAC
title: MF_CAPTURE_ENGINE_D3D_MANAGER atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3c5e87d4817f539f91ecd55aec10a2086afeaeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154645"
---
# <a name="mf_capture_engine_d3d_manager-attribute"></a>\_Atributo de \_ Administrador de D3D del motor de captura MF \_ \_

Establece un puntero al Administrador de dispositivos de DXGI en el motor de captura.

## <a name="data-type"></a>Tipo de datos

**IUnknown \** _

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [_ *IMFDXGIDeviceManager* *](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) . Este atributo permite al motor de captura asignar fotogramas de vídeo mediante superficies de DXGI y usar la aceleración de hardware para la descodificación y el procesamiento de vídeo.

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

 

 




