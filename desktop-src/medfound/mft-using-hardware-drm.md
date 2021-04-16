---
description: Especifica si IMFTransform usa DRM de hardware.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497764"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ con \_ el \_ atributo DRM de hardware

Especifica si IMFTransform usa DRM de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32** (se trata como **bool**)

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Se aplica a

[**IMTransfrom**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Observaciones

Si un Decrypter de MFT especifica este atributo establecido en 1, se usa DRM de hardware. Si un Decrypter de MFT especifica este atributo establecido en 0, no utiliza DRM de hardware. Si un Decrypter de MFT no especifica este atributo o lo especifica con un valor diferente, no (o no puede) indicar si está usando DRM de hardware.


La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Actualización 2020 de abril de Windows 10   <br/>                                       |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




