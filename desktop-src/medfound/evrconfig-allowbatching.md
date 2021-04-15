---
description: Permite que el representador de vídeo mejorado (EVR) procese llamadas por lotes en el método reenviado de Microsoft Direct3D IDirect3DDevice9::P.
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: EVRConfig_AllowBatching atributo (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191c3c0f0ea4ad18e7bb711ae6d37c21f75cd478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539549"
---
# <a name="evrconfig_allowbatching-attribute"></a>\_Atributo AllowBatching de EVRConfig

Permite que el representador de vídeo mejorado (EVR) procese llamadas por lotes en el método reenviado de Microsoft Direct3D **IDirect3DDevice9::P** .

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, utilice **QueryInterface** para consultar el receptor de medios EVR de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ ALLOWBATCHING** en EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obtener una descripción de esta marca.

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

 

 




