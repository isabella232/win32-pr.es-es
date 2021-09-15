---
description: Define el modo de compresión utilizado para almacenar datos comprimidos del conjunto de animaciones.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: D3DXCOMPRESSION_FLAGS enumeración (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569349"
---
# <a name="d3dxcompression_flags-enumeration"></a>Enumeración D3DXCOMPRESSION \_ FLAGS

Define el modo de compresión utilizado para almacenar datos comprimidos del conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ PREDETERMINADO**
</dt> <dd>

Implementa la compresión rápida.

</dd> <dt>

<span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ STRONG**
</dt> <dd>

Implementa la compresión lenta. Normalmente, da como resultado un conjunto de animación comprimido de mejor calidad que si se usa D3DXCOMPRESS \_ DEFAULT.

</dd> <dt>

<span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ FORCE \_ DWORD**
</dt> <dd>

Fuerza esta enumeración a compilar hasta 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




