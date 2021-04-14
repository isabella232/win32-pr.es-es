---
title: Enumeración D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Enumeración de D3DX11_CHANNEL_FLAG Direct3D 11
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
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424523"
---
# <a name="d3dx11_channel_flag-enumeration"></a>\_Enumeración de marcas de canal de D3DX11 \_

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Estas marcas las utilizan las funciones que operan en uno o varios canales de una textura.

## <a name="syntax"></a>Sintaxis


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

<span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**\_Canal \_ rojo de D3DX11**
</dt> <dd>

Indica que se debe usar el canal rojo.

</dd> <dt>

<span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**\_Azul canal \_ D3DX11**
</dt> <dd>

Indica que se debe usar el canal azul.

</dd> <dt>

<span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**\_Canal \_ verde de D3DX11**
</dt> <dd>

Indica que se debe usar el canal verde.

</dd> <dt>

<span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**\_Alfa del canal de D3DX11 \_**
</dt> <dd>

Indica que se debe usar el canal alfa.

</dd> <dt>

<span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_Luminancia del canal de D3DX11 \_**
</dt> <dd>

Indica el luminaces de los canales rojo, verde y azul que se deben usar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





