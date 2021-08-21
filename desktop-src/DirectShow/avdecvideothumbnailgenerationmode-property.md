---
description: Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propiedad AVDecVideoThumbnailGenerationMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb10b4996a88c8d2e62180edcbfaba8f71b6738d7dc7e3019a0b8ee4b44462d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159996"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propiedad AVDecVideoThumbnailGenerationMode

Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Comentarios

Si el valor es **VARIANT \_ TRUE,** el descodificador usa una configuración optimizada para generar imágenes en miniatura rápidamente. (Por ejemplo, podría omitir fotogramas B o P). De lo contrario, si el valor es **VARIANT \_ FALSE,** el descodificador usa su configuración de descodificación normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




