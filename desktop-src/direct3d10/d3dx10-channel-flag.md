---
description: Estas marcas las usan las funciones que operan en uno o varios canales de una textura.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: D3DX10_CHANNEL_FLAG enumeración (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566745"
---
# <a name="d3dx10_channel_flag-enumeration"></a>D3DX10 \_ CHANNEL \_ FLAG (enumeración)

Estas marcas las usan las funciones que operan en uno o varios canales de una textura.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 \_ CHANNEL \_ RED**
</dt> <dd>

Indica que se debe usar el canal rojo.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 \_ CHANNEL \_ BLUE**
</dt> <dd>

Indica que se debe usar el canal azul.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 \_ CHANNEL \_ GREEN**
</dt> <dd>

Indica que se debe usar el canal verde.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**CANAL ALFA D3DX10 \_ \_**
</dt> <dd>

Indica que se debe usar el canal alfa.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**LUMINANCE DEL CANAL D3DX10 \_ \_**
</dt> <dd>

Indica que se deben usar las luminosidades de los canales rojo, verde y azul.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




