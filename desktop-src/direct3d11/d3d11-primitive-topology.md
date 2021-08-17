---
description: Cómo interpreta la canalización los datos de vértice enlazados a la fase del ensamblador de entrada. Estos valores de topología primitivos determinan cómo se representan los datos del vértice en la pantalla.
ms.assetid: ca0547b2-d0f8-4edc-a62c-3c903e1b33ea
title: Enumeración \_ TOPOLOGY PRIMITIVA D3D11 \_
ms.date: 06/26/2019
ms.topic: reference
ms.openlocfilehash: 7c899d738b2a80036eaea61352f5e8aa82c73ddbeb48433d275d74506a478d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990015"
---
# <a name="d3d11_primitive_topology-enumeration"></a>Enumeración \_ TOPOLOGY PRIMITIVA D3D11 \_

Cómo interpreta la canalización los datos de vértice enlazados a la fase del ensamblador de entrada. Estos valores de topología primitivos determinan cómo se representan los datos del vértice en la pantalla.

## <a name="syntax"></a>Syntax


```C++
} D3D11_PRIMITIVE_TOPOLOGY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_UNDEFINED"></span><span id="d3d11_primitive_topology_undefined"></span>**TOPOLOGÍA PRIMITIVA D3D11 \_ \_ SIN \_ DEFINIR**
</dt> <dd>

La fase IA no se ha inicializado con una topología primitiva. La fase IA no funcionará correctamente a menos que se defina una topología primitiva.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_POINTLIST"></span><span id="d3d11_primitive_topology_pointlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ POINTLIST**
</dt> <dd>

Interpretar los datos del vértice como una lista de puntos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST"></span><span id="d3d11_primitive_topology_linelist"></span>**LISTA DE LÍNEAS DE TOPOLOGÍA PRIMITIVA D3D11 \_ \_ \_**
</dt> <dd>

Interpretar los datos del vértice como una lista de líneas.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP"></span><span id="d3d11_primitive_topology_linestrip"></span>**LINESTRIP DE TOPOLOGÍA PRIMITIVA D3D11 \_ \_ \_**
</dt> <dd>

Interpretar los datos del vértice como una franja de líneas.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST"></span><span id="d3d11_primitive_topology_trianglelist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLELIST**
</dt> <dd>

Interpretar los datos del vértice como una lista de triángulos.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP"></span><span id="d3d11_primitive_topology_trianglestrip"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLESTRIP**
</dt> <dd>

Interpretar los datos del vértice como una franja de triángulo.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINELIST_ADJ"></span><span id="d3d11_primitive_topology_linelist_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ LINELIST \_ ADJ**
</dt> <dd>

Interprete los datos de vértice como una lista de líneas con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_LINESTRIP_ADJ"></span><span id="d3d11_primitive_topology_linestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ LINESTRIP \_ ADJ**
</dt> <dd>

Interpreta los datos del vértice como franja de líneas con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLELIST_ADJ"></span><span id="d3d11_primitive_topology_trianglelist_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLELIST \_ ADJ**
</dt> <dd>

Interprete los datos de vértice como una lista de triángulos con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_TRIANGLESTRIP_ADJ"></span><span id="d3d11_primitive_topology_trianglestrip_adj"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ TRIANGLESTRIP \_ ADJ**
</dt> <dd>

Interprete los datos del vértice como una franja de triángulo con datos de adyacencia.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_1_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_1_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 1 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_2_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_2_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 2 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_3_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_3_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 3 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_4_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_4_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 4 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_5_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_5_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 5 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_6_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_6_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 6 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_7_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_7_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 7 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_8_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_8_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 8 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_9_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_9_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 9 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_10_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_10_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 10 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_11_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_11_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 11 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_12_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_12_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 12 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_13_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_13_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 13 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_14_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_14_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 14 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_15_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_15_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 15 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_16_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_16_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 16 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_17_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_17_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 17 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_18_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_18_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 18 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_19_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_19_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 19 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_20_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_20_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 20 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_21_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_21_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 21 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_22_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_22_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 22 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_23_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_23_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 23 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_24_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_24_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 24 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_25_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_25_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 25 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_26_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_26_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 26 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_27_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_27_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 27 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_28_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_28_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 28 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_29_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_29_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 29 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_30_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_30_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 30 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_31_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_31_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 31 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> <dt>

<span id="D3D11_PRIMITIVE_TOPOLOGY_32_CONTROL_POINT_PATCHLIST"></span><span id="d3d11_primitive_topology_32_control_point_patchlist"></span>**D3D11 \_ PRIMITIVE \_ TOPOLOGY \_ 32 \_ CONTROL \_ POINT \_ PATCHLIST**
</dt> <dd>

Interprete los datos del vértice como una lista de revisiones.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La enumeración **\_ \_ TOPOLOGY PRIMITIVA D3D11** es el tipo definido en el archivo de encabezado D3D11.h como una enumeración DE TOPOLOGÍA [**\_ PRIMITIVA \_ D3D,**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive_topology) que está totalmente definida en el archivo de encabezado D3DCommon.h.
