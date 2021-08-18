---
description: La función PdhVbGetCounterPathElements analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales.
ms.assetid: 5459c7dd-e8b6-48cd-a33f-cafdc64dd9ee
title: Función PdhVbGetCounterPathElements
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
ms.openlocfilehash: fecd9ecac573ecc1a5afabcfc4a14bf6fd1ca5cee7b44387ea910b0cf1a5820d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011333"
---
# <a name="pdhvbgetcounterpathelements-function"></a>Función PdhVbGetCounterPathElements

La **función PdhVbGetCounterPathElements** analiza una cadena de ruta de acceso de contador de rendimiento completa en sus elementos individuales. Cada una de las variables de cadena debe tener el mismo tamaño *(BufferSize*) y tener dimensiones e inicializarse antes de que se utilice en esta función.

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetCounterPathElements( \_ ByVal PathString as String, \_ ByVal MachineName as String, \_ ByVal ObjectName as String, \_ ByVal InstanceName as String, \_ ByVal ParentInstance as String, \_ ByVal CounterName as String, \_ ByVal BufferSize as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathString* 
</dt> <dd>

Cadena de ruta de acceso de contador que se va a dividir en sus elementos individuales.

</dd> <dt>

*MachineName* 
</dt> <dd>

Cadena para recibir el nombre del equipo.

</dd> <dt>

*ObjectName* 
</dt> <dd>

Cadena para recibir el nombre del objeto.

</dd> <dt>

*InstanceName* 
</dt> <dd>

Cadena para recibir el nombre de instancia, si se usa.

</dd> <dt>

*ParentInstance* 
</dt> <dd>

Cadena para recibir la instancia primaria, si se usa.

</dd> <dt>

*CounterName* 
</dt> <dd>

Cadena para recibir el nombre del contador.

</dd> <dt>

*BufferSize* 
</dt> <dd>

Tamaño máximo de cada variable de cadena utilizada como parámetro para esta llamada de función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve un **entero Long** igual a ERROR \_ SUCCESS.

Si se produce un error en la función, el valor devuelto es un [código de error del sistema](/windows/desktop/Debug/system-error-codes) o un código de error [PDH](pdh-error-codes.md). A continuación se den los valores posibles.



| Código devuelto                                                                                                     | Descripción                                                                                    |
|-----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ INVALID \_ ARGUMENT**</dt> </dl>           | Uno o varios de los búferes de cadena no tienen el tamaño correcto.<br/>                          |
| <dl> <dt>**PDH \_ MORE \_ DATA**</dt> </dl>                  | Uno o varios de los elementos de la ruta de acceso del contador son demasiado grandes para la longitud del búfer devuelto.<br/> |
| <dl> <dt>**ERROR DE \_ ASIGNACIÓN DE \_ MEMORIA PDH \_**</dt> </dl> | No se pudo asignar un búfer de memoria temporal.<br/>                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

