---
description: Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX10 DEFAULT para cualquiera de estos parámetros hará que D3DX use automáticamente el \_ valor del archivo de origen.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: D3DX10_IMAGE_LOAD_INFO estructura (D3DX10Tex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_IMAGE_LOAD_INFO
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: 89e819e81c11842feaa6996e047f3cac3587792c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566729"
---
# <a name="d3dx10_image_load_info-structure"></a>Estructura D3DX10 \_ IMAGE \_ LOAD \_ INFO

Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX10 DEFAULT para cualquiera de estos parámetros hará que D3DX use automáticamente el \_ valor del archivo de origen.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX10_IMAGE_LOAD_INFO {
  UINT              Width;
  UINT              Height;
  UINT              Depth;
  UINT              FirstMipLevel;
  UINT              MipLevels;
  D3D10_USAGE       Usage;
  UINT              BindFlags;
  UINT              CpuAccessFlags;
  UINT              MiscFlags;
  DXGI_FORMAT       Format;
  UINT              Filter;
  UINT              MipFilter;
  D3DX10_IMAGE_INFO *pSrcInfo;
} D3DX10_IMAGE_LOAD_INFO, *LPD3DX10_IMAGE_LOAD_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de destino de la textura. Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de destino de la textura. Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidad de la textura. Esto solo se aplica a las texturas de volumen.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

El nivel de mapa mip de resolución más alto de la textura. Si es mayor que 0, después de cargar la textura FirstMipLevel se asignará al nivel de mapa mip 0.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Número máximo de niveles de mapa mip que tendrá la textura. El uso de 0 o D3DX10 DEFAULT hará que se cree una cadena \_ de asignación mip completa.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **D3D10 \_ USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

La forma en que el recurso de textura está pensado para usarse. Vea [**D3D10 USAGE ( \_ USO de D3D10).**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Fases de canalización a las que se permitirá el enlace de la textura. Vea [**D3D10 \_ BIND \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Permisos de acceso que tendrá la CPU para el recurso de textura. Consulte [**D3D10 CPU ACCESS FLAG (MARCA \_ DE ACCESO DE CPU \_ D3D10). \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Propiedades de recursos varios (consulte [**D3D10 \_ RESOURCE \_ MISC \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

El formato en el que estará la textura después de cargarla. Vea [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre la textura mediante el filtro especificado (solo al volver amuestrear). Vea [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre los niveles de mip de textura mediante el filtro especificado (solo si se generan mapas mip). Los valores válidos son D3DX10 \_ FILTER \_ NONE, D3DX10 \_ FILTER \_ POINT, D3DX10 FILTER LINEAR o \_ \_ D3DX10 \_ FILTER \_ TRIANGLE. Vea [**D3DX10 \_ FILTER \_ FLAG**](d3dx10-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **D3DX10 \_ IMAGE \_ INFO**](d3dx10-image-info.md)\***

</dd> <dd>

Información sobre la imagen original. Vea D3DX10 IMAGE INFO ( Información de [**\_ imagen \_ de D3DX10).**](d3dx10-image-info.md) Se puede obtener con [**D3DX10GetImageInfoFromFile,**](d3dx10getimageinfofromfile.md) [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)o [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al inicializar la estructura, puede establecer cualquier miembro en D3DX10 DEFAULT y D3DX la inicializará con un valor predeterminado de la textura de origen cuando se cargue \_ la textura.

Esta estructura la pueden usar las API que:

-   Cree recursos, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CreateShaderResourceViewFromFile.**](d3dx10createshaderresourceviewfromfile.md)
-   Cree procesadores de datos, como [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) o [**D3DX10CreateAsyncShaderResourceViewProcessor.**](d3dx10createasyncshaderresourceviewprocessor.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
