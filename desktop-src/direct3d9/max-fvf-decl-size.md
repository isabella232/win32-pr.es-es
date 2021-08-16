---
description: Esta constante es el número máximo de declaradores de vértices para una malla.
ms.assetid: 234e99a2-1907-4065-b03b-fb9e8d6812ab
title: MAX_FVF_DECL_SIZE enumeración (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MAX_FVF_DECL_SIZE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 52ac939cc77bbd87dbecffc07253f0fadc5cbbdaa48e07f938f163c453c21e14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798801"
---
# <a name="max_fvf_decl_size-enumeration"></a>Enumeración MAX \_ FVF \_ DECL \_ SIZE

Esta constante es el número máximo de declaradores de vértices para una malla.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  MAX_FVF_DECL_SIZE  = MAXD3DDECLLENGTH + 1
} MAX_FVF_DECL_SIZE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MAX_FVF_DECL_SIZE"></span><span id="max_fvf_decl_size"></span>**MAX \_ FVF \_ DECL \_ SIZE**
</dt> <dd>

Número máximo de elementos de la declaración de vértice. El adicional (+1) es para [**D3DDECL \_ END.**](d3ddecl-end.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

MAXD3DDECLLENGTH se define como un máximo de 64 (vea d3d9types.h). Esto no incluye el elemento de vértice de marcador "end".

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Enumeraciones D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[**GetDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexdeclaration9-getdeclaration)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> <dt>

[**ID3DXSkinInfo**](id3dxskininfo.md)
</dt> </dl>

 

 
