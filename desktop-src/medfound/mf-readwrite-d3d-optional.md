---
description: Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el lector de origen o en el escritor de receptores.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cebc24991e5c2bfb90b7153f3a90a2e7447c2daef987b2956680e89f162223ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664115"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>Atributo \_ MF READWRITE \_ D3D \_ OPTIONAL

Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el lector [de origen](source-reader.md) o en el escritor [de receptores.](sink-writer.md)

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

Este atributo solo se aplica si la aplicación habilita la compatibilidad con Direct3D mediante el atributo [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md) o [MF SINK WRITER \_ \_ \_ D3D \_ MANAGER.](mf-sink-writer-d3d-manager.md)

Si la aplicación habilita la compatibilidad con Direct3D, tanto el lector de origen como el escritor receptor intentarán asignar superficies de Direct3D para vídeo. Si se produce un error y el atributo MF \_ READWRITE D3D OPTIONAL es TRUE, el lector de origen o el escritor del receptor se retendrán en la asignación de superficies de vídeo en la memoria \_ \_ del sistema.  De lo contrario, si no se pueden asignar superficies de Direct3D y MF \_ READWRITE \_ D3D OPTIONAL es \_ **FALSE,** se produce un error durante el procesamiento.

Si la aplicación no habilita la compatibilidad con Direct3D, el lector de origen/escritor receptor usa la memoria del sistema y omite el valor de MF \_ READWRITE \_ D3D \_ OPTIONAL.

Este atributo es opcional. El valor predeterminado es **FALSE**. Establezca el atributo al crear el lector de origen o el escritor de receptores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de escritor de receptores](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




