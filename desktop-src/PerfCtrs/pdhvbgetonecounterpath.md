---
description: La función PdhVbGetOneCounterPath muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: PdhVbGetOneCounterPath función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetOneCounterPath
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 980665372d49f483e3fb59b7571ec38fa9c2851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909730"
---
# <a name="pdhvbgetonecounterpath-function"></a>PdhVbGetOneCounterPath función)

La función **PdhVbGetOneCounterPath** muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador. El contador seleccionado se devuelve en la variable *PathString* . La variable *PathString* se debe dimensionar e inicializar antes de que se llame a esta función, y la variable *PathLength* debe indicar el tamaño de la dimensión.

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetOneCounterPath ( \_ ByVal PathString As String, \_ ByVal PathLength as Long, \_ ByVal DetailLevel as Long, \_ ByVal CaptionString As String \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathString* 
</dt> <dd>

Variable de cadena inicializada utilizada para recibir la ruta de acceso del contador seleccionada por el usuario.

</dd> <dt>

*PathLength* 
</dt> <dd>

Longitud del PathString inicializado.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores que se van a mostrar en el cuadro de diálogo. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**detalle de rendimiento \_ \_ avanzado**</dt> </dl> | Contadores que es probable que el usuario avanzado entienda, además de los contadores de usuario inexperto.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**\_experto en detalles de rendimiento \_**</dt> </dl>       | Los contadores que es probable que comprenda el desarrollador de software y el usuario experto, además de los contadores para los usuarios principiantes y avanzados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**\_experto en detalles de rendimiento \_**</dt> </dl>       | Solo los contadores que es probable que comprenda el usuario principiante.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**\_Asistente para detalles de rendimiento \_**</dt> </dl>       | Todos los contadores del sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variable de cadena que contiene el texto que se mostrará en la barra de título del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de caracteres que se escriben en el búfer de *PathString* .

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

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




