---
description: Crea una textura de cubo a partir de un archivo en memoria.
ms.assetid: f7e99d5a-5479-4f0b-b040-bb07e7e37666
title: Función D3DXCreateCubeTextureFromFileInMemory (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f1d6de3fba0dcbda959a2811ec665ebc4a6541c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721476"
---
# <a name="d3dxcreatecubetexturefromfileinmemory-function"></a>D3DXCreateCubeTextureFromFileInMemory función)

Crea una textura de cubo a partir de un archivo en memoria.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemory(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  UINT                   SrcDataSize,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.

</dd> <dt>

*pSrcData* \[ de\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al archivo en la memoria desde el que se va a crear el mapa. Vea la sección Comentarios.

</dd> <dt>

*SrcDataSize* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Tamaño del archivo en memoria, en bytes.

</dd> <dt>

*ppCubeTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Dirección de un puntero a una interfaz [**IDirect3DCubeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura del cubo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

La función es equivalente a D3DXCreateCubeTextureFromFileInMemoryEx (pDevice, pSrcData, SrcDataSize, D3DX \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ Managed, d3dx \_ default, D3dx \_ default, 0, **null**, **null**, ppCubeTexture).

Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado. Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.

Este método se ha diseñado para que se use para cargar archivos de imagen almacenados como RT \_ RCDATA, que es un recurso definido por la aplicación (datos sin procesar). De lo contrario, se producirá un error en este método.

El filtrado se aplica automáticamente a una textura creada con este método. El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).

**D3DXCreateCubeTextureFromFileInMemory** usa el formato de archivo de DirectDraw Surface (DDS). El editor de texturas de DirectX (Dxtex.exe) le permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS. Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, vea [¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
