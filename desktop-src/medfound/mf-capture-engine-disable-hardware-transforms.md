---
description: Deshabilita el uso de transformaciones basadas Media Foundation hardware (MTA) en el motor de captura.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7818e79a78ab346ffb8a1967569fdd8711e2b948e0eb656f032770487d8820ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956815"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>Atributo DISABLE \_ \_ HARDWARE \_ TRANSFORMS DEL \_ MOTOR DE CAPTURA \_ DE MF

Deshabilita el uso de transformaciones basadas Media Foundation hardware (MTA) en el motor de captura.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

De forma predeterminada, el motor de captura usa descodificadores de hardware o codificadores. Para deshabilitar el uso de MTA de hardware, establezca este atributo en **TRUE** al crear el motor de captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




