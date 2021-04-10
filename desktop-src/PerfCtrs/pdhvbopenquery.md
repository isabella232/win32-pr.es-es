---
description: La función PdhVbOpenQuery crea e inicializa una estructura de consulta única que se utiliza para administrar la colección de datos de rendimiento.
ms.assetid: 9cf535ef-76ad-4773-8414-8e289f3c52f6
title: PdhVbOpenQuery función)
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
ms.openlocfilehash: c657f033e2e972473218f2b283e03b11659d9f2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156524"
---
# <a name="pdhvbopenquery-function"></a>PdhVbOpenQuery función)

La función **PdhVbOpenQuery** crea e inicializa una estructura de consulta única que se utiliza para administrar la colección de datos de rendimiento.

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbOpenQuery ( \_ ByVal QueryHandle as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Variable que está desactivada (es igual a 0) antes de que se llame a la función y, si la función es correcta, contiene el identificador único de la consulta que se crea y se abre. Este identificador se utiliza en las llamadas subsiguientes a otras funciones de PDH para identificar la consulta.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error \_ correcto y un nuevo identificador en la variable *QueryHandle* .

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md). Los valores posibles son los siguientes.



| Código devuelto                                                                                                     | Descripción                                                  |
|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <dt>**PDH \_ argumento no válido \_**</dt> </dl>           | El argumento no es válido o es incorrecto.<br/>             |
| <dl> <dt>**\_error de \_ asignación de memoria de PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria temporal.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhCloseQuery**](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
</dt> </dl>

 

