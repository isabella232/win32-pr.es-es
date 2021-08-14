---
description: La enumeración MXDC S0 PAGE ENUMS se usa para especificar tipos de recursos que se pueden asociar a páginas de documentos XPS y que microsoft \_ \_ XPS Document Converter (MXDC) puede procesar o pasar sin procesar a su \_ salida.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: MXDC_S0_PAGE_ENUMS enumeración (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0_PAGE_ENUMS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 3aa6622ea65e00c1447e6042a41c998e9ab30a29d1172d43e1a1da81feb34c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471343"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Enumeración MXDC \_ S0 \_ PAGE \_ ENUMS

La enumeración **MXDC \_ S0 \_ PAGE \_ ENUMS** se usa para especificar tipos de recursos que se pueden asociar a páginas de documentos XPS y que microsoft XPS Document Converter (MXDC) puede procesar o pasar sin procesar a su salida.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMxdcS0PageEnums { 
  MXDC_RESOURCE_TTF,
  MXDC_RESOURCE_JPEG,
  MXDC_RESOURCE_PNG,
  MXDC_RESOURCE_TIFF,
  MXDC_RESOURCE_WDP,
  MXDC_RESOURCE_DICTIONARY,
  MXDC_RESOURCE_ICC_PROFILE,
  MXDC_RESOURCE_JPEG_THUMBNAIL,
  MXDC_RESOURCE_PNG_THUMBNAIL,
  MXDC_RESOURCE_MAX
} MXDC_S0_PAGE_ENUMS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**TTF DE \_ RECURSOS \_ DE MXDC**
</dt> <dd>

Fuente TrueType o OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ RESOURCE \_ JPEG**
</dt> <dd>

Imagen JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC \_ RESOURCE \_ PNG**
</dt> <dd>

Imagen PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC \_ RESOURCE \_ TIFF**
</dt> <dd>

Imagen TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**WDP del \_ RECURSO \_ MXDC**
</dt> <dd>

Windows Imagen de foto multimedia.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**DICCIONARIO DE RECURSOS DE MXDC \_ \_**
</dt> <dd>

Diccionario de recursos remotos que se debe pasar a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**PERFIL DE MXDC \_ RESOURCE \_ ICC \_**
</dt> <dd>

Perfil DE TASA QUE se debe pasar a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MINIATURA JPEG \_ DE RECURSOS \_ DE MXDC \_**
</dt> <dd>

Miniatura JPEG que se debe pasar a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MINIATURA PNG \_ DE RECURSOS \_ DE MXDC \_**
</dt> <dd>

Miniatura PNG que se debe pasar a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**MXDC \_ RESOURCE \_ MAX**
</dt> <dd>

Número máximo de recursos para la validación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta enumeración se usa principalmente como miembro **dwResourceType** de la estructura [**MXDC \_ XPS \_ S0PAGE \_ RESOURCE \_ T.**](mxdcxpss0pageresource.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |



 

 




