---
description: Estas marcas proporcionan información adicional sobre los parámetros de efecto.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718273"
---
# <a name="d3dx_parameter"></a>\_Parámetro D3DX

Estas marcas proporcionan información adicional sobre los parámetros de efecto.

[**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)usa las constantes de parámetro Effect.



| Constante                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <dt>**\_Anotación del parámetro D3DX \_**</dt> </dl> | Este parámetro se marca como una anotación. Consulte [Agregar información a los parámetros de efectos con anotaciones](using-an-effect.md).<br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <dt>**\_Literal de parámetro de D3DX \_**</dt> </dl>          | Este parámetro se marca como un valor literal. Los parámetros literales no pueden cambiar después de la compilación, lo que permite al compilador optimizar su uso. Los parámetros compartidos no se pueden marcar como literal. Vea [usos y literales (Direct3D 9)](usages-and-literals.md). <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <dt>**Parámetro de D3DX \_ \_ compartido**</dt> </dl>             | Todos los efectos del mismo espacio de nombres compartirán el valor de un parámetro. Cambiar el valor de un efecto lo cambiará en todos los efectos compartidos. Consulte [uso compartido de parámetros](cloning-and-sharing.md). **D3DX \_ Los parámetros \_ compartidos** no se pueden combinar con el **literal de \_ parámetro \_ de d3dx** o la **\_ \_ anotación de parámetro d3dx**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de efecto](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




