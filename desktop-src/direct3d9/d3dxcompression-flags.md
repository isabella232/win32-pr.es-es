---
description: Define el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Enumeración D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718266"
---
# <a name="d3dxcompression_flags-enumeration"></a>\_Enumeración de marcas D3DXCOMPRESSION

Define el modo de compresión utilizado para almacenar los datos de conjuntos de animación comprimidos.

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

<span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**\_Valor predeterminado de D3DXCOMPRESS**
</dt> <dd>

Implementa la compresión rápida.

</dd> <dt>

<span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ Strong**
</dt> <dd>

Implementa la compresión lenta. Normalmente da como resultado un conjunto de animaciones comprimidas de mejor calidad que si \_ se usa el valor predeterminado D3DXCOMPRESS.

</dd> <dt>

<span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ forzar \_ DWORD**
</dt> <dd>

Obliga a esta enumeración a compilarse en 32 bits de tamaño. Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits. Este valor no se utiliza.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones de D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




