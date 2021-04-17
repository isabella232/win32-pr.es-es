---
description: Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: Propiedad MFPKEY_WMADRC_PEAKREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e91df613541f91f2efd2fd71ea38d7b1ca9a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696687"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>\_ \_ Propiedad PEAKREF de MFPKEY WMADRC

Especifica el nivel de volumen más alto que tiene lugar en el contenido de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede obtener este valor desde el codificador una vez procesado el contenido. Este valor también se puede establecer en el descodificador para el control de intervalo dinámico.

Para obtener más información sobre el control de intervalo dinámico, vea el artículo Web [Windows Media Audio características de códecs profesionales](/previous-versions/ms867218(v=msdn.10)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
