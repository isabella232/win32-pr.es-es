---
title: Métodos IDCompositionVisual3 SetTransform (Dcomp. h)
description: Establece la propiedad de transformación de este visual. La propiedad transform especifica una transformación 3D utilizada para modificar el sistema de coordenadas de este visual. La propiedad puede especificar una matriz de transformación de 4 por 4 o un objeto de transformación.
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
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
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714591"
---
# <a name="idcompositionvisual3settransform-methods"></a>IDCompositionVisual3:: SetTransform (métodos)

Establece la propiedad de transformación de este visual. La propiedad transform especifica una transformación 3D utilizada para modificar el sistema de coordenadas de este visual. La propiedad puede especificar una matriz de transformación de 4 por 4 o un objeto de transformación.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                  | Descripción                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform ( \_ matriz D2D \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | Establece la propiedad transform en la matriz de transformación especificada.<br/>      |
| [**SetTransform (IDCompositionTransform3D \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | Establece la propiedad de transformación en el objeto de transformación especificado.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Dcomp. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Dcomp. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

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
