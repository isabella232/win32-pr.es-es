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
ms.openlocfilehash: d7261096ed373620b8438ccce2d353ccf21f1c236028e8c829951fc64ee3725a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989035"
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



## <a name="members"></a>Miembros

<dl> <dt>

**WaitingForGPUToUseApplicationResourceTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar a que la GPU termine de usar un recurso bloqueado (y no se especificó [D3DLOCK \_ DONOTWAIT).](d3dlock.md)

</dd> <dt>

**WaitingForGPUToAcceptMoreCommandsTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador dedicó a esperar a que la GPU terminara de procesar algunos comandos antes de que el controlador pudiera enviar más. Esto indica que el controlador se ha quedo sin espacio para enviar comandos a la GPU.

</dd> <dt>

**WaitingForGPUToWithinLatencyTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar a que la latencia de GPU se reduzca a menos de tres fotogramas de representación.

Si una aplicación tiene un límite de GPU, el controlador debe detener la CPU hasta que la GPU se encuentra dentro de tres fotogramas. Esto evita que una aplicación haga cola durante muchos segundos de llamadas de representación, lo que puede aumentar drásticamente la latencia entre el momento en que el usuario introduce datos nuevos y el momento en que el usuario ve los resultados de esa entrada. En general, el controlador puede realizar un seguimiento del número de veces que se llama a [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) para evitar la cola de más de tres fotogramas de trabajo de representación.

</dd> <dt>

**WaitingForGPUExclusiveResourceTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar un recurso que no se puede canalizar (que se opera en paralelo). Es posible que una aplicación quiera evitar el uso de un recurso no canalizado por motivos de rendimiento.

</dd> <dt>

**WaitingForGPUOtherTimePercent**
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Porcentaje de tiempo que el controlador ha dedicado a esperar a otro procesamiento de GPU.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estas métricas ayudan a identificar cuándo está esperando un controlador y qué está esperando. Los porcentajes elevados no son necesariamente un problema.

Estas métricas globales del sistema pueden o no implementarse. Dependiendo del hardware específico, es posible que estas métricas no admitan varias consultas simultáneamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
