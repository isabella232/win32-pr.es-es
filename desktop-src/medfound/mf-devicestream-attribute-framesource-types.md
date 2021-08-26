---
description: Representa el tipo de origen del marco.
ms.assetid: 4A2B427E-E654-48BA-8BF4-16F1B1F8D266
title: MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce2e7f90f4e5f23e99bac8e532455fac1309cc0e20177c5800d85f4580e20a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013195"
---
# <a name="mf_devicestream_attribute_framesource_types-attribute"></a>Atributo \_ FRAMESOURCE TYPES del \_ ATRIBUTO MF DEVICESTREAM \_ \_

Representa el tipo de origen del marco.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este valor de este atributo debe ser una máscara de bits de uno o varios valores de la [**enumeración MFFrameSourceTypes.**](/windows/desktop/api/mfapi/ne-mfapi-mfframesourcetypes) Para admitir la compatibilidad con versiones anteriores, cuando este atributo no está definido para un tipo de medio, se supone que tiene el valor **MFFrameSourceTypes::Color**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1607 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




