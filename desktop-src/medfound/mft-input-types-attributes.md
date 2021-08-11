---
description: Contiene los tipos de entrada registrados para una Media Foundation transformación (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a750094361cdaa877bff82e20a74c1beae4e1a1f76ea0a9ad5be83f308c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240240"
---
# <a name="mft_input_types_attributes-attribute"></a>Atributo atributos \_ MFT INPUT \_ TYPES \_

Contiene los tipos de entrada registrados para una Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**MFT \_ REGISTER \_ TYPE \_ INFO \[ \] almacenado** como **BYTE \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**a IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentarios

Este atributo se establece en los punteros [**DE TIPO IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Este atributo contiene una matriz de estructuras [**MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que describen uno o varios formatos de entrada admitidos por MFT. Estos valores se toman del registro y están diseñados como una sugerencia para la aplicación. MFT podría admitir formatos adicionales. Para establecer el formato de entrada real, debe crear el MFT y llamar a [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




