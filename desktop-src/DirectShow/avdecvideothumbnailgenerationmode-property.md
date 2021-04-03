---
description: Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.
ms.assetid: c640d915-585b-481d-aa49-0d4a559d291c
title: Propiedad AVDecVideoThumbnailGenerationMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa2a9c8b095c0fdb0d44a5a12fdfe954b89ba49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997997"
---
# <a name="avdecvideothumbnailgenerationmode-property"></a>Propiedad AVDecVideoThumbnailGenerationMode

Habilita o deshabilita el modo de generación de miniaturas en un descodificador de vídeo.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecVideoThumbnailGenerationMode**

## <a name="remarks"></a>Observaciones

Si el valor es **Variant \_ true**, el descodificador usa una configuración optimizada para generar imágenes en miniatura rápidamente. (Por ejemplo, puede omitir los fotogramas B o P). De lo contrario, si el valor es **Variant \_ false**, el descodificador usa su configuración de descodificación normal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 2000 Professional \|\]<br/>                     |
| Servidor mínimo compatible<br/> | Aplicaciones \[ para UWP de aplicaciones de escritorio de Windows 2000 Server \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**Interfaz ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




