---
title: Función RWTexture1D::Load(int)
description: Lee los datos de textura. | Función RWTexture1D::Load(int)
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: f8d502d6e4fd1f13355c17fbd1ef9c42b3c6de2ec5aa20176aec562af807dd3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981625"
---
# <a name="rwtexture1dloadint-function"></a>Función RWTexture1D::Load(int)

Lee los datos de textura.

## <a name="syntax"></a>Sintaxis


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ubicación* \[ En\]
</dt> <dd>

Tipo: **int**

Ubicación de la textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Escriba:

El tipo de valor devuelto coincide con el tipo de la declaración del [**objeto RWTexture1D.**](sm5-object-rwtexture1d.md)

## <a name="remarks"></a>Comentarios

Esta función es compatible con los siguientes tipos de sombreadores:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Métodos de carga](rwtexture1d-load.md)
</dt> </dl>

 

 




