---
title: Método IDWriteFontFallback MapCharacters
description: Determina una fuente adecuada que se usará para representar el intervalo inicial de texto.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Escritura directa del método MapCharacters
- Método MapCharacters direct write , idWriteFontFallback (interfaz)
- IdWriteFontFallback interface Direct Write , Método MapCharacters
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
ms.openlocfilehash: 99f18932121d44f61d67c8124faa2d26638035bdcff473ad26c4222ceea9a85b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048795"
---
# <a name="idwritefontfallbackmapcharacters-method"></a>Método IDWriteFontFallback::MapCharacters

Determina una fuente adecuada que se usará para representar el intervalo inicial de texto.

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

Tipo: **[ **IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\***

La implementación del origen de texto contiene el texto y la configuración regional.

</dd> <dt>

*textPosition* 
</dt> <dd>

Tipo: **UINT32**

Posición inicial para analizar.

</dd> <dt>

*textLength* 
</dt> <dd>

Tipo: **UINT32**

Longitud del texto que se analizará.

</dd> <dt>

*baseFontCollection* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\***

Colección de fuentes predeterminada que se usará.

</dd> <dt>

*baseFamilyName* \[ in, opcional\]
</dt> <dd>

Tipo: **const wchar \_ t \***

Nombre de familia de la fuente base. Si pasa null, no se realizará ninguna coincidencia con la familia.

</dd> <dt>

*baseWeight* 
</dt> <dd>

Tipo: **[ **DWRITE \_ FONT \_ WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**

Peso deseado.

</dd> <dt>

*baseStyle* 
</dt> <dd>

Tipo: **[ **ESTILO DE \_ FUENTE DWRITE \_**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**

Estilo deseado.

</dd> <dt>

*baseStretch* 
</dt> <dd>

Tipo: **[ **DWRITE \_ FONT \_ STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**

Ajuste deseado.

</dd> <dt>

*mappedLength* \[ out\]
</dt> <dd>

Tipo: **UINT32 \***

Longitud del texto asignado a la fuente asignada. Siempre será menor o igual que la longitud del texto y mayor que cero (si la longitud del texto es distinto de cero), por lo que el autor de la llamada avanza al menos un carácter.

</dd> <dt>

*mappedFont* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***

Fuente que se debe usar para representar los primeros *caracteres asignados del* texto. Si devuelve NULL, significa que ninguna fuente puede representar el texto y *mappedLength* es el número de caracteres que se omitirán (representados con un glifo que falta).

</dd> <dt>

*escala* \[ out\]
</dt> <dd>

Tipo: **\* FLOAT**

Factor de escala por el que se multiplica el tamaño em de la fuente devuelta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                 |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

