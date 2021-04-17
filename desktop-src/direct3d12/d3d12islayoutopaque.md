---
title: Función D3D12IsLayoutOpaque (D3dx12. h)
description: Indica si el diseño es opaco.
ms.assetid: 43B46A18-A725-4999-BD97-108032793A95
keywords:
- D3D12IsLayoutOpaque función)
topic_type:
- apiref
api_name:
- D3D12IsLayoutOpaque
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971c44688e57dd1081d33a4a077a8dcadcb89abf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707756"
---
# <a name="d3d12islayoutopaque-function"></a>D3D12IsLayoutOpaque función)

Indica si el diseño es opaco.

## <a name="syntax"></a>Sintaxis


```C++
bool inline D3D12IsLayoutOpaque(
   D3D12_TEXTURE_LAYOUT Layout
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Diseño* 
</dt> <dd>

Tipo: **[ **\_ \_ diseño de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout)**

El diseño que se va a comprobar, como un [**\_ \_ diseño de textura D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_layout).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **bool**

Un **booleano** que indica si el diseño es opaco. Un diseño es opaco si es D3D12 \_ \_ diseño de textura \_ desconocido o D3D12 de \_ diseño de textura de \_ \_ 64 KB de SWIZZLE no \_ definidos \_ .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





