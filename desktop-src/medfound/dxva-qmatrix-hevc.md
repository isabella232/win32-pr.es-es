---
description: Define una matriz de cuantificación.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC estructura (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_Qmatrix_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: 5d71b392d41c123eb0106d08f1a75d2a5147977b106c811e0bf0786ab2acff2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974594"
---
# <a name="dxva_qmatrix_hevc-structure"></a>Estructura \_ DXVA Qmatrix \_ HEVC

Define una matriz de cuantificación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DXVA_Qmatrix_HEVC {
  UCHAR ucScalingLists0[6][16];
  UCHAR ucScalingLists1[6][64];
  UCHAR ucScalingLists2[6][64];
  UCHAR ucScalingLists3[2][64];
  UCHAR ucScalingListDCCoefSizeID2[6];
  UCHAR ucScalingListDCCoefSizeID3[2];
} DXVA_Qmatrix_HEVC, *LPDXVA_Qmatrix_HEVC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ucScalingLists0 \[ 6 \] \[ 16\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 4x4, correspondiente a ScalingList 0 MatrixID i en la especificación HEVC, donde MatrixID está en el intervalo de 0 a 5, ambos incluidos, e i está en el intervalo de \[ \] \[ \] \[ \] 0 a 15, ambos inclusive.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8x8, correspondiente a ScalingList 1 MatrixID i en la especificación HEVC, donde MatrixID está en el intervalo de 0 a 5, ambos incluidos, e i está en el intervalo de \[ \] \[ \] \[ \] 0 a 63, ambos inclusive.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8x8, correspondiente a ScalingList 2 MatrixID i en la especificación HEVC, donde MatrixID está en el intervalo de 0 a 5, ambos incluidos, e i está en el intervalo de \[ \] \[ \] \[ \] 0 a 63, ambos inclusive.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8x8, correspondiente a ScalingList 3 MatrixID i en la especificación HEVC, donde MatrixID está en el intervalo de 0 a 1, ambos incluidos, e i está en el intervalo de \[ \] \[ \] \[ \] 0 a 63, ambos inclusive.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contiene el valor dc de la lista de escalado para un tamaño de 16x16 con sizeID igual a 2 y correspondiente a la lista de escalado \_ \_ dc \_ coef \_ minus8 \[ sizeID - 2 \] \[ matrixID \] +8 con sizeID igual a 2 y matrixID en el intervalo de 0 a 5, ambos incluidos, en la especificación HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contiene el valor dc de la lista de escalado para un tamaño de 32 x 32 con sizeID igual a 3 y correspondiente a la lista de escalado \_ \_ dc \_ coef \_ minus8 \[ sizeID - 2 \] \[ matrixID \] +8 con sizeID igual a 3 y matrixID en el intervalo de 0 a 1, ambos incluidos, en la especificación HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                           |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




