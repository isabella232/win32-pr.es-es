---
description: Cree un token de versión del sombreador de píxeles.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: D3DPS_VERSION macro (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPS_VERSION
api_type:
- HeaderDef
api_location:
- D3d9types.h
ms.openlocfilehash: a3958cfaa3afe06e22015a28e8e1ebfd8799c01e89772eb9794dd1249cc0df9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750905"
---
# <a name="d3dps_version-macro"></a>Macro D3DPS \_ VERSION

Cree un token de versión del sombreador de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
DWORD D3DPS_VERSION(
   int _Major,
   int _Minor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*\_Principal* 
</dt> <dd>

La versión principal del sombreador de píxeles.

</dd> <dt>

*\_Minor* 
</dt> <dd>

Versión del sombreador de píxeles secundaria.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor DWORD que es una versión del sombreador de píxeles.

## <a name="remarks"></a>Comentarios

Números de versión

El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices menores. Los números válidos se muestran en la tabla.



| Principal | Minor | Ejemplo             |
|-------|-------|---------------------|
| 1     | 1     | D3DPS \_ VERSION(1,1) |
| 1     | 2     | D3DPS \_ VERSION(1,2) |
| 1     | 3     | D3DPS \_ VERSION(1,3) |
| 1     | 4     | D3DPS \_ VERSION(1,4) |
| 2     | 0     | D3DPS \_ VERSION(2,0) |
| 3     | 0     | D3DPS \_ VERSION(3,0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




