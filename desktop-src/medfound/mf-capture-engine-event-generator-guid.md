---
description: Identifica el componente que generó un evento de captura.
ms.assetid: DCCF3054-AF14-44C7-84C0-B03E35B5D90A
title: MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88efff7cea540c1fae2c14d44dd7676c4f523b562a66a4c4f4bc4dffea59d5e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474473"
---
# <a name="mf_capture_engine_event_generator_guid-attribute"></a>Atributo GUID \_ del GENERADOR DE EVENTOS DEL MOTOR DE CAPTURA \_ \_ \_ \_ DE MF

Identifica el componente que generó un evento de captura.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Comentarios

Este atributo aparece en algunos eventos del motor de captura. Para obtener este atributo, llame [**a IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid) en el objeto de evento. El objeto de evento se pasa a la aplicación a través del [**método IMFCaptureEngineOnEventCallback::OnEvent.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)

El valor es un identificador de interfaz para el componente que generó el evento. Por ejemplo, el valor **IID \_ IMFCapturePreviewSink** indica el receptor de vista previa ([**IMFCapturePreviewSink**](/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcapturepreviewsink)). No todos los eventos de captura contienen este atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                   |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del motor de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




