---
description: Identifica qué flujo generó un evento de captura.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580404"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>Atributo MF \_ CAPTURE ENGINE EVENT STREAM \_ \_ \_ \_ INDEX

Identifica qué flujo generó un evento de captura.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

## <a name="remarks"></a>Observaciones

Este atributo aparece en algunos eventos del motor de captura. Para obtener este atributo, llame [**a IMFAttributes::GetUINT32 en**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) el objeto de evento. El objeto de evento se pasa a la aplicación a través del [**método IMFCaptureEngineOnEventCallback::OnEvent.**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)

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

[**IMFCaptureEngineOnEventCallback::OnEvent**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




