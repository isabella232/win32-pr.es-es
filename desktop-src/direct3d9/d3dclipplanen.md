---
description: Define los patrones de bits que habilitan los planos de recorte definidos por el usuario. Estas macros se definen como una comodidad cuando se establecen valores para el \_ Estado de representación de D3DRS CLIPPLANEENABLE.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPPLANEn
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 4508f1654a357eb80b3847b7562e230c6a9be4d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424355"
---
# <a name="d3dclipplanen-macro"></a>D3DCLIPPLANEn (macro)

Define los patrones de bits que habilitan los planos de recorte definidos por el usuario. Estas macros se definen como una comodidad cuando se establecen valores para el \_ Estado de representación de D3DRS CLIPPLANEENABLE.

## <a name="syntax"></a>Sintaxis


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los planos de recorte definidos por el usuario se habilitan cuando el valor establecido en el estado de representación de D3DRS \_ CLIPPLANEENABLE contiene uno o varios bits de conjunto (es decir, no es 0). El valor del estado de representación no es importante; el sistema no interpreta el valor como un número. En su lugar, el valor habilita el plano de recorte cuyo bit correspondiente está establecido. Bit 0 controla el estado del primer plano de recorte (en el índice 0), el bit 1 el segundo plano, etc.

Los patrones de bits creados por estas macros se pueden combinar mediante una operación OR lógica para habilitar simultáneamente varios planos de recorte. Si se omite una de estas macros de la combinación, se deshabilita de manera eficaz el plano de recorte en dicho índice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




