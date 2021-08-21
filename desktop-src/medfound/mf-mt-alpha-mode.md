---
description: Especifica si el modo alfa para los tipos de vídeo multimedia de color es premultiplicado o recta.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c658cae64c68aa89c49230164707d75369c021767c6aa0b46818516ffa26513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035323"
---
# <a name="mf_mt_alpha_mode-attribute"></a>Atributo MF \_ MT \_ ALPHA \_ MODE

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Especifica si el modo alfa para los tipos de vídeo multimedia de color es premultiplicado o recta.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este valor se puede convertir en un [**valor DXGI \_ ALPHA \_ MODE.**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) Si este atributo no está presente, por compatibilidad con versiones anteriores, el valor es **DXGI \_ ALPHA MODE \_ \_ STRAIGHT** para el formato de vídeo que admite el canal alfa, como ARGB32, o **DXGI ALPHA MODE \_ \_ \_ IGNORE** para el formato de vídeo sin canal alfa, como RGB32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
