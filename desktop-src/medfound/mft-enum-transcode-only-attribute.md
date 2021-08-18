---
description: Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0951d4f370849678eb88ecbd9751c417a7e50d2bd709ad1f2c5b6cf96f5f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973084"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>Atributo MFT \_ ENUM \_ TRANSCODE \_ ONLY \_ ATTRIBUTE

Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.

Actualmente, este atributo solo se aplica a los descodificadores basados en hardware que usan el mini controlador AVStream. El atributo se almacena en el registro en la información de funcionalidades del descodificador. Para obtener más información, vea la documentación de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Normalmente, las aplicaciones no usan este atributo.

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Comentarios

Si esta entrada del Registro está presente y es igual a 1, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) omite el descodificador a menos que el autor de la llamada haya especificado la marca **\_ MFT ENUM \_ FLAG \_ TRANSCODE \_ ONLY** en **MFTEnumEx**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
