---
description: Especifica la configuración del hablante en el equipo cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05ed96e4f722c1b3bd7c98178cd7f93a6c2e01df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468616"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>Propiedad MFPKEY \_ WMADEC \_ SPKRCFG

Especifica la configuración del hablante en el equipo cliente.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

No se supone ninguna configuración específica del hablante.

## <a name="remarks"></a>Observaciones

Debe establecer este valor en una de las constantes o valores de la tabla siguiente. Las constantes se definen en Microsoft DirectSound y se enumeran aquí para mayor comodidad. Para resolver estos nombres constantes para el compilador, debe incluir dsound.h.



| Constante             | Value      | Descripción                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DIRECTOUT DE DSSPEAKER \_ | 0x00000000 | El audio se pasa directamente, sin configurarse para los altavoces. |
| DSSPEAKER \_ DE LA CAJA DE SEGURIDAD | 0x00000001 | El equipo cliente está equipado con cascos.                             |
| DSSPEAKER \_ MONO      | 0x00000002 | El equipo cliente está equipado con un altavoz monoaural.                    |
| DSSPEAKER \_ QUAD      | 0x00000003 | El equipo cliente está equipado con altavoces cuadráticos.                  |
| DSSPEAKER \_ STEREO    | 0x00000004 | El equipo cliente está equipado con altavoces estéreo.                        |
| ENTORNO DE DSSPEAKER \_  | 0x00000005 | El equipo cliente está equipado con altavoces de sonido envolvente de cuatro canales.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | El equipo cliente está equipado con cinco altavoces y un altavoz.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | El equipo cliente está equipado con siete altavoces y un altavoz.         |



 

El valor establecido para esta propiedad determina los formatos de salida enumerados por el códec para el audio multicanal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




