---
description: Contiene los tipos de salida registrados para una Media Foundation transformación (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462785"
---
# <a name="mft_output_types_attributes-attribute"></a>Atributo atributos \_ MFT OUTPUT \_ TYPES \_

Contiene los tipos de salida registrados para una Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**MFT \_ REGISTER \_ TYPE \_ INFO \[ \] almacenado** como **BYTE \[ \]**

## <a name="remarks"></a>Comentarios

Este atributo se establece en los punteros [**DE TIPO IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

Este atributo contiene una matriz de estructuras [**MFT \_ REGISTER TYPE \_ \_ INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) que describen uno o varios formatos de salida admitidos por MFT. Estos valores se toman del registro y están diseñados como una sugerencia para la aplicación. MFT podría admitir formatos adicionales. Para establecer el formato de salida real, debe crear el MFT y llamar a [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

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

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




