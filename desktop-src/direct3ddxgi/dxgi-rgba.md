---
description: Representa un valor de color con alfa, que se usa para la transparencia.
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA estructura (DXGItype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_RGBA
api_type:
- HeaderDef
api_location:
- DXGItype.h
ms.openlocfilehash: 77b526e916d43868304c6c01a7dbbe8ebbb5692b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806224"
---
# <a name="dxgi_rgba-structure"></a>DXGI \_ rgba (estructura)

Representa un valor de color con alfa, que se usa para la transparencia.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DXGI_RGBA {
  float r;
  float g;
  float b;
  float a;
} DXGI_RGBA;
```



## <a name="members"></a>Miembros

<dl> <dt>

**r**
</dt> <dd>

Valor de punto flotante que especifica el componente rojo de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.

</dd> <dt>

**g**
</dt> <dd>

Valor de punto flotante que especifica el componente verde de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el color verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Valor de punto flotante que especifica el componente azul de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.

</dd> <dt>

**un**
</dt> <dd>

Valor de punto flotante que especifica el componente alfa de un color. Normalmente, este valor está en el intervalo comprendido entre 0,0 y 1,0. Un valor de 0,0 indica que es completamente transparente, mientras que un valor de 1,0 indica que es totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales. Los valores mayores que 1 producen luces fuertes que tienden a lavar una escena. Los valores negativos producen luces oscuras que realmente quitan la luz de una escena.

El tipo de encabezado DXGItype. h: define la **DXGI \_ RGBA** como un alias de [**D3DCOLORVALUE**](d3dcolorvalue.md), como se indica a continuación:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Puede usar **DXGI \_ RGBA** con [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)y el [**\_ \_ modo alfa de dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 y actualización de plataforma para aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \[ \|\]<br/>                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 y la actualización de plataforma para aplicaciones de \[ UWP de aplicaciones de escritorio de Windows server 2008 R2 \|\]<br/> |
| Encabezado<br/>                   | <dl> <dt>DXGItype. h</dt> </dl>                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (en Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
