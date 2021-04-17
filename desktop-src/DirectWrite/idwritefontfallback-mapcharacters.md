---
title: IDWriteFontFallback MapCharacters, método
description: Determina la fuente adecuada que se va a utilizar para representar el intervalo de texto inicial.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Método MapCharacters de escritura directa
- Método MapCharacters de escritura directa, interfaz IDWriteFontFallback
- Interfaz IDWriteFontFallback Direct Write, método MapCharacters
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359765"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>IDWriteFontFallback:: MapCharacters (método)

Determina la fuente adecuada que se va a utilizar para representar el intervalo de texto inicial.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*de origen* 
</dt> <dd>

Tipo: **[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _

La implementación de origen de texto contiene el texto y la configuración regional.

</dd> <dt>

_textPosition * 
</dt> <dd>

Tipo: **UINT32**

Posición inicial que se va a analizar.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Longitud del texto que se va a analizar.

</dd> <dt>

*baseFontCollection* \[ en, opcional\]
</dt> <dd>

Tipo: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _

Colección de fuentes predeterminada que se va a usar.

</dd> <dt>

_baseFamilyName * \[ en, opcional\]
</dt> <dd>

Tipo: **const WCHAR \_ t \** _

Nombre de familia de la fuente base. Si pasa null, no se realizará ninguna coincidencia con la familia.

</dd> <dt>

_baseWeight * 
</dt> <dd>

Tipo: **[ **DWRITE \_ \_ espesor de fuente**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Peso deseado.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Tipo: **[ **\_ \_ estilo de fuente DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

El estilo deseado.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Tipo: **[ **DWRITE \_ Font \_ Stretch**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Stretch deseado.

</dd> <dt>

*mappedLength* \[ enuncia\]
</dt> <dd>

Tipo: **UINT32 \** _

Longitud de texto asignada a la fuente asignada. Siempre será menor o igual que la longitud del texto y mayor que cero (si la longitud del texto es distinta de cero), por lo que el autor de la llamada avanza al menos un carácter.

</dd> <dt>

_mappedFont * \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Fuente que se debe usar para representar los primeros caracteres *mappedLength* del texto. Si devuelve NULL, significa que ninguna fuente puede representar el texto y *mappedLength* es el número de caracteres que se va a omitir (se representa con un glifo que falta).

</dd> <dt>

*escala* \[ enuncia\]
</dt> <dd>

Tipo: **float \** _

Factor de escala para multiplicar el tamaño em de la fuente devuelta por.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

