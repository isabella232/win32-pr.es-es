---
description: La función PdhVbAddCounter crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador cuando se completa correctamente.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: Función PdhVbAddCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbAddCounter
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 6605e2fb02edad23831b22334b960eaa2e89f23206673608500f248452094ea6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061153"
---
# <a name="pdhvbaddcounter-function"></a>Función PdhVbAddCounter

La **función PdhVbAddCounter** crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador cuando se completa correctamente.

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbAddCounter( \_ ByVal QueryHandle as long, \_ ByVal CounterPath as string, \_ ByVal CounterHandle as long \_ ) as long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

Identificador de la consulta a la que se va a asignar este contador. La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este valor.

</dd> <dt>

*CounterPath* 
</dt> <dd>

Cadena de texto que especifica el nombre de la ruta de acceso del contador que se agregará a la consulta. El contenido de esta cadena debe ser una ruta de acceso de contador válida, como se obtiene del explorador de contadores u otro origen.

</dd> <dt>

*CounterHandle* 
</dt> <dd>

Referencia única que identifica este contador en la consulta. Esta variable debe inicializarse en cero antes de llamar a la función. Contiene un valor válido en la devolución solo si la función se completa correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve un **entero Long** igual a ERROR SUCCESS y un nuevo identificador en la \_ variable *CounterHandle.*

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error [PDH](pdh-error-codes.md). Los siguientes son valores posibles.



| Código devuelto                                                                                                     | Descripción                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ INVALID \_ ARGUMENT**</dt> </dl>           | Uno o varios de los argumentos no son válidos o incorrectos.<br/>              |
| <dl> <dt>**ERROR DE \_ ASIGNACIÓN DE \_ MEMORIA PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria.<br/>                            |
| <dl> <dt>**IDENTIFICADOR NO VÁLIDO de PDH \_ \_**</dt> </dl>             | El identificador de consulta no es válido.<br/>                                     |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ COUNTER**</dt> </dl>        | No se encontró el contador especificado.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ OBJECT**</dt> </dl>         | No se encontró el objeto especificado.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ NO \_ MACHINE**</dt> </dl>        | No se pudo crear una entrada de equipo.<br/>                             |
| <dl> <dt>**PDH \_ CSTATUS \_ BAD \_ COUNTERNAME**</dt> </dl>   | Se pasó una cadena de ruta de acceso de nombre de contador vacía.<br/>                   |
| <dl> <dt>**FUNCIÓN PDH \_ \_ NO \_ ENCONTRADA**</dt> </dl>        | No se pudo determinar la función de cálculo para este contador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

