---
description: Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX10 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.
ms.assetid: 8325d50e-a8a9-4ee2-87e2-e60fb3699af6
title: D3DX10_IMAGE_LOAD_INFO estructura (D3DX10Tex. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718433"
---
# <a name="d3dx10_image_load_info-structure"></a>\_Estructura de \_ información de carga de imagen de D3DX10 \_

Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX10 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.

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



## <a name="members"></a>Miembros

<dl> <dt>

**Width**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de destino de la textura. Si el ancho real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este ancho de destino.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de destino de la textura. Si el alto real de la textura es mayor o menor que este valor, la textura se escalará o reducirá verticalmente para ajustarse a este alto de destino.

</dd> <dt>

**Profundidad**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Profundidad de la textura. Esto solo se aplica a las texturas de volumen.

</dd> <dt>

**FirstMipLevel**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel de mipmap de resolución más alto de la textura. Si es mayor que 0, después de que se cargue la textura, FirstMipLevel se asignará al nivel 0 del mipmap.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Número máximo de niveles de mipmap que tendrá la textura. El uso del valor predeterminado de 0 o D3DX10 hará que \_ se cree una cadena de mipmap completa.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **\_ uso de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)**

</dd> <dd>

La forma en que se va a usar el recurso de textura. Vea [**\_ uso de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).

</dd> <dt>

**BindFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Fases de canalización a las que se puede enlazar la textura. Vea [**D3D10 \_ BIND \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag).

</dd> <dt>

**CpuAccessFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Los permisos de acceso que tendrá la CPU para el recurso de textura. Consulte [**\_ marca de \_ acceso \_ de CPU de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag).

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Propiedades de recursos misceláneas (consulte la [**marca D3D10 de \_ recursos \_ varios \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag)).

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Formato en el que estará la textura después de cargarse. Consulte [**\_ formato de DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).

</dd> <dt>

**Filter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre la textura mediante el filtro especificado (solo cuando se remuestre). Vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md).

</dd> <dt>

**MipFilter**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Filtre los niveles de textura de MIP mediante el filtro especificado (solo si se generan mapas MIP). Los valores válidos son D3DX10 \_ Filter \_ None, D3DX10 Filter \_ \_ Point, D3DX10 \_ Filter \_ linear o D3DX10 \_ Filter \_ Triangle. Vea [**D3DX10 \_ Filter \_ Flag**](d3dx10-filter-flag.md).

</dd> <dt>

**pSrcInfo**
</dt> <dd>

Tipo: **[ **\_ \_ información de imagen de D3DX10**](d3dx10-image-info.md)\***

</dd> <dd>

Información sobre la imagen original. Consulte [**la \_ \_ información**](d3dx10-image-info.md)de la imagen de D3DX10. Se puede obtener con [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md), [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)o [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Al inicializar la estructura, puede establecer cualquier miembro en D3DX10 \_ default y D3DX lo inicializará con un valor predeterminado de la textura de origen cuando se cargue la textura.

Esta estructura la pueden usar las API que:

-   Cree recursos, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) y [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md).
-   Cree procesadores de datos, como [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) o [**D3DX10CreateAsyncShaderResourceViewProcessor**](d3dx10createasyncshaderresourceviewprocessor.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX10Tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
