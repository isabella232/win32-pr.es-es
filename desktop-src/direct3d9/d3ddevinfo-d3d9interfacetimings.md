---
description: Porcentaje de tiempo de procesamiento de datos en el controlador. Estas estadísticas pueden ayudar a identificar los casos en los que el controlador está esperando otros recursos.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: D3DDEVINFO_D3D9INTERFACETIMINGS estructura (D3D9Types.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063747"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a>D3DDEVINFO \_ D3D9INTERFACETIMINGS (estructura)

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



## <a name="members"></a>Members

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha pasado esperando a que la GPU termine de usar un recurso bloqueado (no se especificó [D3DLOCK \_ DONOTWAIT).](d3dlock.md)

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador dedicó a esperar a que la GPU terminara de procesar algunos comandos antes de que el controlador pudiera enviar más. Esto indica que el controlador se ha quedó sin espacio para enviar comandos a la GPU.

</dd> <dt>

**WaitingForGPUToWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar a que la latencia de GPU se reduzca a menos de tres fotogramas de representación.

Si una aplicación está limitada por GPU, el controlador debe detener la CPU hasta que la GPU se entre en tres fotogramas. Esto evita que una aplicación haga cola en llamadas de representación de muchos segundos, lo que puede aumentar considerablemente la latencia entre el momento en que el usuario introduce nuevos datos y el momento en que el usuario ve los resultados de esa entrada. En general, el controlador puede realizar un seguimiento del número de veces que se llama a [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para evitar la cola de más de tres fotogramas del trabajo de representación.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar un recurso que no se puede canaliza (que se opera en paralelo). Es posible que una aplicación quiera evitar el uso de un recurso no canalizado por motivos de rendimiento.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar a otro procesamiento de GPU.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estas métricas ayudan a identificar cuándo está esperando un controlador y qué está esperando. Los porcentajes altos no son necesariamente un problema.

Estas métricas globales del sistema pueden implementarse o no. En función del hardware específico, es posible que estas métricas no admitan varias consultas simultáneamente.

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

 

 
