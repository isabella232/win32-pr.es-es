---
title: D3DX11_IMAGE_INFO estructura (D3DX11tex. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_INFO estructura (D3DX11tex. h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO estructura de Direct3D 11
- Puntero de estructura de LPD3DX11_IMAGE_INFO Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_IMAGE_INFO
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 927967f8e76d0147ccc264bcbdd773191a170ae7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987210"
---
# <a name="d3dx11_image_info-structure"></a>Estructura de información de \_ imagen de D3DX11 \_

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Opcionalmente, puede proporcionar información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX11 \_ predeterminado para cualquiera de estos parámetros hará que D3DX use automáticamente el valor del archivo de código fuente.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DX11_IMAGE_INFO {
  UINT                     Width;
  UINT                     Height;
  UINT                     Depth;
  UINT                     ArraySize;
  UINT                     MipLevels;
  UINT                     MiscFlags;
  DXGI_FORMAT              Format;
  D3D11_RESOURCE_DIMENSION ResourceDimension;
  D3DX11_IMAGE_FILE_FORMAT ImageFileFormat;
} D3DX11_IMAGE_INFO, *LPD3DX11_IMAGE_INFO;
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

**ArraySize**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de la matriz.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número máximo de niveles de mipmap en la textura. Vea los comentarios de [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). El uso del valor predeterminado de 0 o D3DX11 hará que \_ se cree una cadena de mipmap completa.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Propiedades de recursos variadas especificadas con una marca de [**\_ \_ \_ marca de varios recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) .

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Una enumeración de [**\_ formato de DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que especifica el formato en el que estará la textura después de cargarse.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **\_ \_ dimensión de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Un valor de [**\_ \_ dimensión de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) , que identifica el tipo de recurso.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: **[ **\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md)**

</dd> <dd>

Un valor de [**\_ formato de \_ archivo \_ de imagen D3DX11**](d3dx11-image-file-format.md) , que identifica el formato de imagen.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura la usan métodos como: [**D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

