---
description: Crea una textura de cubo a partir de un archivo en memoria. Se trata de una función más avanzada que D3DXCreateCubeTextureFromFileInMemory.
ms.assetid: 598016eb-9ea9-4dca-a297-5708a957da6a
title: Función D3DXCreateCubeTextureFromFileInMemoryEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromFileInMemoryEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1401d3a2d9c0e50a39050fcfd89f33c86047073b72b066c3b392dc0e521ae9c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849825"
---
# <a name="d3dxcreatecubetexturefromfileinmemoryex-function"></a>Función D3DXCreateCubeTextureFromFileInMemoryEx

Crea una textura de cubo a partir de un archivo en memoria. Se trata de una función más avanzada que [**D3DXCreateCubeTextureFromFileInMemory.**](d3dxcreatecubetexturefromfileinmemory.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCubeTextureFromFileInMemoryEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    LPCVOID                pSrcData,
  _In_    UINT                   SrcDataSize,
  _In_    UINT                   Size,
  _In_    UINT                   MipLevels,
  _In_    DWORD                  Usage,
  _In_    D3DFORMAT              Format,
  _In_    D3DPOOL                Pool,
  _In_    DWORD                  Filter,
  _In_    DWORD                  MipFilter,
  _In_    D3DCOLOR               ColorKey,
  _Inout_ D3DXIMAGE_INFO         *pSrcInfo,
  _Out_   PALETTEENTRY           *pPalette,
  _Out_   LPDIRECT3DCUBETEXTURE9 *ppCubeTexture
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo que se va a asociar a la textura del cubo.

</dd> <dt>

*pSrcData* \[ En\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntero al archivo en memoria a partir del cual se va a crear la textura del cubo. Vea la sección Comentarios.

</dd> <dt>

*SrcDataSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Tamaño del archivo en memoria, en bytes.

</dd> <dt>

*Tamaño* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho (o alto) en píxeles. Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo.

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mipmap completa.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC. Establecer esta marca en D3DUSAGE RENDERTARGET indica que la superficie se \_ va a usar como destino de representación. A continuación, el recurso se puede pasar al *parámetro pNewRenderTarget* del [**método SetRenderTarget.**](/windows/desktop/api) Si se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación llamando \_ a [**CheckDeviceFormat**](/windows/desktop/api). Para obtener más información sobre el uso de texturas dinámicas, vea [Usar texturas dinámicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura del cubo. La textura devuelta puede tener un formato diferente del especificado por *Format*. Las aplicaciones deben comprobar el formato de la textura devuelta. Si [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), el formato se toma del archivo. Si D3DFMT FROM FILE, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo [**enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura del cubo.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios filtros [D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen. Especificar D3DX DEFAULT para este parámetro equivale a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios filtros [D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen. Especificar D3DX \_ DEFAULT para este parámetro equivale a especificar D3DX FILTER \_ \_ BOX. Además, use los bits 27-31 para especificar el número de niveles de mip que se omitirán (desde la parte superior de la cadena mipmap) cuando se cargue una textura .dds en la memoria; esto le permite omitir hasta 32 niveles.

</dd> <dt>

*ColorKey* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR que**](d3dcolor.md) se reemplazará por negro transparente o 0 para deshabilitar la clave de color. Siempre es un color ARGB de 32 bits, independientemente del formato de imagen de origen. Alfa es significativo y normalmente debe establecerse en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos del archivo de imagen de origen, o **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores para rellenar, o **NULL.** Vea la sección Comentarios.

</dd> <dt>

*ppCubeTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DCUBETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DCubeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dcubetexture9) que representa el objeto de textura de cubo creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Las texturas de cubo difieren de otras superficies en que son colecciones de superficies. Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget.**

Este método está diseñado para usarse para cargar archivos de imagen almacenados como RT RCDATA, que es un recurso definido por la aplicación \_ (datos sin procesar). De lo contrario, se producirá un error en este método.

Para más información sobre [**PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)consulte el SDK de plataforma. Tenga en cuenta que a partir de DirectX 8.0, el miembro peFlags de la estructura **PALETTEENTRY** no funciona como se documenta en el SDK de plataforma. El miembro peFlags es ahora el canal alfa para los formatos de 8 bits.

**D3DXCreateCubeTextureFromFileInMemoryEx** usa el formato de archivo de superficie DirectDraw (DDS). El Editor de texturas de DirectX (Dxtex.exe) permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS. Puede obtener Dxtex.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

Al omitir los niveles de asignación mip al cargar un archivo .dds, use la macro D3DX SKIP DDS MIP LEVELS para generar el \_ \_ valor de \_ \_ MipFilter. Esta macro toma el número de niveles que se omitirán y el tipo de filtro y devuelve el valor del filtro, que se pasará al parámetro MipFilter.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
