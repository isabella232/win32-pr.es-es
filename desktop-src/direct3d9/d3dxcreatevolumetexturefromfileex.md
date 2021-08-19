---
description: 'Función D3DXCreateVolumeTextureFromFileEx: crea una textura de volumen a partir de un archivo.'
ms.assetid: fa11706a-83cc-4795-957d-6d0e1faf2a8f
title: Función D3DXCreateVolumeTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateVolumeTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 47d46f2472bf9c055814ed575584a087dc5922dc104fcbb3a49b2a2b2a93a958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731894"
---
# <a name="d3dxcreatevolumetexturefromfileex-function"></a>Función D3DXCreateVolumeTextureFromFileEx

Crea una textura de volumen a partir de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateVolumeTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9        pDevice,
  _In_    LPCTSTR                  pSrcFile,
  _In_    UINT                     Width,
  _In_    UINT                     Height,
  _In_    UINT                     Depth,
  _In_    UINT                     MipLevels,
  _In_    DWORD                    Usage,
          D3DFORMAT                Format,
  _In_    D3DPOOL                  Pool,
  _In_    DWORD                    Filter,
  _In_    DWORD                    MipFilter,
  _In_    D3DCOLOR                 ColorKey,
  _Inout_ D3DXIMAGE_INFO           *pSrcInfo,
  _Out_   PALETTEENTRY             *pPalette,
  _Out_   LPDIRECT3DVOLUMETEXTURE9 *ppTexture
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

Puntero a una cadena que especifica el nombre de archivo. Si la configuración del compilador requiere Unicode, el tipo de datos LPCTSTR se resuelve en LPCWSTR. De lo contrario, el tipo de datos de cadena se resuelve en LPCSTR. Vea la sección Comentarios.

</dd> <dt>

*Ancho* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Ancho en píxeles. Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Alto* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Alto, en píxeles. Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*Profundidad* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Profundidad, en píxeles. Si este valor es cero o D3DX \_ DEFAULT, las dimensiones se toman del archivo. La dimensión máxima que admite un controlador (para el ancho, el alto y la profundidad) se puede encontrar en MaxVolumeExtent en [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mipmap completa.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, D3DUSAGE \_ RENDERTARGET o D3DUSAGE \_ DYNAMIC. Establecer esta marca en D3DUSAGE RENDERTARGET indica que la superficie se \_ va a usar como destino de representación. A continuación, el recurso se puede pasar al *parámetro pNewRenderTarget* del [**método SetRenderTarget.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) Si se especifica D3DUSAGE RENDERTARGET o D3DUSAGE DYNAMIC, pool debe establecerse en D3DPOOL DEFAULT y la aplicación debe comprobar que el dispositivo admite esta operación mediante una llamada a \_ \_  \_ [**CheckDeviceFormat**](/windows/desktop/api). D3DUSAGE \_ DYNAMIC indica que la superficie se debe controlar dinámicamente. Para obtener más información sobre el uso de texturas dinámicas, vea [Usar texturas dinámicas.](performance-optimizations.md)

</dd> <dt>

*Format* 
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura. La textura devuelta puede tener un formato diferente del especificado por *Format*. Las aplicaciones deben comprobar el formato de la textura devuelta. Si [D3DFMT \_ UNKNOWN](other-d3dx-constants.md), el formato se toma del archivo. Si D3DFMT FROM FILE, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del tipo [**enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura.

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

Puntero a una [**estructura PALETTEENTRY,**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) que representa una paleta de 256 colores para rellenar, o **NULL.**

</dd> <dt>

*ppTexture* \[ out\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVOLUMETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DVolumeTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolumetexture9) que representa el objeto de textura creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada a la función se resuelve en D3DXCreateVolumeTextureFromFileExW. De lo contrario, la llamada de función se resuelve en D3DXCreateVolumeTextureFromFileExA porque se usan cadenas ANSI.

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Las texturas mipmapped rellenan automáticamente cada nivel con la textura de volumen cargada. Al cargar imágenes en texturas mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función. Si esto sucede, las imágenes deben cargarse manualmente.

Al omitir los niveles de asignación mip al cargar un archivo .dds, use la macro D3DX SKIP DDS MIP LEVELS para generar el \_ \_ valor de \_ \_ *MipFilter.* Esta macro toma el número de niveles que se omitirán y el tipo de filtro y devuelve el valor del filtro, que se pasará al *parámetro MipFilter.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3DXCreateVolumeTextureFromFile**](d3dxcreatevolumetexturefromfile.md)
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

 

 
