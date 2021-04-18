---
title: D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_LOAD_INFO estructura (D3DX11tex. h)
ms.assetid: 6cd2f590-4e15-41e6-9f04-cd91eeb082db
keywords:
- D3DX11_IMAGE_LOAD_INFO estructura de Direct3D 11
- Puntero de estructura de LPD3DX11_IMAGE_LOAD_INFO Direct3D 11
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
ms.openlocfilehash: 2905d135a515f4ef90557ac74c35665623462439
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987205"
---
# <a name="d3dx11_image_load_info-structure"></a>\_Estructura de \_ información de carga de imagen de D3DX11 \_

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX11 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Ancho de destino de la textura. Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Alto de destino de la textura. Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Profundidad de la textura. Esto solo se aplica a las texturas de volumen.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nivel de mipmap de resolución más alto de la textura. Si es mayor que 0, después de que se cargue la textura, FirstMipLevel se asignará al nivel 0 del mipmap.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número máximo de niveles de mipmap en la textura. Vea los comentarios de [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). El uso del valor predeterminado de 0 o D3DX11 hará que \_ se cree una cadena de mipmap completa.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)**

</dd> <dd>

La forma en que se va a usar el recurso de textura. Vea [**\_ uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Fases de canalización a las que se puede enlazar la textura. Vea [**D3D11 \_ BIND \_ Flag**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Los permisos de acceso que tendrá la CPU para el recurso de textura. Consulte [**\_ marca de \_ acceso \_ de CPU de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Propiedades de recursos misceláneas (consulte la [**marca D3D11 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que indica el formato en el que estará la textura después de cargarse.

</dd> <dt>

**Filtrar**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre la textura mediante el filtro especificado (solo cuando se remuestre). Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Filtre los niveles de textura de MIP mediante el filtro especificado (solo si se generan mapas MIP). Los valores válidos son D3DX11 \_ Filter \_ None, D3DX11 Filter \_ \_ Point, D3DX11 \_ Filter \_ linear o D3DX11 \_ Filter \_ Triangle. Vea [**D3DX11 \_ Filter \_ Flag**](d3dx11-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **\_ \_ información de imagen de D3DX11**](d3dx11-image-info.md)\***

</dd> <dd>

Información sobre la imagen original. Consulte [**la \_ \_ información**](d3dx11-image-info.md)de la imagen de D3DX11. Se puede obtener con [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al inicializar la estructura, puede establecer cualquier miembro en D3DX11 \_ default y D3DX lo inicializará con un valor predeterminado de la textura de origen cuando se cargue la textura.

Esta estructura la pueden usar las API que:

-   Cree recursos, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) y [**D3DX11CreateShaderResourceViewFromFile**](d3dx11createshaderresourceviewfromfile.md).
-   Cree procesadores de datos, como [**D3DX11CreateAsyncTextureInfoProcessor**](d3dx11createasynctextureinfoprocessor.md) o [**D3DX11CreateAsyncShaderResourceViewProcessor**](d3dx11createasyncshaderresourceviewprocessor.md).

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



Este es un breve ejemplo que usa esta estructura para proporcionar el formato de píxel al cargar una textura. Para obtener el código completo, consulte HDRFormats10. cpp en el [ejemplo HDRToneMappingCS11](https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx).


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
| Encabezado<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

