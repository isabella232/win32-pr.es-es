---
description: Especifica el tamaño de la ventana de destino para la reproducción de vídeo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: MF_TOPOLOGY_PLAYBACK_MAX_DIMS atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98575a32b1d68414cb4d94a547273aa4986e03dc707023d5c40f9860b77b5a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604785"
---
# <a name="mf_topology_playback_max_dims-attribute"></a>Atributo DIMS MAX DE REPRODUCCIÓN DE TOPOLOGÍA \_ \_ \_ \_ MF

Especifica el tamaño de la ventana de destino para la reproducción de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a MFGetAttributeSize.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)

Para establecer este atributo, llame a [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Comentarios

El cargador de topologías usa este atributo para optimizar la canalización antes de que se inicie la reproducción. Si establece este atributo, establezca también el atributo [ \_ MF TOPOLOGY STATIC PLAYBACK \_ \_ \_ OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) en **TRUE.**

Los 32 bits superiores del valor del atributo contienen el ancho y los 32 bits inferiores contienen el alto, ambos en píxeles.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




