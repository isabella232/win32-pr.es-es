---
description: Contiene el nombre para mostrar de una transformación de Media Foundation hardware (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: MFT_FRIENDLY_NAME_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b867db021c43679fef026022bf95bda1186a679eb544465393562b0a51d5d7af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554925"
---
# <a name="mft_friendly_name_attribute-attribute"></a>Atributo MFT \_ FRIENDLY \_ NAME \_

Contiene el nombre para mostrar de una transformación de Media Foundation hardware (MFT).

## <a name="data-type"></a>Tipo de datos

**Wchar\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentarios

Este atributo es compatible con las MTO basadas en hardware. También se establece en los punteros [**DE HECHOActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) asignados por la función [**MFTEnumEx,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) cuando esos punteros representan MFT basados en hardware.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




