---
description: Función definida por la aplicación que libera la memoria asignada por la función AuthzComputeGroupsCallback. AuthzFreeGroupsCallback es un marcador de posición para el nombre de la función definida por la aplicación.
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
ms.openlocfilehash: 3cce78e261892fede79fb8fc76bc5b0d009342db3e0bf672be2854cb8492bcec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783769"
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

## <a name="remarks"></a>Comentarios

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

 

 




