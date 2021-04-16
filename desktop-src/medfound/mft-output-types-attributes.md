---
description: Contiene los tipos de salida registrados para una transformación de Media Foundation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: MFT_OUTPUT_TYPES_Attributes atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705898"
---
# <a name="mft_output_types_attributes-attribute"></a>\_Atributo de \_ atributos de tipos de salida de MFT \_

Contiene los tipos de salida registrados para una transformación de Media Foundation (MFT).

## <a name="data-type"></a>Tipo de datos

**MFT \_ Registrar \_ \_ información \[ de \] tipo** almacenada como **byte \[ \]**

## <a name="remarks"></a>Observaciones

Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Este atributo contiene una matriz de estructuras de información de tipo de registro de MFT que describen uno o más formatos de salida admitidos por la MFT. [**\_ \_ \_**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) Estos valores se toman del registro y están pensados como una sugerencia para la aplicación. La MFT podría admitir formatos adicionales. Para establecer el formato de salida real, debe crear la MFT y llamar a [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

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

 

 




