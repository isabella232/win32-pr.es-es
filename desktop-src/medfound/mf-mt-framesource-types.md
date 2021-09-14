---
description: Valor que indica el tipo de sensor proporcionado por un origen de marco, como el color, el calor o la profundidad.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363995"
---
# <a name="mf_mt_framesource_types-attribute"></a>Atributo MF \_ \_ MT FRAMESOURCE \_ TYPES

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Valor que indica el tipo de sensor proporcionado por un origen de marco, como el color, el calor o la profundidad.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor debe ser miembro de la [**\_ enumeración MFFrameSourceTypes.**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) Por compatibilidad con versiones anteriores, cuando este atributo no está definido en un tipo de medio, se supone que es **\_ MFFrameSourceTyes::Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Servidor, solo aplicaciones de escritorio de la versión 1709 \[\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
