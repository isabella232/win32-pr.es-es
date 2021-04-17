---
description: Valor que indica el tipo de sensor proporcionado por un origen de fotogramas, como color, infrarrojos o Depth.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: MF_MT_FRAMESOURCE_TYPES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659846"
---
# <a name="mf_mt_framesource_types-attribute"></a>MF \_ MT \_ FRAMESOURCE \_ Types (atributo)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Valor que indica el tipo de sensor proporcionado por un origen de fotogramas, como color, infrarrojos o Depth.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor debe ser un miembro de la enumeración [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) . Por compatibilidad con versiones anteriores, cuando este atributo no está definido en un tipo de medio, se supone que es **\_ MFFrameSourceTyes:: color**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                      |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
