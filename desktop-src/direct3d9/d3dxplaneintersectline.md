---
description: 'Función D3DXPlaneIntersectLine (D3dx9math.h): busca la intersección entre un plano y una línea.'
ms.assetid: 2723cd3e-fdc3-4aab-a089-0089e5b14e3e
title: Función D3DXPlaneIntersectLine (D3dx9math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPlaneIntersectLine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a9b89508079b0b400135f4ae39fd6fdfaed61952
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098073"
---
# <a name="d3dxplaneintersectline-function-d3dx9mathh"></a>Función D3DXPlaneIntersectLine (D3dx9math.h)

Busca la intersección entre un plano y una línea.

## <a name="syntax"></a>Sintaxis


```C++
D3DXVECTOR3* D3DXPlaneIntersectLine(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_    const D3DXPLANE   *pP,
  _In_    const D3DXVECTOR3 *pV1,
  _In_    const D3DXVECTOR3 *pV2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3,**](d3dxvector3.md) que identifica la intersección entre el plano y la línea especificados.

</dd> <dt>

*pP* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXPLANE**](d3dxplane.md) \***

Puntero a la estructura [**D3DXPLANE de**](d3dxplane.md) origen.

</dd> <dt>

*pV1* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen, definiendo un punto inicial de línea.

</dd> <dt>

*pV2* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Puntero a una estructura [**D3DXVECTOR3 de**](d3dxvector3.md) origen, definiendo un punto final de línea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a una [**estructura D3DXVECTOR3**](d3dxvector3.md) que es la intersección entre el plano y la línea especificados.

## <a name="remarks"></a>Comentarios

Si la línea es paralela al plano, **se devuelve NULL.**

El valor devuelto para esta función es el mismo valor devuelto en el *parámetro pOut.* De esta manera, la **función D3DXPlaneIntersectLine** se puede usar como parámetro para otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 




