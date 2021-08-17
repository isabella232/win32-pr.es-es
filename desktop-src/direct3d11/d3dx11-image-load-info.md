---
title: D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex.h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO estructura direct3D 11
- LPD3DX11_IMAGE_LOAD_INFO puntero de estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_LOAD_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c45bc3b9ec948c869b121190f52435a257141f1e5a6e9f36c347ab29bafb5522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536862"
---
# <a name="d3dx11_image_load_info-structure"></a>Estructura D3DX11 \_ IMAGE \_ LOAD \_ INFO

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX11 DEFAULT para cualquiera de estos parámetros hará que D3DX use automáticamente el \_ valor del archivo de origen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX11_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D11_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX11_IMAGE_INFO *pSrcInfo;
} D3DX11_IMAGE_LOAD_INFO, *LPD3DX11_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ancho de destino de la textura. Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alto de destino de la textura. Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profundidad de la textura. Esto solo se aplica a las texturas de volumen.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

El nivel de mapa mip de resolución más alto de la textura. Si es mayor que 0, después de cargar la textura FirstMipLevel se asignará al nivel 0 de mipmap.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número máximo de niveles de mapa mip en la textura. Vea los comentarios en [**D3D11 \_ TEXAS1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). El uso de 0 o D3DX11 DEFAULT hará que se cree una \_ cadena de asignación mip completa.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **D3D11 \_ USAGE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

La forma en que el recurso de textura está pensado para usarse. Vea [**D3D11 USAGE ( \_ USO de D3D11).**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fases de canalización a las que se permitirá el enlace de la textura. Vea [**D3D11 \_ BIND \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Permisos de acceso que tendrá la CPU para el recurso de textura. Consulte [**D3D11 CPU ACCESS FLAG (MARCA \_ DE ACCESO DE CPU \_ D3D11). \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag)

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Propiedades de recursos varios (consulte [**D3D11 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumeración [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que indica el formato en el que estará la textura después de cargarla.

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre la textura mediante el filtro especificado (solo al volver amuestrear). Vea [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre los niveles de mip de textura mediante el filtro especificado (solo si se generan mapas mip). Los valores válidos son D3DX11 \_ FILTER \_ NONE, D3DX11 \_ FILTER \_ POINT, D3DX11 FILTER LINEAR o \_ \_ D3DX11 \_ FILTER \_ TRIANGLE. Vea [**D3DX11 \_ FILTER \_ FLAG**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX11 \_ IMAGE \_ INFO**](d3dx11-image-info.md)\***

</dd> <dd>

Información sobre la imagen original. Vea [**D3DX11 IMAGE INFO ( Información de imagen de D3DX11). \_ \_**](d3dx11-image-info.md) Se puede obtener con [**D3DX11GetImageInfoFromFile,**](d3dx11getimageinfofromfile.md) [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Al inicializar la estructura, puede establecer cualquier miembro en D3DX11 DEFAULT y D3DX la inicializará con un valor predeterminado de la textura de origen cuando se cargue \_ la textura.

Esta estructura la pueden usar las API que:

-   Cree recursos, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CreateShaderResourceViewFromFile.**](d3dx11createshaderresourceviewfromfile.md)
-   Cree procesadores de datos, [**como D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) o [**D3DX11CreateAsyncShaderResourceViewProcessor.**](d3dx11createasyncshaderresourceviewprocessor.md)

Los valores predeterminados son:


```
    Width = D3DX11_DEFAULT;
    Height = D3DX11_DEFAULT;
    Depth = D3DX11_DEFAULT;
    FirstMipLevel = D3DX11_DEFAULT;
    MipLevels = D3DX11_DEFAULT;
    Usage = (D3D11_USAGE) D3DX11_DEFAULT;
    BindFlags = D3DX11_DEFAULT;
    CpuAccessFlags = D3DX11_DEFAULT;
    MiscFlags = D3DX11_DEFAULT;
    Format = DXGI_FORMAT_FROM_FILE;
    Filter = D3DX11_DEFAULT;
    MipFilter = D3DX11_DEFAULT;
    pSrcInfo = NULL;
```



Este es un breve ejemplo que usa esta estructura para proporcionar el formato de píxel al cargar una textura. Para obtener el código completo, vea HDRFormats10.cpp en [el ejemplo HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


```
ID3D11ShaderResourceView* pCubeRV = NULL;
WCHAR strPath[MAX_PATH];
D3DX11_IMAGE_LOAD_INFO LoadInfo;

    DXUTFindDXSDKMediaFileCch( strPath, MAX_PATH, 
        L"Light Probes\\uffizi_cross.dds" );

    LoadInfo.Format = DXGI_FORMAT_R16G16B16A16_FLOAT;

    hr = D3DX11CreateShaderResourceViewFromFile( pd3dDevice, strPath, 
        &LoadInfo, NULL, &pCubeRV, NULL );
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

