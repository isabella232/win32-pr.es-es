---
title: Métodos IDCompositionVisual SetClip (Dcomp.h)
description: Establece la propiedad Clip de este objeto visual en la región rectangular o el objeto de recorte especificados.
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- Métodos SetClip DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 1cc1d0f24c30e6ec11ecaa40b0317109eddaf432ee311a5b9545f34f7afa8582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043063"
---
# <a name="idcompositionvisualsetclip-methods"></a>Métodos IDCompositionVisual::SetClip

Establece la propiedad Clip de este objeto visual en la región rectangular o el objeto de recorte especificados. La propiedad Clip restringe la representación del subárbol visual que se basa en este objeto visual a una región rectangular.

### <a name="overload-list"></a>Lista de sobrecarga



| Método                                                                                | Descripción                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip(const D2D \_ RECT \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | Establece la propiedad Clip en la región rectangular especificada.<br/> |
| [**SetClip(IDCompositionClip \* )**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | Establece la propiedad Clip en el objeto de recorte especificado.<br/>        |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 8 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2012 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Dcomp.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Dcomp.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Recorte](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
