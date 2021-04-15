---
description: Porcentaje de tiempo de procesamiento de datos en el controlador. Estas estadísticas pueden ayudar a identificar los casos en los que el controlador está esperando otros recursos.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS estructura (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649403"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ estructura D3D9INTERFACETIMINGS

Porcentaje de tiempo de procesamiento de datos en el controlador. Estas estadísticas pueden ayudar a identificar los casos en los que el controlador está esperando otros recursos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador invierte en esperar a que la GPU termine de usar un recurso bloqueado (no se especificó [D3DLOCK \_ DONOTWAIT](d3dlock.md) ).

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador invierte en esperar a que la GPU termine de procesar algunos comandos antes de que el controlador pudiera enviar más. Esto indica que el controlador se ha quedado sin espacio para enviar comandos a la GPU.

</dd> <dt>

**WaitingForGPUToStayWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador invierte en esperar a que la latencia de la GPU se reduzca a menos de tres fotogramas de representación.

Si una aplicación está limitada por GPU, el controlador debe detenerla hasta que la GPU se encuentre dentro de tres fotogramas. Esto evita que una aplicación se incluya en la cola de llamadas de representación de muchos segundos, lo que puede aumentar drásticamente la latencia entre el momento en que el usuario introduce datos nuevos y el momento en que el usuario ve los resultados de dicha entrada. En general, el controlador puede realizar un seguimiento del número [**de veces que**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) se llama a para evitar poner en cola más de tres fotogramas de trabajo de representación.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador invierte en esperar un recurso que no se puede canalizar (se opera en paralelo). Una aplicación puede querer evitar el uso de un recurso no canalizado por razones de rendimiento.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador invierte en esperar a otro procesamiento de GPU.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estas métricas ayudan a identificar cuándo un controlador está esperando y qué está esperando. Los porcentajes altos no son necesariamente un problema.

Estas métricas globales del sistema pueden implementarse o no. En función del hardware específico, es posible que estas métricas no admitan varias consultas simultáneamente.

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

 

 
