---
description: Deshabilita el uso de complementos de cámara posteriores al procesamiento por parte del Lector de origen.
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f66ae9c69d13b6af3e368b57a3f864f031d0cc7e63716d2267ae5d3869d102b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600295"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a>Atributo DISABLE \_ \_ CAMERA \_ \_ \_ PLUGINS de MF SOURCE READER

Deshabilita el uso de complementos de cámara posteriores al procesamiento por parte del [lector de origen.](source-reader.md)

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo se aplica cuando se usa el Lector de origen con un origen de captura de vídeo. Si este atributo es **TRUE,** impide que el Lector de origen cargue los complementos posteriores al procesamiento que pueda proporcionar la cámara. De lo contrario, el Lector de origen los cargará de forma predeterminada.

El valor predeterminado de este atributo es **FALSE.** Establezca el atributo al crear el lector de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                              |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




