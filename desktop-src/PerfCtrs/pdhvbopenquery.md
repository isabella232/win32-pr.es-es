---
description: La función PdhVbOpenQuery crea e inicializa una estructura de consulta única que se usa para administrar la colección de datos de rendimiento.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: Función PdhVbOpenQuery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenQuery
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 70d207696f68b9ef86ba0bae1f596826bd6e400d05d011b330f67241e186f5eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962395"
---
# <a name="pdhvbopenquery-function"></a>Función PdhVbOpenQuery

La **función PdhVbOpenQuery** crea e inicializa una estructura de consulta única que se usa para administrar la colección de datos de rendimiento.

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbOpenQuery( \_ ByVal QueryHandle as Long \_ ) As Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variable que se borra (es igual a 0) antes de llamar a la función y, si la función se realiza correctamente, contiene el identificador único de la consulta que se crea y se abre. Este identificador se usa en las llamadas posteriores a otras funciones PDH para identificar la consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve un **entero Long** igual a ERROR SUCCESS y un nuevo identificador en la \_ variable *QueryHandle.*

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error [PDH](pdh-error-codes.md). A continuación se den los valores posibles.



| Código devuelto                                                                                                     | Descripción                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**PDH \_ INVALID \_ ARGUMENT**</dt> </dl>           | El argumento no es válido o incorrecto.<br/>             |
| <dl> <dt>**ERROR DE \_ ASIGNACIÓN DE \_ MEMORIA DE PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria temporal.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

