---
description: Especifica la frecuencia de actualización del monitor.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: MF_TOPOLOGY_PLAYBACK_FRAMERATE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361152"
---
# <a name="mf_topology_playback_framerate-attribute"></a>Atributo \_ FRAMERATE DE \_ REPRODUCCIÓN DE TOPOLOGÍA \_ MF

Especifica la frecuencia de actualización del monitor.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

El cargador de topologías usa este atributo para optimizar la canalización antes de que se inicie la reproducción. Si establece este atributo, establezca también el atributo [ \_ MF TOPOLOGY STATIC PLAYBACK \_ \_ \_ OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) en **TRUE.**

La velocidad de fotogramas se expresa como una relación. Los 32 bits superiores del valor del atributo contienen el numerador y los 32 bits inferiores contienen el denominador.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de topología](topology-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




