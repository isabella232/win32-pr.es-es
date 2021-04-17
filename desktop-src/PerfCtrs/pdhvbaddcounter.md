---
description: La función PdhVbAddCounter crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador después de la finalización correcta.
ms.assetid: 20a9e6cd-bf0d-497d-b660-88e786e2f004
title: PdhVbAddCounter función)
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
ms.openlocfilehash: 19f97abeec74af0d08f340b70aa139e1bec7bf1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667315"
---
# <a name="pdhvbaddcounter-function"></a>PdhVbAddCounter función)

La función **PdhVbAddCounter** crea una entrada de contador en el objeto de consulta especificado y devuelve un identificador a ese contador después de la finalización correcta.

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbAddCounter ( \_ ByVal QueryHandle as Long, \_ ByVal Perpath As String, \_ ByVal contrahandle as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*QueryHandle* 
</dt> <dd>

IDENTIFICADOR de la consulta a la que se va a asignar este contador. La función [**PdhVbOpenQuery**](pdhvbopenquery.md) devuelve este valor.

</dd> <dt>

*CounterPath* 
</dt> <dd>

Cadena de texto que especifica el nombre de la ruta de acceso del contador que se va a agregar a la consulta. El contenido de esta cadena debe ser una ruta de acceso de contador válida, como se obtiene del explorador de contadores u otro origen.

</dd> <dt>

*Control de contracargo* 
</dt> <dd>

Referencia única que identifica este contador en la consulta. Esta variable se debe inicializar en cero antes de que se llame a la función. Contiene un valor válido en la devolución solo si la función se completa correctamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error \_ correcto y un nuevo identificador en la variable de control de *supercontrolador* .

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md). Los valores posibles son los siguientes.



| Código devuelto                                                                                                     | Descripción                                                                   |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ argumento no válido \_**</dt> </dl>           | Uno o varios argumentos no son válidos o son incorrectos.<br/>              |
| <dl> <dt>**\_error de \_ asignación de memoria de PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria.<br/>                            |
| <dl> <dt>**\_identificador no válido de PDH \_**</dt> </dl>             | El identificador de consulta no es válido.<br/>                                     |
| <dl> <dt>**\_CSTATUS \_ no \_ contador de PDH**</dt> </dl>        | No se encontró el contador especificado.<br/>                               |
| <dl> <dt>**PDH \_ CSTATUS \_ ningún \_ objeto**</dt> </dl>         | No se encontró el objeto especificado.<br/>                           |
| <dl> <dt>**PDH \_ CSTATUS \_ sin \_ equipo**</dt> </dl>        | No se pudo crear una entrada de equipo.<br/>                             |
| <dl> <dt>**\_ \_ nombre incorrecto de PDH CSTATUS \_**</dt> </dl>   | Se pasó una cadena de ruta de acceso de nombre de contador vacía.<br/>                   |
| <dl> <dt>**\_ \_ no \_ se encontró la función PDH**</dt> </dl>        | No se pudo determinar la función de cálculo para este contador.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbOpenQuery**](pdhvbopenquery.md)
</dt> </dl>

 

