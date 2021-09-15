---
description: Fuerza al representador de vídeo mejorado (EVR) a procesar por lotes las llamadas al método IDirect3D9Device::P resent.
ms.assetid: d7523000-baa0-4011-97e1-d1ffe7263d01
title: EVRConfig_ForceBatching atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6dff5d7a5e90377c8749519033b6a66ef7663a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573416"
---
# <a name="evrconfig_forcebatching-attribute"></a>Atributo ForceBatching de EVRConfig \_

Fuerza al representador de vídeo mejorado (EVR) a procesar por lotes las llamadas al [**método IDirect3D9Device::P resent.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **QueryInterface para** consultar el receptor de medios EVR para la [**interfaz DEATTRIBUTES.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la **marca \_ ForceBatching MFVideoRenderPrefs** en la EVR. Vea [**MFVideoRenderPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) obtener una descripción de esta marca.

La constante GUID para este atributo se exporta desde strmiids.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 \[ aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos evr](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 
