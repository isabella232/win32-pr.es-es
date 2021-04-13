---
description: Cree un token de versión del sombreador de píxeles.
ms.assetid: 70089a93-83df-4ac4-8d98-4e1bb6ad2581
title: Macro D3DPS_VERSION (D3d9types. h)
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
ms.openlocfilehash: c3f30d673145ec9dfe38bd8e2a636ac04c9a195a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362609"
---
# <a name="d3dps_version-macro"></a>D3DPS \_ versión (macro)

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

*\_Principales* 
</dt> <dd>

Versión principal del sombreador de píxeles.

</dd> <dt>

*\_Minor* 
</dt> <dd>

Versión secundaria del sombreador de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor DWORD que es una versión de sombreador de píxeles.

## <a name="remarks"></a>Observaciones

Números de versión

El número de versión es una combinación de la versión principal y los números de versión del sombreador de vértices secundarios. Los números válidos se muestran en la tabla.



| Principal | Minor | Ejemplo             |
|-------|-------|---------------------|
| 1     | 1     | \_Versión de D3DPS (1,1) |
| 1     | 2     | \_Versión de D3DPS (1,2) |
| 1     | 3     | \_Versión de D3DPS (1,1) |
| 1     | 4     | \_Versión de D3DPS (1,1) |
| 2     | 0     | \_Versión de D3DPS (2,0) |
| 3     | 0     | \_Versión de D3DPS (3, 0) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Macros](dx9-graphics-reference-d3d-macros.md)
</dt> <dt>

[D3DCAPS9](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> </dl>

 

 




