---
title: D3DX11_IMAGE_INFO estructura (D3DX11tex.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store. Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. | D3DX11_IMAGE_INFO estructura (D3DX11tex.h)
ms.assetid: 981f4f1d-7609-416a-8f92-c7223d8b2773
keywords:
- D3DX11_IMAGE_INFO estructura direct3D 11
- LPD3DX11_IMAGE_INFO puntero de estructura direct3D 11
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
ms.openlocfilehash: 64366755e9bb9398e8107d931ee5425d2fcee78fdd9d03487b9533270cc17c19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536872"
---
# <a name="d3dx11_image_info-structure"></a>Estructura D3DX11 \_ IMAGE \_ INFO

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

Opcionalmente, proporcione información a las API del cargador de texturas para controlar cómo se cargan las texturas. Un valor de D3DX11 DEFAULT para cualquiera de estos parámetros hará que D3DX use automáticamente el \_ valor del archivo de origen.

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

**ArraySize**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de elementos de la matriz.

</dd> <dt>

**MipLevels**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número máximo de niveles de mapa mip en la textura. Vea los comentarios en [**D3D11 \_ TEXAS1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv). El uso de 0 o D3DX11 DEFAULT hará que se cree una \_ cadena de asignación mip completa.

</dd> <dt>

**MiscFlags**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Propiedades de recursos varios especificadas con una [**marca \_ \_ MISC \_ DE RECURSOS D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

</dd> <dt>

**Format**
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

</dd> <dd>

Enumeración [**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) que especifica el formato en el que estará la textura después de cargarla.

</dd> <dt>

**ResourceDimension**
</dt> <dd>

Tipo: **[ **DIMENSIÓN DE \_ RECURSOS \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension)**

</dd> <dd>

Valor [**DE DIMENSIÓN DE \_ RECURSOS \_ D3D11,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_dimension) que identifica el tipo de recurso.

</dd> <dt>

**ImageFileFormat**
</dt> <dd>

Tipo: FORMATO DE ARCHIVO DE **[ **\_ IMAGEN \_ \_ D3DX11**](d3dx11-image-file-format.md)**

</dd> <dd>

Valor [**D3DX11 \_ IMAGE FILE \_ \_ FORMAT,**](d3dx11-image-file-format.md) que identifica el formato de imagen.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura la usan métodos [**como: D3DX11GetImageInfoFromFile**](d3dx11getimageinfofromfile.md), [**D3DX11GetImageInfoFromMemory**](d3dx11getimageinfofrommemory.md)o [**D3DX11GetImageInfoFromResource**](d3dx11getimageinfofromresource.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3DX11tex.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras D3DX](d3d11-graphics-reference-d3dx11-structures.md)
</dt> </dl>

 

