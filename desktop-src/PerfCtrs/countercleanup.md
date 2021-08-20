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
ms.openlocfilehash: fe06923849a12609b6662505df94c927c3d9dfd4aeb8bc6a42bd6a225e042ef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011373"
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

## <a name="remarks"></a>Comentarios

El proveedor llama a esta función. La función llama a [**la función PerfStopProvider**](/windows/desktop/api/Perflib/nf-perflib-perfstopprovider) para quitar el registro del proveedor.

La [**herramienta CTRPP**](ctrpp.md) genera esta función insertda cuando se especifica el **argumento -o.** El nombre de la función incluye una cadena *de* prefijo si especifica el **argumento -prefix** (por ejemplo, **_prefix_CounterCleanup**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/> |



 

 




