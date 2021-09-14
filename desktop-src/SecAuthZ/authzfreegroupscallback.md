---
description: Función definida por la aplicación que libera memoria asignada por la función AuthzComputeGroupsCallback. AuthzFreeGroupsCallback es un marcador de posición para el nombre de la función definida por la aplicación.
ms.assetid: 5563311c-2bd1-4e96-ba0a-5a4225050f77
title: Función de devolución de llamada AuthzFreeGroupsCallback
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeGroupsCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7d8942acbc67f122ea79f0b9e98793628b5f21f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071199"
---
# <a name="authzfreegroupscallback-callback-function"></a>Función de devolución de llamada AuthzFreeGroupsCallback

La **función AuthzFreeGroupsCallback** es una función definida por la aplicación que libera la memoria asignada por la función [**AuthzComputeGroupsCallback.**](authzcomputegroupscallback.md) **AuthzFreeGroupsCallback es** un marcador de posición para el nombre de la función definida por la aplicación.

## <a name="syntax"></a>Sintaxis


```C++
void CALLBACK AuthzFreeGroupsCallback(
  _In_ PSID_AND_ATTRIBUTES pSidAttrArray
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSidAttrArray* \[ En\]
</dt> <dd>

Puntero a la memoria asignada por [**AuthzComputeGroupsCallback.**](authzcomputegroupscallback.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función de devolución de llamada no devuelve un valor.

## <a name="remarks"></a>Observaciones

Las variables de atributo deben tener el formato de una expresión cuando se usan con operadores lógicos; De lo contrario, se evalúan como desconocidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |
| Redistribuible<br/>          | Windows Paquete de herramientas de administración de Server 2003 en Windows XP<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones Access Control básicas](authorization-functions.md)
</dt> <dt>

[**AuthzComputeGroupsCallback**](authzcomputegroupscallback.md)
</dt> </dl>

 

 




