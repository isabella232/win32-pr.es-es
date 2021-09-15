---
description: Estas marcas proporcionan información adicional sobre los parámetros de efecto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575261"
---
# <a name="d3dx_parameter"></a>PARÁMETRO \_ D3DX

Estas marcas proporcionan información adicional sobre los parámetros de efecto.

[**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)usa constantes de parámetro de efecto.



| Constante                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**ANOTACIÓN DE \_ PARÁMETROS D3DX \_**</dt> </dl> | Este parámetro se marca como una anotación. Vea [Agregar información para hacer efecto a los parámetros con anotaciones](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**LITERAL DE PARÁMETRO D3DX \_ \_**</dt> </dl>          | Este parámetro se marca como un valor literal. Los parámetros literales no pueden cambiar después de la compilación, lo que permite al compilador optimizar su uso. Los parámetros compartidos no se pueden marcar como literales. Vea [Usages and Literals (Direct3D 9) (Usos y literales [Direct3D 9]).](usages-and-literals.md) <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**PARÁMETRO D3DX \_ \_ COMPARTIDO**</dt> </dl>             | Todos los efectos del mismo espacio de nombres compartirán el valor de un parámetro. Cambiar el valor en un efecto lo cambiará en todos los efectos compartidos. Consulte [Uso compartido de parámetros](cloning-and-sharing.md). **D3DX \_ PARAMETER \_ SHARED no** se puede combinar con **D3DX \_ PARAMETER \_ LITERAL** o **D3DX \_ PARAMETER \_ ANNOTATION**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes de efecto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




