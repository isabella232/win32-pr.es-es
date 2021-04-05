---
description: Este atributo especifica protección adicional ofrecida por una autoridad de confianza de salida de vídeo (OTA) cuando un conector no ofrece protección de la salida.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001455"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM

Este atributo especifica protección adicional ofrecida por una autoridad de confianza de salida de vídeo (OTA) cuando un conector no ofrece protección de la salida.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Se trata de una protección adicional que ofrece una autoridad de confianza (OTA) de salida de vídeo cuando un conector no ofrece protección de salida (consulte [**IMFOutputTrustAuthority**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority)). En este caso, la OTA puede ofrecer esta protección cuyo efecto es el mismo que el de la protección de [ \_ CONSTRICTVIDEO de MFPROTECTION](mfprotection-constrictvideo.md) . Esto se define para evitar la confusión con llamadas anteriores a interacciones de [**IMFOutputPolicy:: GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) en las que se usó la presencia de MFPROTECTION \_ CONSTRICTVIDEO Protection para ayudar a identificar el pseudo conector del administrador de ventanas de escritorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




