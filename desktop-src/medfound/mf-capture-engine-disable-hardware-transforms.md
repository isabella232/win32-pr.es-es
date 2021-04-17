---
description: Deshabilita el uso de transformaciones de Media Foundation basadas en hardware (MFTs) en el motor de captura.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS atributo (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715653"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a>El \_ \_ atributo de \_ \_ transformaciones de hardware deshabilitar el motor de captura MF \_

Deshabilita el uso de transformaciones de Media Foundation basadas en hardware (MFTs) en el motor de captura.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

De forma predeterminada, el motor de captura utiliza descodificadores o codificadores de hardware. Para deshabilitar el uso de MFTs de hardware, establezca este atributo en **true** al crear el motor de captura.

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

 

 




