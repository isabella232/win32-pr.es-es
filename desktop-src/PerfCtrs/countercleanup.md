---
description: Quita el registro de proveedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Función de limpieza
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterCleanup
api_type:
- NA
api_location: ''
ms.openlocfilehash: eb768d3152aad5401c30b18a3f1ff13d1ef2397d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667341"
---
# <a name="countercleanup-function"></a>Función de limpieza

Quita el registro del proveedor.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI CounterCleanup(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El proveedor llama a esta función. La función llama a la función [**PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.

La herramienta [**CTRPP**](ctrpp.md) genera esta función insertada al especificar el argumento **-o** . El nombre de la función incluye una cadena de *prefijo* si se especifica el argumento **-prefix** (por ejemplo, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/> |



 

 




