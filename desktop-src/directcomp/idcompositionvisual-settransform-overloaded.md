---
title: Métodos IDCompositionVisual SetTransform (Dcomp.h)
description: Establece la propiedad Transform de este objeto visual. La propiedad Transform especifica una transformación 2D que se usa para modificar el sistema de coordenadas de este objeto visual. La propiedad puede especificar una matriz de transformación 3 por 2 o un objeto de transformación.
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- Métodos SetTransform DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b38c2e8fce2f0687b78b65574858a38bba681c6bc1174cab13dfa254e3b186c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281252"
---
# <a name="idcompositionvisualsettransform-methods"></a>Métodos IDCompositionVisual::SetTransform

Establece la propiedad Transform de este objeto visual. La propiedad Transform especifica una transformación 2D que se usa para modificar el sistema de coordenadas de este objeto visual. La propiedad puede especificar una matriz de transformación 3 por 2 o un objeto de transformación.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                                    | Descripción                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform(D2D \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | Establece la propiedad Transform en la matriz de transformación especificada.<br/>      |
| [**SetTransform(IDCompositionTransform \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | Establece la propiedad Transform en el objeto de transformación especificado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 8 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2012 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
