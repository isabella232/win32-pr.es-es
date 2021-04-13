---
description: Representa un valor de color con alfa, que se usa para la transparencia.
ms.assetid: 27A86A10-FC0E-421E-BEA7-2DEB539849BB
title: Estructura D3DCOLORVALUE (Dxgitype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOLORVALUE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b7d768af9e471f3183c6a400622c2b0e0719a2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362551"
---
# <a name="d3dcolorvalue-structure-dxgitypeh"></a>Estructura D3DCOLORVALUE (Dxgitype. h)

Representa un valor de color con alfa, que se usa para la transparencia.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DCOLORVALUE {
  float r;
  float g;
  float b;
  float a;
} D3DCOLORVALUE;
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

El tipo de encabezado DXGItype. h: define la [**DXGI \_ RGBA**](dxgi-rgba.md) como un alias de **D3DCOLORVALUE**, como se indica a continuación:


```
typedef D3DCOLORVALUE DXGI_RGBA;
```



Puede usar D3DCOLORVALUE o [**dxgi \_ RGBA**](dxgi-rgba.md) con [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor), [**IDXGISwapChain1:: GetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)y el [**\_ \_ modo alfa de dxgi**](/windows/desktop/api/DXGI1_2/ne-dxgi1_2-dxgi_alpha_mode).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Dxgitype. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DXGI](d3d10-graphics-reference-dxgi-structures.md)
</dt> <dt>

[**RGBA de DXGI \_**](dxgi-rgba.md)
</dt> </dl>

 

 




