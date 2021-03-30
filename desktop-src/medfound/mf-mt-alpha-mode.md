---
description: Especifica si el modo alfa para los tipos de vídeo en color está premultiplicado o recto.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: MF_MT_ALPHA_MODE atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082729"
---
# <a name="mf_mt_alpha_mode-attribute"></a>\_Atributo de \_ modo alfa MF MT \_

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Especifica si el modo alfa para los tipos de vídeo en color está premultiplicado o recto.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor se puede convertir en un valor de [**\_ \_ modo alfa de DXGI**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) . Si este atributo no está presente, para la compatibilidad con versiones anteriores, el valor es el **\_ modo alfa de dxgi \_ \_ recto** para el formato de vídeo compatible con el canal alfa, como ARGB32, o el **\_ modo Alpha alfa \_ \_ omite** el formato de vídeo sin canal alfa, como RGB32.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
