---
description: Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.
ms.assetid: 0e05cb05-87a8-4174-a3c6-a0a0c7765024
title: MFT_ENUM_TRANSCODE_ONLY_ATTRIBUTE atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fa3349da254534605178995d493f63525a81489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423851"
---
# <a name="mft_enum_transcode_only_attribute-attribute"></a>Atributo \_ de \_ atributo de solo Metacode de enumeración de MFT \_ \_

Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.

Actualmente, este atributo solo se aplica a los descodificadores basados en hardware que usan el controlador de AVStream. El atributo se almacena en el registro en la información de capacidades del descodificador. Para obtener más información, consulte la documentación de [**IGetCapabilitiesKey**](/windows/win32/api/strmif/nn-strmif-igetcapabilitieskey).

Normalmente, las aplicaciones no usan este atributo.

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

Si esta entrada del registro está presente y es igual a 1, la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) omite el descodificador, a menos que el autor de la llamada haya especificado la marca de **enumeración de MFT \_ \_ \_ \_ solo Transcode** Flag en **MFTEnumEx**.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)
</dt> </dl>

 

 
