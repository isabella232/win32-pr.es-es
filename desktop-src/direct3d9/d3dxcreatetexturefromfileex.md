---
description: Crea una textura a partir de un archivo. Se trata de una función más avanzada que D3DXCreateTextureFromFile.
ms.assetid: 820bbd77-98af-4051-a22e-825fa4dd87d8
title: Función D3DXCreateTextureFromFileEx (D3dx9tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureFromFileEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4dba1424f98389a9282fdebf9dae55c7e1601f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969811"
---
# <a name="d3dxcreatetexturefromfileex-function"></a>Función D3DXCreateTextureFromFileEx

Crea una textura a partir de un archivo. Se trata de una función más avanzada que [**D3DXCreateTextureFromFile.**](d3dxcreatetexturefromfile.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateTextureFromFileEx(
  _In_    LPDIRECT3DDEVICE9  pDevice,
  _In_    LPCTSTR            pSrcFile,
  _In_    UINT               Width,
  _In_    UINT               Height,
  _In_    UINT               MipLevels,
  _In_    DWORD              Usage,
  _In_    D3DFORMAT          Format,
  _In_    D3DPOOL            Pool,
  _In_    DWORD              Filter,
  _In_    DWORD              MipFilter,
  _In_    D3DCOLOR           ColorKey,
  _Inout_ D3DXIMAGE_INFO     *pSrcInfo,
  _Out_   PALETTEENTRY       *pPalette,
  _Out_   LPDIRECT3DTEXTURE9 *ppTexture
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

Ancho en píxeles. Si este valor es cero o D3DX DEFAULT, las dimensiones se toman del archivo y se \_ redondean hasta una potencia de dos. Si el dispositivo admite la no potencia de 2 texturas y se especifica [D3DX \_ DEFAULT \_ NONPOW2,](other-d3dx-constants.md) el tamaño no se redondeará.

</dd> <dt>

*Alto* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Alto, en píxeles. Si este valor es cero o D3DX DEFAULT, las dimensiones se toman del archivo y se \_ redondean hasta una potencia de dos. Si el dispositivo admite texturas sin potencia de 2 y [D3DX \_ DEFAULT \_ NONPOW2](other-d3dx-constants.md) está secificado, el tamaño no se redondeará.

</dd> <dt>

*MipLevels* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de niveles mip solicitados. Si este valor es cero o D3DX DEFAULT, se crea una \_ cadena de asignación mipmap completa. Si D3DX FROM FILE, el tamaño se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.

</dd> <dt>

*Uso* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

0, [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md)o **D3DUSAGE \_ DYNAMIC**. Establecer esta marca en **D3DUSAGE \_ RENDERTARGET** indica que la superficie se va a usar como destino de representación. A continuación, el recurso se puede pasar al *parámetro pNewRenderTarget* del [**método SetRenderTarget.**](/windows/desktop/api) Si se **especifica D3DUSAGE \_ RENDERTARGET** o **D3DUSAGE \_ DYNAMIC,** *pool* debe establecerse en D3DPOOL DEFAULT y la aplicación debe comprobar que el dispositivo admite esta operación mediante una llamada a \_ [**CheckDeviceFormat**](/windows/desktop/api). **D3DUSAGE \_ DYNAMIC** indica que la superficie se debe controlar dinámicamente. Consulte [Uso de texturas dinámicas.](performance-optimizations.md)

</dd> <dt>

*Formato* \[ En\]
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

Miembro del tipo [enumerado D3DFORMAT,](d3dformat.md) que describe el formato de píxel solicitado para la textura. La textura devuelta puede tener un formato diferente del especificado por *Format*. Las aplicaciones deben comprobar el formato de la textura devuelta. Si D3DFMT \_ UNKNOWN, el formato se toma del archivo. Si D3DFMT FROM FILE, el formato se toma exactamente como está en el archivo y se producirá un error en la llamada si esto infringe las funcionalidades \_ \_ del dispositivo.

</dd> <dt>

*Grupo* \[ En\]
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

Miembro del [**tipo enumerado D3DPOOL,**](./d3dpool.md) que describe la clase de memoria en la que se debe colocar la textura.

</dd> <dt>

*Filtro* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias constantes [D3DX \_ FILTER](d3dx-filter.md) que controlan cómo se filtra la imagen. Especificar [D3DX \_ DEFAULT para](other-d3dx-constants.md) este parámetro equivale a especificar D3DX FILTER TRIANGLE \_ \_ \| D3DX \_ FILTER \_ DITHER.

</dd> <dt>

*MipFilter* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias constantes [D3DX \_ FILTER](d3dx-filter.md) que controlan cómo se filtra la imagen. Especificar D3DX \_ DEFAULT para este parámetro equivale a especificar D3DX FILTER \_ \_ BOX. Además, use los bits 27-31 para especificar el número de niveles de mip que se omitirán (desde la parte superior de la cadena mipmap) cuando se cargue una textura .dds en la memoria; esto le permite omitir hasta 32 niveles.

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

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***

Dirección de un puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ NOTAVAILABLE, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La configuración del compilador también determina la versión de la función. Si se define Unicode, la llamada de función se resuelve en D3DXCreateTextureFromFileExW. De lo contrario, la llamada de función se resuelve en D3DXCreateTextureFromFileExA porque se usan cadenas ANSI.

Use [**D3DXCheckTextureRequirements**](d3dxchecktexturerequirements.md) para determinar si el dispositivo puede admitir la textura según el estado actual.

Esta función admite los siguientes formatos de archivo: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm y .tga. Vea [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).

Las texturas mipmapped rellenan automáticamente cada nivel con la textura cargada. Al cargar imágenes en texturas mipmapped, algunos dispositivos no pueden ir a una imagen 1x1 y se producirá un error en esta función. Si esto sucede, las imágenes deben cargarse manualmente.

Para obtener el mejor rendimiento cuando se **usa D3DXCreateTextureFromFileEx**:

1.  El escalado de imágenes y la conversión de formato en tiempo de carga pueden ser lentos. Almacene las imágenes en el formato y la resolución que se usarán. Si el hardware de destino requiere una potencia de 2 dimensiones, cree y almacene imágenes con la potencia de 2 dimensiones.
2.  Para la creación de imágenes mipmap en tiempo de carga, filtre mediante [D3DX \_ FILTER \_ BOX](d3dx-filter.md). Un filtro de cuadro es mucho más rápido que otros tipos de filtro, como D3DX \_ FILTER \_ TRIANGLE.
3.  Considere la posibilidad de usar archivos DDS. Dado que los archivos DDS se pueden usar para representar cualquier formato de textura de Direct3D 9, son muy fáciles de leer para D3DX. Además, pueden almacenar mapas mip, por lo que se pueden usar algoritmos de generación de mipmap para crear las imágenes.

Al omitir los niveles de asignación mip al cargar un archivo .dds, use la macro D3DX SKIP DDS MIP LEVELS para generar el \_ \_ valor de \_ \_ MipFilter. Esta macro toma el número de niveles que se omitirán y el tipo de filtro y devuelve el valor del filtro, que se pasará al parámetro MipFilter.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9tex.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
</dt> <dt>

[Funciones de textura en D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
