---
description: Crea una textura de cubo a partir de un recurso especificado por una cadena. Se trata de una función más avanzada que D3DXCreateCubeTextureFromResource.
ms.assetid: 4d263386-8270-4967-8ef5-e9ac69e502a5
title: Función D3DXCreateCubeTextureFromResourceEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCubeTextureFromResourceEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8548863f7c35ff3d56fd83287cf1c3628bb1a9ff89d8ad34346530063c494c99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857305"
---
# <a name="d3dxcreatecubetexturefromresourceex-function"></a>Función D3DXCreateCubeTextureFromResourceEx

Crea una textura de cubo a partir de un recurso especificado por una cadena. Se trata de una función más avanzada que [**D3DXCreateCubeTextureFromResource.**](d3dxcreatecubetexturefromresource.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCubeTextureFromResourceEx(
  _In_    LPDIRECT3DDEVICE9      pDevice,
  _In_    HMODULE                hSrcModule,
  _In_    LPCTSTR                pSrcResource,
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

*hSrcModule* \[ En\]
</dt> <dd>

Tipo: **[ **HMODULE**](../winprog/windows-data-types.md)**

Identificador del módulo donde se encuentra el recurso o **NULL** para el módulo asociado a la imagen que el sistema operativo usó para crear el proceso actual.

</dd> <dt>

*pSrcResource* \[ En\]
</dt> <dd>

Tipo: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Puntero a una cadena que especifica el nombre del recurso. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve como LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*Tamaño* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho y alto de la textura del cubo, en píxeles. Por ejemplo, si la textura del cubo es un cubo de 8 píxeles por 8 píxeles, el valor de este parámetro debe ser 8. Si este valor es 0 o D3DX \_ DEFAULT, las dimensiones se toman del archivo.

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles de mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mip completa.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC. Establecer esta marca en D3DUSAGE RENDERTARGET indica que la superficie se \_ va a usar como destino de representación. A continuación, el recurso se puede pasar al *parámetro pNewRenderTarget* del [**método SetRenderTarget.**](/windows/desktop/api) Si se especifica D3DUSAGE RENDERTARGET, la aplicación debe comprobar que el dispositivo admite esta operación mediante \_ una llamada [**a CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ DYNAMIC indica que la superficie se debe controlar dinámicamente. Para obtener más información sobre el uso de texturas dinámicas, vea [Usar texturas dinámicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura del cubo. La textura de cubo devuelta puede tener un formato diferente del especificado por *Format*. Las aplicaciones deben comprobar el formato de la textura del cubo devuelta. Si [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), el formato se toma del archivo . Si D3DFMT FROM FILE, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo [**enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura del cubo.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios [filtros D3DX \_ ](d3dx-filter.md)que controlan cómo se filtra la imagen. Especificar D3DX DEFAULT para este parámetro equivale a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de uno o varios filtros [D3DX \_ que](d3dx-filter.md) controlan cómo se filtra la imagen. Especificar D3DX \_ DEFAULT para este parámetro equivale a especificar D3DX FILTER \_ \_ BOX.

</dd> <dt>

*ColorKey* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

[**Valor D3DCOLOR**](d3dcolor.md) que se reemplazará por negro transparente o 0 para deshabilitar la clave de color. Siempre es un color ARGB de 32 bits, independientemente del formato de imagen de origen. Alfa es significativo y normalmente debe establecerse en FF para las claves de color opacas. Por lo tanto, para el negro opaco, el valor sería igual a 0xFF000000.

</dd> <dt>

*pSrcInfo* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXIMAGE \_ INFO**](d3dximage-info.md)\***

Puntero a una [**estructura \_ INFO D3DXIMAGE**](d3dximage-info.md) que se va a rellenar con una descripción de los datos en el archivo de imagen de origen o **NULL.**

</dd> <dt>

*pPalette* \[ out\]
</dt> <dd>

Tipo: **[ **PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores para rellenar o **NULL.**

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

La configuración del compilador determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en **D3DXCreateCubeTextureFromResourceExW**. De lo contrario, la llamada de función se resuelve en **D3DXCreateCubeTextureFromResourceExA** porque se usan cadenas ANSI.

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Las texturas de cubo difieren de otras superficies en que son colecciones de superficies. Para llamar a [**SetRenderTarget**](/windows/desktop/api) con una textura de cubo, debe seleccionar una cara individual mediante [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) y pasar la superficie resultante a **SetRenderTarget.**

**D3DXCreateCubeTextureFromResourceEx** usa el formato de archivo de superficie DirectDraw (DDS). El Editor de texturas de DirectX (Dxtex.exe) permite generar un mapa de cubo a partir de otros formatos de archivo y guardarlo en el formato de archivo DDS. Puede obtener información Dxtex.exe y obtener información sobre él desde el SDK de DirectX. Para obtener información sobre el SDK de DirectX, [consulte ¿Dónde está el SDK de DirectX?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3DXCreateCubeTextureFromResource**](d3dxcreatecubetexturefromresource.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
