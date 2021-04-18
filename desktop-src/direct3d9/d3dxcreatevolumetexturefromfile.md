---
description: Crea una textura de volumen a partir de un archivo.
ms.assetid: e68ac4bb-a89a-41a1-b2ba-40a1ac519e3d
title: Función D3DXCreateVolumeTextureFromFile (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 51ee51f1aee7a69fbd86d7f9bb2ded894dde9ead
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718213"
---
# <a name="d3dxcreatevolumetexturefromfile-function"></a>D3DXCreateVolumeTextureFromFile función)

Crea una textura de volumen a partir de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateVolumeTextureFromFile(
  _In_  LPDIRECT3DDEVICE9        pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _Out_ LPDIRECT3DVOLUMETEXTURE9 *ppVolumeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del volumen.

</dd> <dt>

*pSrcFile* \[ de\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve como LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppVolumeTexture* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Dirección de un puntero a una interfaz [**IDirect3DVolumeTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve como D3DXCreateVolumeTextureFromFileW. De lo contrario, la llamada de función se resuelve como D3DXCreateVolumeTextureFromFileA porque se usan cadenas ANSI.

La función es equivalente a D3DXCreateVolumeTextureFromFileEx (pDevice, pSrcFile, D3DX \_ default, d3dx \_ default, d3dx \_ default, d3dx \_ default, 0, D3DFMT \_ Unknown, D3DPOOL \_ MANaged, d3dx default \_ , d3dx default, \_ 0, **null**, **null**, ppVolumeTexture).

Esta función admite los siguientes formatos de archivo:. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm y. TGA. Consulte [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Las texturas de Mipmapped automáticamente tienen cada nivel rellenado con la textura cargada.

Al cargar imágenes en texturas de mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función. Si esto ocurre, las imágenes deben cargarse manualmente.

Tenga en cuenta que un recurso creado con esta función cuando se llama desde un objeto IDirect3DDevice9 se colocará en la clase de memoria indicada por D3DPOOL \_ administrado. Cuando se llama a este método desde un objeto IDirect3DDevice9Ex, el recurso se colocará en la clase de memoria indicada por el \_ valor predeterminado de D3DPOOL.

El filtrado se aplica automáticamente a una textura creada con este método. El filtrado es equivalente al filtro de D3DX \_ \_ \| del triángulo del filtro de d3dx en el \_ \_ [ \_ filtro de d3dx](d3dx-filter.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3DXCreateVolumeTextureFromFileEx**](d3dxcreatevolumetexturefromfileex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemory**](d3dxcreatevolumetexturefromfileinmemory.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromFileInMemoryEx**](d3dxcreatevolumetexturefromfileinmemoryex.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResource**](d3dxcreatevolumetexturefromresource.md)
</dt> <dt>

[**D3DXCreateVolumeTextureFromResourceEx**](d3dxcreatevolumetexturefromresourceex.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
