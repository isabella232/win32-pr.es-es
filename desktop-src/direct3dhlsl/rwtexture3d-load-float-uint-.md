---
title: Función RWTexture3D::Load(int,uint)
description: Lee los datos de textura y devuelve el estado de la operación. | Función RWTexture3D::Load(int,uint)
ms.assetid: 7BC334D3-217A-454F-B205-A9D7D66B5E99
keywords:
- Carga de la función HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c43649a18ec5935829f56a87fd05e133692da3022539ea736df65a112b23253b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981545"
---
# <a name="rwtexture3dloadintuint-function"></a>Función RWTexture3D::Load(int,uint)

Lee los datos de textura y devuelve el estado de la operación.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in  int  Location,
  out uint Status
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int**

Ubicación de la textura.

</dd> <dt>

*Estado* \[ out\]
</dt> <dd>

Tipo: **uint**

Estado de la operación. No se puede acceder al estado directamente; en su lugar, pase el estado a la función intrínseca [**CheckAccessFullyMapped.**](checkaccessfullymapped.md) **CheckAccessFullyMapped** devuelve **TRUE** si todos los valores de la operación Sample **,** **Gather** o **Load** correspondientes accedieron a iconos asignados en un recurso [en mosaico.](/windows/desktop/direct3d11/direct3d-11-2-features) Si se tomaron valores de un icono no asociado, **CheckAccessFullyMapped** devuelve **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración para el [**objeto RWTexture3D.**](sm5-object-rwtexture3d.md)

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de carga](rwtexture3d-load.md)
</dt> </dl>

 

 
