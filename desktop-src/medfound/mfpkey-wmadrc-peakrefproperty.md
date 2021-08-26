---
description: Especifica el nivel de volumen más alto que se produce en el contenido de audio.
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: MFPKEY_WMADRC_PEAKREF (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58013ba116b9217ad6c16c93e420a09872cd887c4d5068f7c5b5dd68bf013377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953464"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>Propiedad MFPKEY \_ WMADRC \_ PEAKREF

Especifica el nivel de volumen más alto que se produce en el contenido de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Comentarios

Puede obtener este valor del codificador después de procesar el contenido. Este valor también se puede establecer en el descodificador para el control de intervalo dinámico.

Para obtener más información sobre el control de intervalo dinámico, vea el artículo web [Windows Media Audio Professional Codec Features](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
