---
description: Métricas de rendimiento para ayudar a comprender el rendimiento de una aplicación.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: D3DDEVINFO_D3D9BANDWIDTHTIMINGS estructura (D3D9Types.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060745"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a>D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS (estructura)

Métricas de rendimiento para ayudar a comprender el rendimiento de una aplicación.

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



## <a name="members"></a>Members

<dl> <dt>

**MaxBandwidthUtilized**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Ancho de banda o velocidad máxima de transferencia de datos desde la CPU del host a la GPU. Este suele ser el ancho de banda del bus PCI o AGP que conecta la CPU y la GPU.

</dd> <dt>

**FrontEndUploadMemoryUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de memoria utilizada al cargar datos desde la CPU del host a la GPU.

</dd> <dt>

**VertexRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de vértices. Este es el número de vértices procesados en comparación con la velocidad de procesamiento máxima teórica de vértices.

</dd> <dt>

**TriangleSetupRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de configuración de triángulos. Este es el número de triángulos configurados para la rasterización en comparación con la velocidad de configuración de triángulos máxima teórica.

</dd> <dt>

**FillRateUtilizedPercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de rendimiento de relleno de píxeles. Este es el número de píxeles que se rellenan en comparación con el relleno de píxeles teórico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
