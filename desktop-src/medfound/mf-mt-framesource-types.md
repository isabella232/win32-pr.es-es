---
description: Valor que indica el tipo de sensor proporcionado por un origen de marco, como el color, el calor o la profundidad.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad3cddc28db050ec3fdb55e47ca2ceb1bd24fb2813bdf90fce439843957a7ae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113775"
---
# <a name="mf_mt_framesource_types-attribute"></a>Atributo MF \_ \_ MT FRAMESOURCE \_ TYPES

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que indica el tipo de sensor proporcionado por un origen de marco, como el color, el calor o la profundidad.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este valor debe ser miembro de la [**\_ enumeración MFFrameSourceTypes.**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) Por compatibilidad con versiones anteriores, cuando este atributo no está definido en un tipo de medio, se supone que es **\_ MFFrameSourceTyes::Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
