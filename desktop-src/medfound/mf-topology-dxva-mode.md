---
description: Especifica si el cargador de topologías habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5462ccf575f94935d100eb70a6d806e139f09762151c2dad8d4e155ca5d1d17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117875746"
---
# <a name="mf_topology_dxva_mode-attribute"></a>Atributo \_ MF TOPOLOGY \_ DXVA \_ MODE

Especifica si el cargador de topologías habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.

## <a name="data-type"></a>Tipo de datos

**[**MFTOPOLOGY \_ MODO DXVA \_ almacenado**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

El valor de este atributo es una constante de [**enumeración MFTOPOLOGY \_ DXVA \_ MODE.**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) El valor predeterminado es **MFTOPOLOGY \_ DXVA \_ DEFAULT.**

Este atributo controla qué MFP reciben un puntero al administrador de dispositivos Direct3D. Para habilitar la aceleración de vídeo completa, establezca el valor en **MFTOPOLOGY \_ DXVA \_ FULL**. El valor **MFTOPOLOGY \_ DXVA \_ DEFAULT** se define por compatibilidad con versiones anteriores; coincide con el comportamiento de todas las versiones anteriores de Microsoft Media Foundation.

La constante GUID para este atributo se exporta desde mfuuid.lib.

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

 

 




