---
description: La \_ \_ \_ enumeración de enumeraciones de página S0 de MXDC se usa para especificar los tipos de recursos que se pueden asociar a las páginas de los documentos XPS y que se pueden procesar, o pasar sin procesar, el convertidor de documentos XPS de Microsoft (MXDC) a su salida.
ms.assetid: e111d92e-5102-4b39-b311-f9ff1d1a96f1
title: Enumeración MXDC_S0_PAGE_ENUMS (winspool. h)
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
ms.openlocfilehash: 1b4331210027f7fc23f36fb6b9d13a2c232ccbf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909577"
---
# <a name="mxdc_s0_page_enums-enumeration"></a>Enumeración de enumeraciones de \_ Página S0 de MXDC \_ \_

La enumeración de **\_ \_ \_ enumeraciones de página S0 de MXDC** se usa para especificar los tipos de recursos que se pueden asociar a las páginas de los documentos XPS y que se pueden procesar, o pasar sin procesar, el convertidor de documentos XPS de Microsoft (MXDC) a su salida.

## <a name="syntax"></a>Sintaxis


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

<span id="MXDC_RESOURCE_TTF"></span><span id="mxdc_resource_ttf"></span>**\_recurso MXDC \_ ttf**
</dt> <dd>

Fuente TrueType o OpenType.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG"></span><span id="mxdc_resource_jpeg"></span>**MXDC \_ recurso \_ JPEG**
</dt> <dd>

Imagen JPEG

</dd> <dt>

<span id="MXDC_RESOURCE_PNG"></span><span id="mxdc_resource_png"></span>**MXDC de \_ recursos \_ PNG**
</dt> <dd>

Imagen PNG.

</dd> <dt>

<span id="MXDC_RESOURCE_TIFF"></span><span id="mxdc_resource_tiff"></span>**MXDC de \_ recursos \_ TIFF**
</dt> <dd>

Imagen TIFF.

</dd> <dt>

<span id="MXDC_RESOURCE_WDP"></span><span id="mxdc_resource_wdp"></span>**MXDC \_ Resource \_ WDP**
</dt> <dd>

Imagen de Windows Media Photo.

</dd> <dt>

<span id="MXDC_RESOURCE_DICTIONARY"></span><span id="mxdc_resource_dictionary"></span>**\_Diccionario de recursos MXDC \_**
</dt> <dd>

Diccionario de recursos remotos que debe pasarse a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_ICC_PROFILE"></span><span id="mxdc_resource_icc_profile"></span>**\_ \_ perfil ICC de recurso MXDC \_**
</dt> <dd>

Perfil ICC que debe pasarse a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_JPEG_THUMBNAIL"></span><span id="mxdc_resource_jpeg_thumbnail"></span>**MXDC \_ miniatura de recurso \_ JPEG \_**
</dt> <dd>

Miniatura JPEG que se debe pasar a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_PNG_THUMBNAIL"></span><span id="mxdc_resource_png_thumbnail"></span>**MXDC \_ miniatura de recurso \_ PNG \_**
</dt> <dd>

Miniatura PNG que debe pasarse a la salida de MXDC sin procesar.

</dd> <dt>

<span id="MXDC_RESOURCE_MAX"></span><span id="mxdc_resource_max"></span>**\_recurso MXDC \_ máximo**
</dt> <dd>

Recuento máximo de recursos para la validación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta enumeración se utiliza principalmente como el miembro **dwResourceType** de la estructura de [**\_ \_ \_ recursos \_ T S0PAGE de MXDC XPS**](mxdcxpss0pageresource.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                      |
| Encabezado<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |



 

 




