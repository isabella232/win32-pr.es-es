---
description: Define el tipo de luz.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumeración D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707936"
---
# <a name="d3dlighttype-enumeration"></a>Enumeración D3DLIGHTTYPE

Define el tipo de luz.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**\_Punto D3DLIGHT**
</dt> <dd>

Light es un origen de punto. La luz tiene una posición en el espacio y irradia la luz en todas las direcciones.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_**
</dt> <dd>

Light es un origen de Spotlight. Esta luz es como una luz puntual, salvo que la iluminación está limitada a un cono. Este tipo de luz tiene una dirección y otros parámetros que determinan la forma del cono que produce. Para obtener información sobre estos parámetros, consulte la estructura [**D3DLIGHT9**](d3dlight9.md) .

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**\_Direccional D3DLIGHT**
</dt> <dd>

Light es una fuente de luz direccional. Esto es equivalente a usar una fuente de luz puntual a una distancia infinita.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las luces direccionales son ligeramente más rápidas que las fuentes de luz puntual, pero las luces puntuales parecen un poco mejor. Los Spotlight ofrecen efectos visuales interesantes, pero consumen mucho tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




