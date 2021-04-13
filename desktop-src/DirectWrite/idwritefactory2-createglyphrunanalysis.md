---
title: IDWriteFactory2 CreateGlyphRunAnalysis, método
description: Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Método CreateGlyphRunAnalysis de escritura directa
- Método CreateGlyphRunAnalysis de escritura directa, interfaz IDWriteFactory2
- Interfaz IDWriteFactory2 Direct Write, método CreateGlyphRunAnalysis
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422447"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a>IDWriteFactory2:: CreateGlyphRunAnalysis (método)

Crea un objeto de análisis de ejecución de glifos, que encapsula la información utilizada para representar una ejecución de glifo.

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

*glyphRun* \[ de\]
</dt> <dd>

Tipo: **\* const [**DWRITE \_ \_ ejecución del glifo**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)* _

Estructura que especifica las propiedades de la ejecución del glifo.

</dd> <dt>

_transform * \[ en, opcional\]
</dt> <dd>

Tipo: **const [**DWRITE \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _

Transformación opcional aplicada a los glifos y sus posiciones. Esta transformación se aplica después del ajuste de escala especificado por emSize y pixelsPerDip.

</dd> <dt>

_renderingMode * 
</dt> <dd>

Tipo: **\_ \_ modo de representación DWRITE**

Especifica el modo de representación, que debe ser uno de los modos de representación de tramas (es decir, no tiene valor predeterminado y no contorno).

</dd> <dt>

*measuringMode* 
</dt> <dd>

Tipo: **[ **\_ \_ modo de medición DWRITE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**

Especifica el método para medir glifos.

</dd> <dt>

*gridFitMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ \_ \_ modo de ajuste de cuadrícula**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**

Cómo ajustar el glifo a la cuadrícula. Este no debe ser predeterminado.

</dd> <dt>

*antialiasMode* 
</dt> <dd>

Tipo: **[ **DWRITE \_ \_ \_ modo de suavizado de texto**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**

Especifica el modo antialias.

</dd> <dt>

*baselineOriginX* 
</dt> <dd>

Tipo: **float**

Posición horizontal del origen de la línea base, en DIP.

</dd> <dt>

*baselineOriginY* 
</dt> <dd>

Tipo: **float**

Posición vertical del origen de la línea base, en DIP.

</dd> <dt>

*glyphRunAnalysis* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***

Recibe un puntero al objeto que se acaba de crear.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDWriteFactory2**](idwritefactory2.md)
</dt> </dl>

 

