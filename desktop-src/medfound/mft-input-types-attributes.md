---
description: Contiene los tipos de entrada registrados para una transformación de Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: MFT_INPUT_TYPES_Attributes atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543915"
---
# <a name="mft_input_types_attributes-attribute"></a>\_Atributo de \_ atributos de tipos de entrada de MFT \_

Contiene los tipos de entrada registrados para una transformación de Media Foundation (MFT).

## <a name="data-type"></a>Tipo de datos

**MFT \_ Registrar \_ \_ información \[ de \] tipo** almacenada como **byte \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Observaciones

Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Este atributo contiene una matriz de estructuras de información de tipo de registro de MFT que describen uno o más formatos de entrada admitidos por la MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) Estos valores se toman del registro y están pensados como una sugerencia para la aplicación. La MFT podría admitir formatos adicionales. Para establecer el formato de entrada real, debe crear la MFT y llamar a [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

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

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




