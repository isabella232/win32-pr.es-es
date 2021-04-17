---
description: Representa el tipo de origen del marco.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8823a828a81290fe3b039c8959d694c62331622f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696759"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>Atributo MF \_ DEVICESTREAM \_ atributo \_ FRAMESOURCE \_ Types

Representa el tipo de origen del marco.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este valor de este atributo debe ser una máscara de máscara de uno o más valores de la enumeración [**MFFrameSourceTypes**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) . Para admitir la compatibilidad con versiones anteriores, cuando este atributo no está definido para un tipo de medio, se supone que tiene el valor **MFFrameSourceTypes:: color**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1607 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




