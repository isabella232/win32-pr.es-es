---
description: 'DXGI_RGBA estructura: representa un valor de color con alfa, que se usa para la transparencia.'
ms.assetid: 5F9DDDC1-644E-4DA2-8E3D-F157789809E7
title: DXGI_RGBA estructura (DXGItype.h)
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
ms.openlocfilehash: b0447d6470401d4136fbfd36f6d9c089e331b14b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360850"
---
# <a name="dxgi_rgba-structure"></a>Estructura \_ RGBA de DXGI

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



## <a name="members"></a>Members

<dl> <dt>

**r**
</dt> <dd>

Valor de punto flotante que especifica el componente rojo de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente rojo, mientras que un valor de 1,0 indica que el rojo está totalmente presente.

</dd> <dt>

**g**
</dt> <dd>

Valor de punto flotante que especifica el componente verde de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente verde, mientras que un valor de 1,0 indica que el verde está totalmente presente.

</dd> <dt>

**b**
</dt> <dd>

Valor de punto flotante que especifica el componente azul de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica la ausencia completa del componente azul, mientras que un valor de 1,0 indica que el azul está totalmente presente.

</dd> <dt>

**Un**
</dt> <dd>

Valor de punto flotante que especifica el componente alfa de un color. Este valor suele estar en el intervalo de 0,0 a 1,0. Un valor de 0,0 indica totalmente transparente, mientras que un valor de 1,0 indica totalmente opaco.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Puede establecer los miembros de esta estructura en valores fuera del intervalo de 0 a 1 para implementar algunos efectos inusuales. Los valores mayores que 1 producen luces fuertes que tienden a apagar una escena. Los valores negativos producen luces oscuras que realmente quitan la luz de una escena.

El tipo de encabezado DXGItype.h define **DXGI \_ RGBA** como un alias [**de D3DCOLORVALUE**](d3dcolorvalue.md), como se indica a continuación:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Puede usar **DXGI \_ RGBA** con [**IDXGISwapChain1::SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1::GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)y [**DXGI \_ ALPHA \_ MODE**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8 y actualización de plataforma para Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                        |
| Servidor mínimo compatible<br/> | Windows Server 2012 y actualización de plataforma para Windows aplicaciones de escritorio de UWP de Server 2008 R2 \[ \|\]<br/> |
| Encabezado<br/>                   | <dl> <dt>DXGItype.h</dt> </dl>                      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**D3DCOLORVALUE**](d3dcolorvalue.md)
</dt> <dt>

[**D3DCOLORVALUE (en Direct3D 9)**](../direct3d9/d3dcolorvalue.md)
</dt> </dl>

 

 
