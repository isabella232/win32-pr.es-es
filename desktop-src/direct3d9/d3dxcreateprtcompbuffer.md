---
description: Crea un búfer de transferencia de Radiance (PRT) comprimido previamente a partir de un objeto ID3DXPRTBuffer no comprimido. Esta función debe usarse con búferes de volumen o por vértices.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: Función D3DXCreatePRTCompBuffer (D3DX9Mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362583"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>D3DXCreatePRTCompBuffer función)

Crea un búfer de transferencia de Radiance (PRT) comprimido previamente a partir de un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) no comprimido. Esta función debe usarse con búferes de volumen o por vértices.

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

*Calidad* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Calidad de la compresión armónica esférica (SH). Vea [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*NumClusters* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de clústeres que se usarán para la compresión.

</dd> <dt>

*NumPCA* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vectores de base del análisis de componentes principales (PCA) que se van a usar en cada clúster.

</dd> <dt>

*pCB* \[ de\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntero opcional a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que se usa para calcular el porcentaje de los cálculos de compresión de PRT completados. La función de devolución de llamada debe implementarse para devolver \_ los valores correctos para seguir ejecutando la rutina de compresión. Cualquier otro valor detendrá la compresión. Puede ser **null**.

</dd> <dt>

*lpUserContext* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero opcional a un valor definido por el usuario que se pasa a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) . Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada. Puede ser **null**.

</dd> <dt>

*pBuffer* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) sin comprimir que se comprimirá.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Dirección de un puntero al objeto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
