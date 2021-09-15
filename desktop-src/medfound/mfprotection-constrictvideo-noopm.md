---
description: Este atributo especifica la protección adicional que ofrece una autoridad de confianza de salida (OTA) de vídeo cuando un conector no ofrece protección de salida.
ms.assetid: D3EAD386-E730-44E8-9E05-773E1E2175C5
title: MFPROTECTION_CONSTRICTVIDEO_NOOPM atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617bd629852a3aa03708d12dca7736b4f773094b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475660"
---
# <a name="mfprotection_constrictvideo_noopm-attribute"></a>Atributo MFPROTECTION \_ CONSTRICTVIDEO \_ NOOPM

Este atributo especifica la protección adicional que ofrece una autoridad de confianza de salida (OTA) de vídeo cuando un conector no ofrece protección de salida.

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="remarks"></a>Observaciones

Se trata de una protección adicional que ofrece una entidad de confianza de salida de vídeo (OTA) cuando un conector no ofrece protección de salida (consulte EL ARTÍCULO SOBRE [**LA SALIDATrustAuthority).**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority) En este caso, el OTA puede ofrecer esta protección cuyo efecto es el mismo que la protección [MFPROTECTION \_ CONSTRICTVIDEO.](mfprotection-constrictvideo.md) Esto se define para evitar confusiones con las llamadas anteriores a [**interacciones DE MFOutputPolicy::GenerateRequiredSchemas**](/windows/desktop/api/mfidl/nf-mfidl-imfoutputpolicy-generaterequiredschemas) en las que se usó la presencia de la protección MFPROTECTION CONSTRICTVIDEO para ayudar a identificar el pseudoconexiones del administrador de ventanas de \_ escritorio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




