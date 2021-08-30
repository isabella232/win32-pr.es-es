---
description: Define constantes que describen los modos de direccionamiento de textura admitidos.
ms.assetid: 5c03c55f-4a74-4b0e-ba05-e4a6582ff47c
title: Enumeración D3DTEXTUREADDRESS (D3D9Types.h)
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
ms.openlocfilehash: 0ad5fad2699eac272c8abc173af47402130ecaafc918921cdef7717ccdab2095
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069415"
---
# <a name="d3dtextureaddress-enumeration"></a>D3DTEXTUREADDRESS (enumeración)

Define constantes que describen los modos de direccionamiento de textura admitidos.

## <a name="syntax"></a>Syntax


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

<span id="D3DTADDRESS_WRAP"></span><span id="d3dtaddress_wrap"></span>**D3DTADDRESS \_ WRAP**
</dt> <dd>

Mosaico de la textura en cada unión de entero. Por ejemplo, para los valores entre 0 y 3, la textura se repite tres veces; no se realiza ninguna creación de reflejo.

</dd> <dt>

<span id="D3DTADDRESS_MIRROR"></span><span id="d3dtaddress_mirror"></span>**D3DTADDRESS \_ MIRROR**
</dt> <dd>

Es similar a D3DTADDRESS WRAP, salvo que la textura \_ se volteará en cada unión de entero. para los valores entre 0 y 1, por ejemplo, la textura se aborda normalmente; entre 1 y 2, la textura se voltear (reflejada); entre 2 y 3, la textura vuelve a ser normal; y así sucesivamente.

</dd> <dt>

<span id="D3DTADDRESS_CLAMP"></span><span id="d3dtaddress_clamp"></span>**D3DTADDRESS \_ CLAMP**
</dt> <dd>

Las coordenadas de textura fuera del intervalo 0,0, 1,0 se establecen en el color de textura en \[ \] 0,0 o 1,0, respectivamente.

</dd> <dt>

<span id="D3DTADDRESS_BORDER"></span><span id="d3dtaddress_border"></span>**BORDE \_ D3DTADDRESS**
</dt> <dd>

Las coordenadas de textura fuera \[ del intervalo 0,0, 1,0 \] se establecen en el color del borde.

</dd> <dt>

<span id="D3DTADDRESS_MIRRORONCE"></span><span id="d3dtaddress_mirroronce"></span>**D3DTADDRESS \_ MIRRORONCE**
</dt> <dd>

Similar a D3DTADDRESS \_ MIRROR y D3DTADDRESS \_ CLAMP. Toma el valor absoluto de la coordenada de textura (por lo tanto, la creación de reflejo alrededor de 0) y, a continuación, fija al valor máximo. El uso más común es para las texturas de volumen, donde la compatibilidad con el modo de direccionamiento de textura D3DTADDRESS MIRRORONCE completo no es necesaria, pero los datos son simétricos alrededor de un \_ eje.

</dd> <dt>

<span id="D3DTADDRESS_FORCE_DWORD"></span><span id="d3dtaddress_force_dword"></span>**D3DTADDRESS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara con un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)
</dt> </dl>

 

 
