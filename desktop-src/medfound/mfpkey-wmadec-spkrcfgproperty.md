---
description: Especifica la configuración de los altavoces en el equipo cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: Propiedad MFPKEY_WMADEC_SPKRCFG (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544782"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>\_ \_ Propiedad SPKRCFG de MFPKEY WMADEC

Especifica la configuración de los altavoces en el equipo cliente.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

No se presupone ninguna configuración específica del orador.

## <a name="remarks"></a>Observaciones

Debe establecer este valor en una de las constantes o valores de la tabla siguiente. Las constantes se definen en Microsoft DirectSound y se enumeran aquí para mayor comodidad. Para resolver estos nombres de constantes para el compilador, debe incluir dsound. h.



| Constante             | Value      | Descripción                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DSSPEAKER \_ DIRECTOUT | 0x00000000 | El audio se pasa directamente, sin tener que configurarse para los altavoces. |
| \_auriculares DSSPEAKER | 0x00000001 | El equipo cliente está equipado con auriculares.                             |
| \_mono DSSPEAKER      | 0x00000002 | El equipo cliente está equipado con un orador monoaural.                    |
| DSSPEAKER \_ cuádruple      | 0x00000003 | El equipo cliente está equipado con altavoces quadraphonic.                  |
| \_estéreo DSSPEAKER    | 0x00000004 | El equipo cliente está equipado con altavoces estéreo.                        |
| \_envolvente DSSPEAKER  | 0x00000005 | El equipo cliente está equipado con altavoces con sonido envolvente de cuatro canales.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | El equipo cliente está equipado con cinco altavoces y un subwoofer.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | El equipo cliente está equipado con siete altavoces y un subwoofer.         |



 

El valor establecido para esta propiedad determina los formatos de salida enumerados por el códec para el audio multicanal.

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

 

 




