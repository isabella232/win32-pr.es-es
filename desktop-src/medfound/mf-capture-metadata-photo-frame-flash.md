---
description: Indica si se desencadenó un flash para el fotograma capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff5e9a47c07c8d7a2cec4e7dbf7b34669301122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696760"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>\_Atributo de \_ \_ \_ fotograma fotográfico de METAdatos de captura MF \_

Indica si se desencadenó un flash para el fotograma capturado.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                               | Significado                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | No se activó un flash en este marco.<br/>                                                                                                   |
| <dl> <dt>distinto de cero</dt> </dl> | Se desencadenó un flash en este marco.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reservado<br/> No Compruebe explícitamente si el valor es 1. Las aplicaciones solo deben buscar! = 0 para indicar si se desencadenó un flash.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




