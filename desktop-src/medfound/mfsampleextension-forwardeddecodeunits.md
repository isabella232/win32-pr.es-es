---
description: Obtiene un objeto de tipo IMFCollection que contiene objetos RECORDSETSample que contienen unidades de capa de abstracción de red (NALUs) y unidades de información de mejora complementaria (SEI) reenviadas por un descodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2298a29d722c118fb79d5f0b49aa9d3d94fd735150a65772eb15e6da7638445
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713735"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>Atributo MFSampleExtension \_ ForwardedDecodeUnits

Obtiene un objeto de tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contiene objetos [**RECORDSETSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contienen unidades de capa de abstracción de red (NALUs) y unidades de información de mejora complementaria (SEI) reenviadas por un descodificador.

## <a name="data-type"></a>Tipo de datos

**IUnknown**

## <a name="remarks"></a>Comentarios

La colección contiene todas las unidades NALU/SEI personalizadas desde el fotograma anterior con bytes de prevención de emulación quitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




