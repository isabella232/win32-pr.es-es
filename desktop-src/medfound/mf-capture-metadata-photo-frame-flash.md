---
description: Indica si se desencadenó un flash para el fotograma capturado.
ms.assetid: CF900CB4-8967-40F3-B60C-867192A641E9
title: MF_CAPTURE_METADATA_PHOTO_FRAME_FLASH atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a885786674c524b382912100171502dba78a010b2169738233b5aaad88ed701a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973924"
---
# <a name="mf_capture_metadata_photo_frame_flash-attribute"></a>Atributo MF \_ CAPTURE METADATA PHOTO FRAME \_ \_ \_ \_ FLASH

Indica si se desencadenó un flash para el fotograma capturado.

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Valor                                                                               | Significado                                                                                                                                               |
|-------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>        | No se desencadenó un flash en este marco.<br/>                                                                                                   |
| <dl> <dt>distinto de cero</dt> </dl> | Se desencadenó un flash en este marco.<br/>                                                                                                       |
| <dl> <dt>1</dt> </dl>        | Reservada<br/> No compruebe explícitamente un valor de 1. Las aplicaciones solo deben comprobar !=0 para indicar si se desencadenó una flash.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




