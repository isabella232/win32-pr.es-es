---
description: Especifica la frecuencia de actualización del monitor.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: MF_TOPOLOGY_PLAYBACK_FRAMERATE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275943"
---
# <a name="mf_topology_playback_framerate-attribute"></a>Atributo de velocidad de reproducción de \_ topología MF \_ \_

Especifica la frecuencia de actualización del monitor.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Para establecer este atributo, llame a [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="applies-to"></a>Se aplica a

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Observaciones

El cargador de topología utiliza este atributo para optimizar la canalización antes de que se inicie la reproducción. Si establece este atributo, establezca también el atributo [de \_ \_ \_ \_ optimizaciones de reproducción estática de la topología MF](mf-topology-static-playback-optimizations.md) en **true**.

La velocidad de fotogramas se expresa como una proporción. Los 32 superiores del valor del atributo contienen el numerador, y los 32 bits inferiores contienen el denominador.

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

[Atributos de topología](topology-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




