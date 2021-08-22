---
description: Valor que indica si un fotograma se capturó mediante iluminación de insondación activa (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23658f8f396a81180a074badc43e98d0f392fc355c1a81a4d1e731d132de12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973954"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>Atributo DE MARCO DE METADATOS DE CAPTURA DE MF \_ AL ATRIBUTO DE \_ \_ \_ INDABA DE METADATOS DE

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que indica si un fotograma se capturó mediante iluminación de insondación activa (IR).

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Este atributo es una máscara de bits. Es un valor de 64 bits por compatibilidad con versiones anteriores.

La iluminación activa se realiza cuando un dispositivo tiene un emisor de luz cerca de la cámara de IR que emite un haz de luz para iluminación de la escena, lo que normalmente emite luz de IR para que no adorme los ojos humanos. Establezca el valor en (valor & 0x1) != 0 si el marco se capturó cuando la iluminación activa estaba activada y se estableció (valor & 0x1) == 0 si la iluminación activa estaba desactivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




