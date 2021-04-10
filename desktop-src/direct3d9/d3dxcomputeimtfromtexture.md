---
description: Calcula el IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las funciones de UVAtlas de D3DX.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Función D3DXComputeIMTFromTexture (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083776"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>D3DXComputeIMTFromTexture función)

Calcula el IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)de D3DX.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*pTexture* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a la textura (vea [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)) que está asignada a la malla.

</dd> <dt>

*dwTextureIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de ajuste de textura. Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado. Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> <dt>

*ppIMTData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta. Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Dada una textura que se asigna a través de la superficie de la malla, el algoritmo calcula el IMT para cada cara. Esto hará que los triángulos que contienen datos de señal de menor frecuencia ocupen menos espacio en el Atlas de textura final cuando se parametrizan con las funciones de UVAtlas. Se supone que la textura se interpola a través de la malla bilinealmente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Usar UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
