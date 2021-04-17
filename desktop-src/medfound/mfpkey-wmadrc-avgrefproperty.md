---
description: Especifica el nivel de volumen medio del contenido de audio.
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: Propiedad MFPKEY_WMADRC_AVGREF (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf18c37b00f84cc3ae3fdf1f44b2fbefcc56d9f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666781"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>\_ \_ Propiedad AVGREF de MFPKEY WMADRC

Especifica el nivel de volumen medio del contenido de audio.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="remarks"></a>Observaciones

Puede obtener este valor desde el codificador una vez procesado el contenido. Este valor también se puede establecer en el descodificador para el control de intervalo dinámico, pero solo tendrá efecto si se establece la propiedad [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) .

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

 

 
