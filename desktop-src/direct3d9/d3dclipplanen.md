---
description: Define patrones de bits que habilitan los planos de recorte definidos por el usuario. Estas macros se definen como una comodidad al establecer valores para el estado de representación \_ CLIPPLANEENABLE de D3DRS.
ms.assetid: 5bca2401-a3fb-4b1c-bb59-621b15da10f1
title: Macro D3DCLIPPLANEn (D3D9Types.h)
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
ms.openlocfilehash: 315f1cdd8f8835b869f04edd9869243f3e05a9c2c9a08a41eeffc014727b3fc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805472"
---
# <a name="d3dclipplanen-macro"></a>Macro D3DCLIPPLANEn

Define patrones de bits que habilitan los planos de recorte definidos por el usuario. Estas macros se definen como una comodidad al establecer valores para el estado de representación \_ CLIPPLANEENABLE de D3DRS.

## <a name="syntax"></a>Sintaxis


```C++
void D3DCLIPPLANEn(void);
```



## <a name="parameters"></a>Parámetros

Esta macro no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta macro no devuelve un valor.

## <a name="remarks"></a>Comentarios

Los planos de recorte definidos por el usuario se habilitan cuando el valor establecido en el estado de representación CLIPPLANEENABLE de D3DRS contiene uno o varios bits de conjunto \_ (es decir, no es 0). El valor del estado de representación no es importante; el sistema no interpreta el valor como un número. En su lugar, el valor habilita el plano de recorte cuyo bit correspondiente está establecido. El bit 0 controla el estado del primer plano de recorte (en el índice 0), el bit 1 el segundo plano, y así sucesivamente.

Los patrones de bits que crean estas macros se pueden combinar mediante una operación LÓGICA OR para habilitar simultáneamente varios planos de recorte. Si se omite una de estas macros de la combinación, se deshabilita eficazmente el plano de recorte en ese índice.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> </dl>

 

 




