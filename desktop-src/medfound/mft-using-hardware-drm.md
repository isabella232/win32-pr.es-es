---
description: Especifica si EL ELEMENTO IMFTransform usa DRM de hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473556"
---
# <a name="mft_using_hardware_drm-attribute"></a>Atributo MFT \_ USING \_ HARDWARE \_ DRM

Especifica si EL ELEMENTO IMFTransform usa DRM de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32** (tratado como **BOOL)**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Comentarios

Si un descifrador MFT especifica este atributo establecido en 1, usa DRM de hardware. Si un descifrador MFT especifica este atributo establecido en 0, no usa DRM de hardware. Si un descifrador MFT no especifica este atributo o lo especifica con un valor diferente, no indica (o no puede) indicar si usa DRM de hardware.


La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10 Actualización de abril de 2020   <br/>                                       |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




