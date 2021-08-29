---
description: Habilita o deshabilita las optimizaciones de CPU.
ms.assetid: 6f73df12-f2fc-4651-b0f7-f7a55e534d3d
title: Función D3DXCpuOptimizations (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCpuOptimizations
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: de2c24667384ad8f163774c77b4f7fea9332e953425cd5ee520cd310fa0733a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853455"
---
# <a name="d3dxcpuoptimizations-function"></a>Función D3DXCpuOptimizations

Habilita o deshabilita las optimizaciones de CPU.

## <a name="syntax"></a>Sintaxis


```C++
D3DX_CPU_OPTIMIZATION D3DXCpuOptimizations(
  _In_ BOOL Enable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Habilitar* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

**TRUE** para habilitar las optimizaciones de CPU; en caso **contrario, FALSE**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **OPTIMIZACIÓN DE \_ CPU \_ D3DX**](d3dx-cpu-optimization.md)**

Devuelve el tipo de CPU detectada y para qué optimizaciones existen (vea [**OPTIMIZACIÓN DE \_ CPU \_ D3DX).**](d3dx-cpu-optimization.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Math.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
