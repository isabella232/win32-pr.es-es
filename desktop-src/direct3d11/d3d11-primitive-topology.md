---
description: Cómo la canalización interpreta los datos de vértices que están enlazados a la fase de ensamblador de entrada. Estos valores de topología primitiva determinan cómo se representan los datos de vértices en la pantalla.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: D3D11 \_ \_ enumeración de topología primitiva
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 1d2beab107a3f3abe03e5a17f068e1b508422241
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104998001"
---
# <a name="d3d11_primitive_topology-enumeration"></a>D3D11 \_ \_ enumeración de topología primitiva

Cómo la canalización interpreta los datos de vértices que están enlazados a la fase de ensamblador de entrada. Estos valores de topología primitiva determinan cómo se representan los datos de vértices en la pantalla.

## <a name="syntax"></a>Sintaxis


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**\_Topología primitiva D3D11 \_ \_ sin definir**
</dt> <dd>

La fase del IA no se ha inicializado con una topología primitiva. La fase del IA no funcionará correctamente a menos que se defina una topología primitiva.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ \_ topología primitiva \_ POINTLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de puntos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**D3D11 \_ \_ topología primitiva \_ LINELIST**
</dt> <dd>

Interprete los datos de vértice como una lista de líneas.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**D3D11 \_ \_ topología primitiva \_ LINESTRIP**
</dt> <dd>

Interprete los datos de vértice como una franja de líneas.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ \_ topología primitiva \_ TRIANGLELIST**
</dt> <dd>

Interprete los datos de vértice como una lista de triángulos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ \_ topología primitiva \_ TRIANGLESTRIP**
</dt> <dd>

Interprete los datos de vértice como una franja de triángulo.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ \_ \_ LINELIST ADJ de topología \_ primitiva**
</dt> <dd>

Interprete los datos de vértices como una lista de líneas con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ \_ \_ LINESTRIP ADJ de topología \_ primitiva**
</dt> <dd>

Interprete los datos de vértices como franja de líneas con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ \_ \_ TRIANGLELIST ADJ de topología \_ primitiva**
</dt> <dd>

Interprete los datos de vértices como una lista de triángulos con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ \_ \_ TRIANGLESTRIP ADJ de topología \_ primitiva**
</dt> <dd>

Interprete los datos de vértices como franja de triángulo con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 1 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 2 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 3 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 4 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 5 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 6 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 7 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 8 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 9 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 10 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 11 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 12 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 13 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 14 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 15 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 16 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 17 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 18 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**Punto de control de la \_ topología primitiva de D3D11 \_ \_ 19 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ punto de control de topología primitiva de \_ \_ 20 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 21 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 23 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 24 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 25 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 26 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 27 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ punto de control de la \_ topología primitiva \_ 28 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ 30 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ punto de control de la topología primitiva de \_ \_ \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ \_ punto de control de topología primitiva \_ 32 \_ \_ \_ PATCHLIST**
</dt> <dd>

Interprete los datos de vértice como una lista de revisiones.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La enumeración de **\_ \_ topología primitiva D3D11** es el tipo definido en el archivo de encabezado D3D11. h como una enumeración de [**\_ \_ topología de D3D primitivo**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) , que está totalmente definida en el archivo de encabezado D3DCommon. h.
