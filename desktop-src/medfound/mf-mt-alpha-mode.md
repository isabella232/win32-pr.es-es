---
description: Especifica si el modo alfa para los tipos de vídeo multimedia de color es premultiplicado o recta.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579897"
---
# <a name="mf_mt_alpha_mode-attribute"></a>Atributo MF \_ MT \_ ALPHA \_ MODE

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Especifica si el modo alfa para los tipos de vídeo multimedia de color es premultiplicado o recta.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor se puede convertir en un [**valor DXGI \_ ALPHA \_ MODE.**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) Si este atributo no está presente, por compatibilidad con versiones anteriores, el valor es **DXGI \_ ALPHA MODE \_ \_ STRAIGHT** para el formato de vídeo que admite el canal alfa, como ARGB32, o **DXGI ALPHA MODE \_ \_ \_ IGNORE** para el formato de vídeo sin canal alfa, como RGB32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
