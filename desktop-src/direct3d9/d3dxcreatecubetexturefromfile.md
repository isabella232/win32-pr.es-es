---
description: Crea una textura de cubo a partir de un archivo.
ms.assetid: 7ff3b051-568c-4c77-b8a6-b626ba156eb1
title: Función D3DXCreateCubeTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e25b6692fc22eed1695b1d60b019a595826de15af87e4ca70f2610a621abc532
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279895"
---
# <a name="d3dxcreatecubetexturefromfile-function"></a>Función D3DXCreateCubeTextureFromFile

Crea una textura de cubo a partir de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCubeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9      pDevice,
  _In_  LPCTSTR                pSrcFile,
  _Out_ LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.

</dd> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura de cubo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en **D3DXCreateCubeTextureFromFileW**. De lo contrario, la llamada de función se resuelve en **D3DXCreateCubeTextureFromFileA** porque se usan cadenas ANSI.

La función es equivalente a D3DXCreateCubeTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL**, ppCubeTexture).

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria que D3DPOOL \_ MANAGED indica. Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria que indica D3DPOOL \_ DEFAULT.

El filtrado se aplica automáticamente a una textura creada mediante este método. El filtrado es equivalente a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER en [D3DX \_ FILTER](d3dx-filter.md).

**D3DXCreateCubeTextureFromFile** usa el formato de archivo de superficie DirectDraw (DDS). El Editor de texturas de DirectX (Dxtex.exe) permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS. Puede obtener información Dxtex.exe y obtener información al respecto desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3DXCreateCubeTextureFromFileEx**](d3dxcreatecubetexturefromfileex.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
