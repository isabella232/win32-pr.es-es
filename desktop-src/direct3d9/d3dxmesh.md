---
description: 'Enumeración D3DXMESH: marcas que se usan para especificar opciones de creación para una malla.'
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeración D3DXMESH (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 6b83389ae4d92027245877e24e01621f0d93f123dee9ff4f040586b3e7c5111d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118525281"
---
# <a name="d3dxmesh-enumeration"></a>D3DXMESH (enumeración)

Marcas usadas para especificar opciones de creación para una malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 BITS**
</dt> <dd>

La malla tiene índices de 32 bits en lugar de índices de 16 bits. Vea la sección Comentarios.

</dd> <dt>

<span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**
</dt> <dd>

Use la [**marca de uso D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para los búferes de vértice e índice.

</dd> <dt>

<span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**PUNTOS D3DXMESH \_**
</dt> <dd>

Use la [**marca de uso D3DUSAGE \_ POINTS para**](d3dusage.md) los búferes de vértice e índice.

</dd> <dt>

<span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**
</dt> <dd>

Use la [**marca de uso D3DUSAGE \_ RTPATCHES**](d3dusage.md) para los búferes de vértices e índices.

</dd> <dt>

<span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**
</dt> <dd>

Al especificar esta marca, el vértice y el búfer de índice de la malla se crean con la marca [**D3DUSAGE \_ NPATCHES.**](d3dusage.md) Esto es necesario si el objeto de malla se va a representar mediante la mejora de N revisiones mediante Direct3D.

</dd> <dt>

<span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**
</dt> <dd>

Use la [**marca de uso D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para los búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH \_ VB \_ ADMINISTRADO**
</dt> <dd>

Use la marca [**de uso D3DPOOL \_ MANAGED**](./d3dpool.md) para búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**
</dt> <dd>

Use la [**marca de uso \_ WRITEONLY de D3DUSAGE**](d3dusage.md) para los búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ DYNAMIC**
</dt> <dd>

Use la [**marca de \_ uso dinámico D3DUSAGE**](d3dusage.md) para búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use la [**marca de uso D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para los búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**
</dt> <dd>

Use la [**marca de uso D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para los búferes de índice.

</dd> <dt>

<span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ ADMINISTRADO**
</dt> <dd>

Use la [**marca de uso D3DPOOL \_ MANAGED**](./d3dpool.md) para los búferes de índice.

</dd> <dt>

<span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**
</dt> <dd>

Use la [**marca de uso \_ WRITEONLY de D3DUSAGE**](d3dusage.md) para los búferes de índice.

</dd> <dt>

<span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ DYNAMIC**
</dt> <dd>

Use la [**marca de \_ uso DYNAMIC de D3DUSAGE**](d3dusage.md) para los búferes de índice.

</dd> <dt>

<span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**
</dt> <dd>

Use la [**marca de uso D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para los búferes de índice.

</dd> <dt>

<span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH \_ VB \_ COMPARTIDO**
</dt> <dd>

Fuerza a las mallas clonadas a compartir búferes de vértices.

</dd> <dt>

<span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**
</dt> <dd>

Use solo el procesamiento de hardware. En el caso del dispositivo en modo mixto, esta marca hará que el sistema use hardware (si se admite en hardware) o que el procesamiento de software sea predeterminado.

</dd> <dt>

<span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.

</dd> <dt>

<span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH \_ ADMINISTRADO**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ MANAGED y D3DXMESH \_ IB \_ MANAGED.

</dd> <dt>

<span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH \_ WRITEONLY**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ WRITEONLY y D3DXMESH \_ IB \_ WRITEONLY.

</dd> <dt>

<span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ DYNAMIC**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ DYNAMIC y D3DXMESH \_ IB \_ DYNAMIC.

</dd> <dt>

<span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**
</dt> <dd>

Equivalente a especificar D3DXMESH \_ VB \_ SOFTWAREPROCESSING y D3DXMESH \_ IB \_ SOFTWAREPROCESSING.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una malla de 32 bits (D3DXMESH de 32 BITS) puede admitir teóricamente \_ (2^32)-1 caras y vértices. Sin embargo, no es práctico asignar memoria para una malla que sea grande en un sistema operativo de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
