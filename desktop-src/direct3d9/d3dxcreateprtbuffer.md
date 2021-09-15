---
description: Crea un búfer de transferencia de radiancia (PRT) precalutado que un simulador puede comprimir o rellenar. Esta función debe usarse para crear búferes por vértice o volumen.
ms.assetid: f79a3691-ab5f-4404-aafd-f9635ff88e71
title: Función D3DXCreatePRTBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8107edfec436d9eda35324f6934b3f70df6a05d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575241"
---
# <a name="d3dxcreateprtbuffer-function"></a>Función D3DXCreatePRTBuffer

Crea un búfer de transferencia de radiancia (PRT) precalutado que un simulador puede comprimir o rellenar. Esta función debe usarse para crear búferes por vértice o volumen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePRTBuffer(
  _In_    UINT            NumSamples,
  _In_    UINT            NumCoeffs,
  _In_    UINT            NumChannels,
  _Inout_ LPD3DXPRTBUFFER *ppBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumSamples* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices (o texeles) muestreados.

</dd> <dt>

*NumCoeffs* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de coeficientes por ubicación de muestra. Cuando se usa prT de armónico esférico (SH), el número de coeficientes debe ser Orderntes, donde Order es el orden de la evaluación de SH. El orden debe estar en el intervalo [de D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. El grado de la evaluación es Order - 1.

</dd> <dt>

*NumChannels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de canales de color que se establecerán en la malla. Establezca en 1 para especificar materiales grises (R = G = B) o 3 para habilitar los efectos de color.

</dd> <dt>

*ppBuffer* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)\***

Dirección de un puntero al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de estos: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Cuando se crea el búfer, todos los valores se inicializan en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
