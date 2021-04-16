---
description: Especifica si el cargador de topología habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: MF_TOPOLOGY_DXVA_MODE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705559"
---
# <a name="mf_topology_dxva_mode-attribute"></a>\_ \_ Atributo de modo DXVA de topología MF \_

Especifica si el cargador de topología habilita la aceleración de vídeo de Microsoft DirectX (DXVA) en la topología.

## <a name="data-type"></a>Tipo de datos

**[**MFTOPOLOGY \_ \_Modo DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

El valor de este atributo es una constante de enumeración del [**\_ \_ modo DXVA de MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) . El valor predeterminado es **MFTOPOLOGY \_ DXVA \_ default**.

Este atributo controla qué MFTs reciben un puntero al administrador de dispositivos de Direct3D. Para habilitar la aceleración de vídeo completa, establezca el valor en **MFTOPOLOGY \_ DXVA \_ Full**. El valor **\_ \_ predeterminado de DXVA MFTOPOLOGY** se define para la compatibilidad con versiones anteriores; coincide con el comportamiento de todas las versiones anteriores de Microsoft Media Foundation.

La constante GUID para este atributo se exporta desde mfuuid. lib.

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

 

 




