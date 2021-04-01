---
description: Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el lector de origen o el escritor de receptores.
ms.assetid: 3844ED7B-E1E5-4CD7-B080-FE7EC7B28AC5
title: MF_READWRITE_D3D_OPTIONAL atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8c78295dd12e5d187c9be380305dc225d7e8e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279045"
---
# <a name="mf_readwrite_d3d_optional-attribute"></a>MF \_ ReadWrite \_ ( \_ atributo opcional)

Especifica si la aplicación requiere compatibilidad con Microsoft Direct3D en el [lector de origen](source-reader.md) o el escritor de [receptores](sink-writer.md).

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

Este atributo solo se aplica si la aplicación habilita la compatibilidad con Direct3D mediante el atributo de administrador de D3D del [ \_ lector de código fuente MF \_ \_ \_ ](mf-source-reader-d3d-manager.md) o el atributo de [ \_ \_ \_ \_ Administrador de recepción de receptor MF](mf-sink-writer-d3d-manager.md) .

Si la aplicación habilita la compatibilidad con Direct3D, el lector de origen y el escritor del receptor intentarán asignar las superficies de Direct3D para el vídeo. Si se produce un error en esta y el \_ \_ atributo opcional MF ReadWrite D3D \_ es **true**, el sistema de escritura de origen/receptor de lectura revertirá a la asignación de superficies de vídeo en la memoria del sistema. De lo contrario, si no se pueden asignar superficies de Direct3D y MF \_ ReadWrite \_ \_ opcional es **false**, se produce un error durante el procesamiento.

Si la aplicación no habilita la compatibilidad con Direct3D, el sistema de escritura del receptor o el lector de origen usa la memoria del sistema y omite el valor de MF \_ ReadWrite ( \_ opcional) \_ .

Este atributo es opcional. El valor predeterminado es **FALSE**. Establezca el atributo al crear el lector de origen o el escritor del receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos del escritor de receptor](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




