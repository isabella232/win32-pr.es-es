---
description: Alllows el representador de vídeo mejorado (EVR) para mezclar el vídeo dentro de un rectángulo que sea menor que el rectángulo de salida y, a continuación, escale el resultado.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: EVRConfig_AllowScaling atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1d0662c7145d9f5c5484df81c2483305402850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907564"
---
# <a name="evrconfig_allowscaling-attribute"></a>\_Atributo AllowScaling de EVRConfig

Alllows el representador de vídeo mejorado (EVR) para mezclar el vídeo dentro de un rectángulo que sea menor que el rectángulo de salida y, a continuación, escale el resultado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, utilice **QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ ALLOWSCALING** en EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obtener una descripción de esta marca.

La constante GUID para este atributo se exporta desde strmiids. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




