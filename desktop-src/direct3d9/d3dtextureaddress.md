---
description: Define constantes que describen los modos de direccionamiento de textura admitidos.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumeración D3DTEXTUREADDRESS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREADDRESS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2cb1893541f80efb9bf85ea444b27bebba5dea29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083712"
---
# <a name="d3dtextureaddress-enumeration"></a>Enumeración D3DTEXTUREADDRESS

Define constantes que describen los modos de direccionamiento de textura admitidos.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DTEXTUREADDRESS { 
  D3DTADDRESS_WRAP         = 1,
  D3DTADDRESS_MIRROR       = 2,
  D3DTADDRESS_CLAMP        = 3,
  D3DTADDRESS_BORDER       = 4,
  D3DTADDRESS_MIRRORONCE   = 5,
  D3DTADDRESS_FORCE_DWORD  = 0x7fffffff
} D3DTEXTUREADDRESS, *LPD3DTEXTUREADDRESS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ Wrap**
</dt> <dd>

Coloque la textura en mosaico en cada unión de enteros. Por ejemplo, para los valores entre 0 y 3, la textura se repite tres veces; no se realiza la creación de reflejo.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**Reflejo de D3DTADDRESS \_**
</dt> <dd>

Similar a D3DTADDRESS \_ Wrap, salvo que la textura se voltea en cada unión de enteros. para los valores entre 0 y 1, por ejemplo, la textura se corrige normalmente; entre 1 y 2, la textura se voltea (reflejada). entre 2 y 3, la textura es normal de nuevo; etc.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**\_Abrazadera D3DTADDRESS**
</dt> <dd>

Las coordenadas de textura fuera del intervalo \[ 0,0, 1,0 \] se establecen en el color de textura en 0,0 o 1,0, respectivamente.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**Borde de D3DTADDRESS \_**
</dt> <dd>

Las coordenadas de textura fuera del intervalo \[ 0,0, 1,0 \] se establecen en el color del borde.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**
</dt> <dd>

Similar a D3DTADDRESS \_ Mirror y D3DTADDRESS \_ Clamp. Toma el valor absoluto de la coordenada de textura (por lo tanto, la creación de reflejo alrededor de 0) y, a continuación, se fija en el valor máximo. El uso más común es para las texturas de volumen, donde la compatibilidad con el modo completo de D3DTADDRESS \_ MIRRORONCE Texture-Addressing no es necesario, pero los datos son simétricos alrededor de un eje.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
