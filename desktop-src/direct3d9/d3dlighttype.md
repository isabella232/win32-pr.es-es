---
description: Define el tipo de luz.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumeración D3DLIGHTTYPE (D3D9Types.h)
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
ms.openlocfilehash: 66aefec5d614e5fc51f82741fbb30ace71222997273b7647c0bf51f2d5038878
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804780"
---
# <a name="d3dlighttype-enumeration"></a>D3DLIGHTTYPE (enumeración)

Define el tipo de luz.

## <a name="syntax"></a>Syntax


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

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**D3DLIGHT \_ POINT**
</dt> <dd>

La luz es un origen de punto. La luz tiene una posición en el espacio y emite luz en todas las direcciones.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**D3DLIGHT \_ SPOT**
</dt> <dd>

La luz es un origen destacado. Esta luz es como una luz de punto, salvo que la iluminación se limita a un cono. Este tipo de luz tiene una dirección y otros parámetros que determinan la forma del cono que genera. Para obtener información sobre estos parámetros, vea la [**estructura D3DLIGHT9.**](d3dlight9.md)

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**D3DLIGHT \_ DIRECTIONAL**
</dt> <dd>

La luz es una fuente de luz direccional. Esto equivale a usar una fuente de luz de punto a una distancia infinita.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las luces direccionales son ligeramente más rápidas que las fuentes de luz de punto, pero tienen un aspecto un poco mejor. Los contenidos destacados ofrecen efectos visuales interesantes, pero consumen mucho tiempo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




