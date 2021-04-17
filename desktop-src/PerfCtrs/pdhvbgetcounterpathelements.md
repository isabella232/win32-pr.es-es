---
description: La función PdhVbGetCounterPathElements analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: PdhVbGetCounterPathElements función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathElements
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 003374141b0454d730ba4b844715bd6f00b544da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667313"
---
# <a name="pdhvbgetcounterpathelements-function"></a>PdhVbGetCounterPathElements función)

La función **PdhVbGetCounterPathElements** analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales. Cada una de las variables de cadena debe tener el mismo tamaño (*BufferSize*) y estar dimensionada e inicializada antes de que se use en esta función.

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Function PdhVbGetCounterPathElements ( \_ ByVal PathString As String, \_ ByVal MachineName As String, \_ ByVal objectname As String, \_ ByVal nombreDeInstancia As String, \_ ByVal ParentInstance As String, \_ ByVal Contraname As String, \_ ByVal BufferSize as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathString* 
</dt> <dd>

Cadena de ruta de acceso de contador que se va a dividir en sus elementos individuales.

</dd> <dt>

*MachineName* 
</dt> <dd>

Cadena que recibirá el nombre del equipo.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Cadena que va a recibir el nombre del objeto.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Cadena que recibirá el nombre de instancia, si se utiliza.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Cadena que recibirá la instancia primaria, si se utiliza.

</dd> <dt>

*CounterName* 
</dt> <dd>

Cadena que va a recibir el nombre del contador.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Tamaño máximo de cada variable de cadena utilizada como parámetro para esta llamada de función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve un entero **largo** igual a error de \_ éxito.

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un [código de error de PDH](pdh-error-codes.md). Los valores posibles son los siguientes.



| Código devuelto                                                                                                     | Descripción                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ argumento no válido \_**</dt> </dl>           | Uno o varios de los búferes de cadena no tienen el tamaño correcto.<br/>                          |
| <dl> <dt>**PDH \_ más \_ datos**</dt> </dl>                  | Uno o varios de los elementos de la ruta de acceso del contador son demasiado grandes para la longitud del búfer de retorno.<br/> |
| <dl> <dt>**\_error de \_ asignación de memoria de PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria temporal.<br/>                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

