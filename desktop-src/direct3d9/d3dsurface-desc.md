---
description: Describe una superficie.
ms.assetid: fad8ffdb-36e5-4695-b343-e1315357c31a
title: D3DSURFACE_DESC estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSURFACE_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 6424bbe9b78532657670bc5cd9ad0705de89a3b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717689"
---
# <a name="d3dsurface_desc-structure"></a>D3DSURFACE \_ DESC (estructura)

Describe una superficie.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DSURFACE_DESC {
  D3DFORMAT           Format;
  D3DRESOURCETYPE     Type;
  DWORD               Usage;
  D3DPOOL             Pool;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  UINT                Width;
  UINT                Height;
} D3DSURFACE_DESC, *LPD3DSURFACE_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Format**
</dt> <dd>

Tipo: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) , que describe el formato de la superficie.

</dd> <dt>

**Tipo**
</dt> <dd>

Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DRESOURCETYPE**](./d3dresourcetype.md) que identifica este recurso como una superficie.

</dd> <dt>

**Uso**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Los valores D3DUSAGE \_ DEPTHSTENCIL o D3DUSAGE \_ RENDERTARGET. Para obtener más información, vea [**D3DUSAGE**](d3dusage.md).

</dd> <dt>

**Grupo**
</dt> <dd>

Tipo: **[ **D3DPOOL**](./d3dpool.md)**

</dd> <dd>

Miembro del tipo enumerado [**D3DPOOL**](./d3dpool.md) , que especifica la clase de memoria asignada para esta superficie.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Tipo: **[ **D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md)**

</dd> <dd>

Miembro del tipo enumerado de [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) , que especifica los niveles de muestreo múltiple de escena completa admitidos por la superficie.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Nivel de calidad. El intervalo válido está comprendido entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype). Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL. Los valores MultisampleQuality de los destinos de presentación emparejados, las superficies de estarcido de profundidad y el tipo de Multimuestra deben coincidir.

</dd> <dt>

**Width**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de la superficie, en píxeles.

</dd> <dt>

**Height**
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Alto de la superficie, en píxeles.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> <dt>

[**GetDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-getdesc)
</dt> <dt>

[**GetLevelDesc**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getleveldesc)
</dt> </dl>

 

 
