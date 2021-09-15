---
title: Método IDWriteFactory2 CreateGlyphRunAnalysis
description: Crea un objeto de análisis de ejecución de glifo, que encapsula la información utilizada para representar una ejecución de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Método CreateGlyphRunAnalysis de escritura directa
- Método CreateGlyphRunAnalysis direct write , interfaz IDWriteFactory2
- Método CreateGlyphRunAnalysis de la interfaz IDWriteFactory2
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476940"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>Método IDWriteFactory2::CreateGlyphRunAnalysis

Crea un objeto de análisis de ejecución de glifo, que encapsula la información utilizada para representar una ejecución de glifo.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*glyphRun* \[ En\]
</dt> <dd>

Tipo: **const [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \***

Estructura que especifica las propiedades de la ejecución del glifo.

</dd> <dt>

*transformación* \[ en, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***

Transformación opcional aplicada a los glifos y sus posiciones. Esta transformación se aplica después del escalado especificado por emSize y pixelsPerDip.

</dd> <dt>

*renderingMode* 
</dt> <dd>

Tipo: **DWRITE \_ RENDERING \_ MODE**

Especifica el modo de representación, que debe ser uno de los modos de representación de trama (es decir, no predeterminado y no esquema).

</dd> <dt>

*measuringMode* 
</dt> <dd>

Tipo: **[ **MODO DE \_ MEDICIÓN DE \_ DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Especifica el método para medir glifos.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ GRID \_ FIT \_ MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Cómo ajustar a la cuadrícula los contornos del glifo. Debe ser no predeterminado.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ TEXT \_ ANTIALIAS \_ MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Especifica el modo antialias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **FLOAT**

Posición horizontal del origen de línea base, en DIP.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Tipo: **FLOAT**

Posición vertical del origen de línea base, en DIP.

</dd> <dt>

*glyphRunAnalysis* \[ out\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Recibe un puntero al objeto recién creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| para aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

