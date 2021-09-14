---
description: Crea una textura a partir de un archivo.
ms.assetid: 247b0ee2-ee31-4090-b94c-41951b46675f
title: Función D3DXCreateTextureFromFile (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 19453986405ee4d46a3e72145c2117bb113663bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969812"
---
# <a name="d3dxcreatetexturefromfile-function"></a>Función D3DXCreateTextureFromFile

Crea una textura a partir de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateTextureFromFile(
  _In_  LPDIRECT3DDEVICE9  pDevice,
  _In_  LPCTSTR            pSrcFile,
  _Out_ LPDIRECT3DTEXTURE9 *ppTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura.

</dd> <dt>

*pSrcFile* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateTextureFromFileW. De lo contrario, la llamada de función se resuelve en D3DXCreateTextureFromFileA porque se usan cadenas ANSI.

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

La función es equivalente a D3DXCreateTextureFromFileEx(pDevice, pSrcFile, D3DX \_ DEFAULT, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, D3DFMT \_ UNKNOWN, D3DPOOL \_ MANAGED, D3DX \_ DEFAULT, D3DX \_ DEFAULT, 0, **NULL,** **NULL**, ppTexture).

Las texturas mipmapped rellenan automáticamente cada nivel con la textura cargada.

Al cargar imágenes en texturas mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función. Si esto sucede, las imágenes deben cargarse manualmente.

Tenga en cuenta que un recurso creado con esta función se colocará en la clase de memoria que indica D3DPOOL \_ MANAGED.

El filtrado se aplica automáticamente a una textura creada mediante este método. El filtrado es equivalente a D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER en [D3DX \_ FILTER](d3dx-filter.md).

Para obtener el mejor rendimiento cuando se **usa D3DXCreateTextureFromFile**:

1.  El escalado de imágenes y la conversión de formato en tiempo de carga pueden ser lentos. Almacene las imágenes en el formato y la resolución que se usarán. Si el hardware de destino requiere potencia de dos dimensiones, cree y almacene imágenes con la potencia de dos dimensiones.
2.  Considere la posibilidad de usar archivos de superficie de DirectDraw (DDS). Dado que los archivos DDS se pueden usar para representar cualquier formato de textura de Direct3D 9, son muy fáciles de leer para D3DX. Además, pueden almacenar mapas mip, por lo que cualquier algoritmo de generación de mapas mip se puede usar para crear las imágenes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
