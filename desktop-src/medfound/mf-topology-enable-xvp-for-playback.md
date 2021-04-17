---
description: Especifica si el cargador de topología habilita el procesador de vídeo de transcodificación (XVP). en el caso de las conversiones, habilitar la conversión de color acelerado de hardware.
title: MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK atributo (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105721409"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a>\_Topología MF \_ habilitar \_ XVP para el \_ atributo de \_ reproducción

Especifica si el cargador de topología habilita el procesador de vídeo de transcodificación (XVP). en el caso de las conversiones, habilitar la conversión de color acelerado de hardware.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

Si se establece este atributo, el cargador de topología incorporará el procesador de vídeo, si es necesario, durante la resolución de topología no transcodificada. Cuando se usa la topología para compilar su propio [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , este atributo indica al cargador que use XVP para las conversiones en lugar del convertidor de color heredado, lo que permite la conversión de color acelerado de hardware. el convertidor de colores heredado es solo software.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Administrador de dispositivos de Direct3D](direct3d-device-manager.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> </dl>

 

 




