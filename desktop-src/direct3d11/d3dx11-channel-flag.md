---
title: D3DX11_CHANNEL_FLAG enumeración (D3DX11tex.h)
description: 'Nota: La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Estas marcas las usan las funciones que operan en uno o varios canales de una textura.'
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- D3DX11_CHANNEL_FLAG enumeración Direct3D 11
- LPD3DX11_CHANNEL_FLAG puntero de enumeración Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45f8142d34235a151638e1043928521666f2d1751319ee785d22b92004a14421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028315"
---
# <a name="d3dx11_channel_flag-enumeration"></a>D3DX11 \_ CHANNEL \_ FLAG (enumeración)

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Estas marcas las usan las funciones que operan en uno o varios canales de una textura.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 \_ CHANNEL \_ RED**
</dt> <dd>

Indica que se debe usar el canal rojo.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 \_ CHANNEL \_ BLUE**
</dt> <dd>

Indica que se debe usar el canal azul.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11 \_ CHANNEL \_ GREEN**
</dt> <dd>

Indica que se debe usar el canal verde.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**CANAL ALFA D3DX11 \_ \_**
</dt> <dd>

Indica que se debe usar el canal alfa.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**LUMINANCE DEL CANAL D3DX11 \_ \_**
</dt> <dd>

Indica que se deben usar las luminosidades de los canales rojo, verde y azul.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





