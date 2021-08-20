---
description: Especifica si el cargador de topologías habilita el procesador de vídeo transcodificador (XVP). para conversiones, habilitando la conversión de color acelerada por hardware.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK atributo (Mfidl.h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: 3f315463ce1719617c5a48066401219f4b971f0a555cadf2af43b055a2b0e9a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875745"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>ATRIBUTO \_ ENABLE \_ \_ XVP \_ FOR \_ PLAYBACK DE LA TOPOLOGÍA MF

Especifica si el cargador de topologías habilita el procesador de vídeo transcodificador (XVP). para conversiones, habilitando la conversión de color acelerada por hardware.

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

Si se establece este atributo, el cargador de topologías extraerá el procesador de vídeo, si es necesario, durante la resolución de la topología sin transcodificación. Cuando se usa la topología para crear su propio [ELEMENTO DETOPOLOGY,](/windows/win32/api/mfidl/nn-mfidl-imftopology) este atributo indica al cargador que use XVP para las conversiones en lugar del convertidor de colores heredado, lo que permite la conversión de color acelerada por hardware. el convertidor de colores heredado es de solo software.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D Administrador de dispositivos](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




