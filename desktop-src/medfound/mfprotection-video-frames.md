---
description: Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.
ms.assetid: 7D2A9003-B36E-4082-877E-8AC7F5645E89
title: MFPROTECTION_VIDEO_FRAMES atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a8ccfc56fb1c1b52b14e16d8e702111f3d8564
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474068"
---
# <a name="mfprotection_video_frames-attribute"></a>Atributo MFPROTECTION \_ VIDEO \_ FRAMES

Especifica si se permite a una aplicación el acceso a fotogramas de vídeo sin comprimir.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Un valor de 0 indica que se permite a la aplicación el acceso a los fotogramas. Esto puede determinarse como resultado de un acuerdo privado entre la aplicación y el sistema de protección de contenido concreto en uso.

El valor 1 indica que se permite a la aplicación el acceso a fotogramas si la aplicación proporciona un certificado de aplicación válido (vea [**IMFMediaEngineProtectedContent::SetApplicationCertificate).**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setapplicationcertificate)

Un valor de 0xFFFFFFFF, que es el valor predeterminado, indica que no se permite el acceso de ninguna aplicación a fotogramas sin comprimir.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 Solo aplicaciones para UWP\]<br/>                                             |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 Solo aplicaciones para UWP\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




