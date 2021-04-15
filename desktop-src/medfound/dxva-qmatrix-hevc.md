---
description: Define una matriz de cuantificación.
ms.assetid: 44a5c81f-98d8-4b16-a467-433bae781691
title: DXVA_Qmatrix_HEVC estructura (DXVA. h)
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
ms.openlocfilehash: 2aba66636717eee5deb04032d9408ace495e1edf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539562"
---
# <a name="dxva_qmatrix_hevc-structure"></a>Qmatrix de DXVA \_ \_ HEVC estructura

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

Contiene las listas de escalado para el proceso de escala de 4x4, correspondiente a ScalingList \[ 0 \] \[ MatrixID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, e i está en el intervalo de 0 a 15, ambos incluidos.

</dd> <dt>

**ucScalingLists1 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8 x 4, que corresponde a ScalingList \[ 1 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.

</dd> <dt>

**ucScalingLists2 \[ 6 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8 x 4, que corresponde a ScalingList \[ 2 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 5, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.

</dd> <dt>

**ucScalingLists3 \[ 2 \] \[ 64\]**
</dt> <dd>

Contiene las listas de escalado para el proceso de escalado de 8 x 3, que corresponde a ScalingList \[ 3 \] \[ MATRIXID \] \[ i \] en HEVC Specification, donde MatrixID está en el intervalo de 0 a 1, ambos inclusive, y se encuentra en el intervalo de 0 a 63, ambos incluidos.

</dd> <dt>

**ucScalingListDCCoefSizeID2**
</dt> <dd>

Contiene el valor DC de la lista de escalado para el tamaño 16x16 con sizeID igual a 2 y correspondiente a la \_ lista de escalado \_ DC \_ Coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID igual a 2 y matrixID en el intervalo de 0 a 5, ambos inclusive, en la especificación HEVC.

</dd> <dt>

**ucScalingListDCCoefSizeID3**
</dt> <dd>

Contiene el valor DC de la lista de escalado para el tamaño 32x32 con sizeID igual a 3 y correspondiente a la \_ lista de escalado \_ DC \_ Coef \_ minus8 \[ sizeID − 2 \] \[ matrixID \] + 8 con sizeID igual a 3 y matrixID en el intervalo de 0 a 1, ambos incluidos, en la especificación HEVC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio Windows 8.1\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation estructuras](media-foundation-structures.md)
</dt> </dl>

 

 




