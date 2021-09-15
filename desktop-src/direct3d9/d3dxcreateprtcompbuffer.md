---
description: Crea un búfer de transferencia de base precalutada (PRT) comprimido a partir de un objeto ID3DXPRTBuffer sin comprimir. Esta función debe usarse con búferes por vértice o volumen.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Función D3DXCreatePRTCompBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575236"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>Función D3DXCreatePRTCompBuffer

Crea un búfer de transferencia de base precalutada (PRT) comprimido a partir de un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) sin comprimir. Esta función debe usarse con búferes por vértice o volumen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Calidad* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Calidad de compresión armónica esférica (SH). Vea [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de clústeres que se usarán para la compresión.

</dd> <dt>

*NumPCA* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vectores de base de análisis de componentes principales (PCA) que se usarán en cada clúster.

</dd> <dt>

*pCB* \[ En\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntero opcional a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que se usa para calcular el porcentaje de cálculos de compresión PRT completados. La función de devolución de llamada debe implementarse para devolver S \_ OK para seguir ejecutando la rutina de compresión. Cualquier otro valor detendrá la compresión. Puede ser **NULL.**

</dd> <dt>

*lpUserContext* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero opcional a un valor definido por el usuario pasado a la función de devolución de llamada [LPD3DXSHPRTSIMCB.](lpd3dxshprtsimcb.md) Normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada. Puede ser **NULL.**

</dd> <dt>

*pBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) sin comprimir que se comprimirá.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Dirección de un puntero al objeto [**ID3DXPRTCompBuffer de**](id3dxprtcompbuffer.md) salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
