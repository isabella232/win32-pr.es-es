---
description: Métricas de rendimiento para ayudarle a comprender el rendimiento de una aplicación.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280279"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ estructura D3D9BANDWIDTHTIMINGS

Métricas de rendimiento para ayudarle a comprender el rendimiento de una aplicación.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

El ancho de banda o la velocidad de transferencia de datos máxima de la CPU del host a la GPU. Suele ser el ancho de banda del bus PCI o AGP que conecta la CPU y la GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de uso de memoria al cargar datos desde la CPU del host a la GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de vértices. Es el número de vértices procesados en comparación con la velocidad máxima de procesamiento de vértices teóricos.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de configuración de triángulo. Es el número de triángulos que se configuran para la rasterización en comparación con la tasa de configuración del triángulo máximo teórico.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de relleno de píxeles. Es el número de píxeles que se rellenan en comparación con el relleno de píxeles teórico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
