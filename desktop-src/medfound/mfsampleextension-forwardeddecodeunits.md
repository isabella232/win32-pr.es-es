---
description: Obtiene un objeto de tipo IMFCollection que contiene objetos IMFSample que contienen unidades de capa de abstracción de red (NALUs) e información de mejora adicional (SEI) reenviadas por un descodificador.
ms.assetid: F9FD7959-A78A-4C72-8326-EE8FF9066E6C
title: MFSampleExtension_ForwardedDecodeUnits atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ab5c10a4a7fb4dfd201f9c494c1bc65e14c162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720496"
---
# <a name="mfsampleextension_forwardeddecodeunits-attribute"></a>\_Atributo ForwardedDecodeUnits de MFSampleExtension

Obtiene un objeto de tipo [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) que contiene objetos [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que contienen unidades de capa de abstracción de red (NALUs) e información de mejora adicional (SEI) reenviadas por un descodificador.

## <a name="data-type"></a>Tipo de datos

**IUnknown**

## <a name="remarks"></a>Observaciones

La colección contiene todas las unidades NALU/SEI personalizadas desde el fotograma anterior con bytes de prevención de emulación quitados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




