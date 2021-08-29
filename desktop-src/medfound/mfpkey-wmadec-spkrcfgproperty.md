---
description: Especifica la configuración del hablante en el equipo cliente.
ms.assetid: a0353e70-0741-4705-95e0-e76ebd8ba977
title: MFPKEY_WMADEC_SPKRCFG propiedad (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4ebe2d15390a09629d4afaeb7a558fd6c87c82e23954aecf9bb9763f8815fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953465"
---
# <a name="mfpkey_wmadec_spkrcfg-property"></a>Propiedad MFPKEY \_ WMADEC \_ SPKRCFG

Especifica la configuración del hablante en el equipo cliente.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACSpeakerConfig

## <a name="data-type"></a>Tipo de datos

**VT \_ UI4**

## <a name="default-value"></a>Valor predeterminado

No se supone ninguna configuración específica del hablante.

## <a name="remarks"></a>Comentarios

Debe establecer este valor en una de las constantes o valores de la tabla siguiente. Las constantes se definen en Microsoft Direct Sound y se enumeran aquí para mayor comodidad. Para resolver estos nombres constantes para el compilador, debe incluir d sound.h.



| Constante             | Value      | Descripción                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| DIRECTOUT de DSSPEAKER \_ | 0x00000000 | El audio se pasa directamente, sin estar configurado para los altavoces. |
| DSSPEAKER \_ PARA LA INSERTE | 0x00000001 | El equipo cliente está equipado con auriculares.                             |
| DSSPEAKER \_ MONO      | 0x00000002 | El equipo cliente está equipado con un altavoz monoaural.                    |
| DSSPEAKER \_ QUAD      | 0x00000003 | El equipo cliente está equipado con altavoces cuadráticos.                  |
| DSSPEAKER \_ STEREO    | 0x00000004 | El equipo cliente está equipado con altavoces estéreo.                        |
| DSSPEAKER \_ SURROUND  | 0x00000005 | El equipo cliente está equipado con altavoces de sonido envolvente de cuatro canales.   |
| DSSPEAKER \_ 5POINT1   | 0x00000006 | El equipo cliente está equipado con cinco altavoces y un altavoz.          |
| DSSPEAKER \_ 7POINT1   | 0x00000007 | El equipo cliente está equipado con siete altavoces y un altavoz.         |



 

El valor establecido para esta propiedad determina los formatos de salida enumerados por el códec para el audio multicanal.

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

 

 




