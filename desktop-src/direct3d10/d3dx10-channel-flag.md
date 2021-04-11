---
description: Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumeración D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362726"
---
# <a name="d3dx10_channel_flag-enumeration"></a>\_Enumeración de marcas de canal de D3DX10 \_

Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.

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

<span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**\_Canal \_ rojo de D3DX10**
</dt> <dd>

Indica que se debe usar el canal rojo.

</dd> <dt>

<span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**\_Azul canal \_ D3DX10**
</dt> <dd>

Indica que se debe usar el canal azul.

</dd> <dt>

<span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**\_Canal \_ verde de D3DX10**
</dt> <dd>

Indica que se debe usar el canal verde.

</dd> <dt>

<span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**\_Alfa del canal de D3DX10 \_**
</dt> <dd>

Indica que se debe usar el canal alfa.

</dd> <dt>

<span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminancia del canal de D3DX10 \_**
</dt> <dd>

Indica el luminaces de los canales rojo, verde y azul que se deben usar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




