---
description: Quita el registro de proveedores.
ms.assetid: e52c1ee0-140a-4277-bddd-d93338a512bc
title: Función CounterCleanup
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071446"
---
# <a name="countercleanup-function"></a>Función CounterCleanup

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

El proveedor llama a esta función. La función llama a [**la función PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.

La [**herramienta CTRPP**](ctrpp.md) genera esta función insertda cuando se especifica el **argumento -o.** El nombre de la función incluye una cadena *de* prefijo si especifica el **argumento -prefix** (por ejemplo, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 




