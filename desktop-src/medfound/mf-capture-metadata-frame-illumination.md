---
description: Un valor que indica si un fotograma se capturó con la iluminación de infrarrojos (IR) activa.
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: MF_CAPTURE_METADATA_FRAME_ILLUMINATION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696603"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a>\_Atributo de \_ \_ iluminación de fotogramas de metadatos de captura MF \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Un valor que indica si un fotograma se capturó con la iluminación de infrarrojos (IR) activa.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Este atributo es una máscara de máscara. Es un valor de 64 bits para la compatibilidad con versiones anteriores.

La iluminación activa es cuando un dispositivo tiene un emisor de luz cerca de la cámara de INFRARROJOs que emite un rayo de luz para iluminar la escena, lo que normalmente emite luz de INFRARROJOs, por lo que no afectará a los ojos humanos. Establezca valor en (valor & 0x1)! = 0 si el fotograma se capturó cuando la iluminación activa estaba activada y establecida (valor & 0x1) = = 0 si la iluminación activa estaba desactivada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




