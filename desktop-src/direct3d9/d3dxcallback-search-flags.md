---
description: Marcas usadas para obtener información de devolución de llamada.
ms.assetid: e8126ff0-db23-4da6-a999-0efb8c2647da
title: Enumeración D3DXCALLBACK_SEARCH_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCALLBACK_SEARCH_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: d3302b79734557a5c1f2082ec2a4e95c03790f4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083742"
---
# <a name="d3dxcallback_search_flags-enumeration"></a>\_Enumeración de marcas de búsqueda de D3DXCALLBACK \_

Marcas usadas para obtener información de devolución de llamada.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum D3DXCALLBACK_SEARCH_FLAGS { 
  D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION  = 1,
  D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION     = 2,
  D3DXCALLBACK_SEARCH_FORCE_DWORD                 = 0x7fffffff
} D3DXCALLBACK_SEARCH_FLAGS, *LPD3DXCALLBACK_SEARCH_FLAGS;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXCALLBACK_SEARCH_EXCLUDING_INITIAL_POSITION"></span><span id="d3dxcallback_search_excluding_initial_position"></span>**D3DXCALLBACK \_ búsqueda \_ excluyendo la \_ \_ posición inicial**
</dt> <dd>

Excluya las devoluciones de llamada ubicadas en la posición inicial de la búsqueda.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_BEHIND_INITIAL_POSITION"></span><span id="d3dxcallback_search_behind_initial_position"></span>**D3DXCALLBACK \_ Buscar \_ detrás de la \_ \_ posición inicial**
</dt> <dd>

Invertir la dirección de búsqueda de devolución de llamada.

</dd> <dt>

<span id="D3DXCALLBACK_SEARCH_FORCE_DWORD"></span><span id="d3dxcallback_search_force_dword"></span>**D3DXCALLBACK \_ de \_ forzar búsqueda en \_ DWORD**
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

 

 




