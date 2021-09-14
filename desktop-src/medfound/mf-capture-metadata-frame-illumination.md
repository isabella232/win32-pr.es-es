---
description: Valor que indica si un fotograma se capturó mediante iluminación de insondisibilidad activa (IR).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364094"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>Atributo MF \_ CAPTURE METADATA FRAME AL QUE SE LE HA APLICADO EL NOMBRE DE \_ \_ \_ ARCHIVO

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que indica si un fotograma se capturó mediante iluminación de insondisibilidad activa (IR).

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Este atributo es una máscara de bits. Es un valor de 64 bits por compatibilidad con versiones anteriores.

La iluminación activa se realiza cuando un dispositivo tiene un emisor de luz cerca de la cámara de IR que emite un haz de luz para iluminar la escena, lo que normalmente emite luz de IR para que no atasque los ojos humanos. Establezca el valor en (valor & 0x1) != 0 si el marco se capturó cuando la iluminación activa estaba activada y se estableció (valor & 0x1) == 0 si la iluminación activa estaba desactivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




