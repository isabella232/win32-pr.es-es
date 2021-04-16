---
description: Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: MFPROTECTION_VIDEO_FRAMES atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706129"
---
# <a name="mfprotection_video_frames-attribute"></a>MFPROTECTION \_ \_ atributo de fotogramas de vídeo

Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Un valor de 0 indica que se permite el acceso a la aplicación a los marcos. Esto puede determinarse como resultado de un acuerdo privado entre la aplicación y el sistema de protección de contenido determinado en uso.

Un valor de 1 indica que se permite el acceso de la aplicación a los marcos si la aplicación proporciona un certificado de aplicación válido (vea [**IMFMediaEngineProtectedContent:: SetApplicationCertificate**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)).

Un valor de 0xFFFFFFFF, que es el valor predeterminado, indica que no se permite el acceso a las aplicaciones a los marcos sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones para UWP de Windows 8\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones para UWP de Windows Server 2012\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




