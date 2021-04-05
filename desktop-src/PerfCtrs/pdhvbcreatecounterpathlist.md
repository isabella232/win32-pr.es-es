---
description: La función PdhVbCreateCounterPathList muestra el cuadro de diálogo exploración de contadores de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento. Cada ruta de acceso de contador seleccionada se debe leer mediante la función PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: PdhVbCreateCounterPathList función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbCreateCounterPathList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: bef484846507bf68d8ccfc0ad3ea10a250b83133
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909734"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>PdhVbCreateCounterPathList función)

La función **PdhVbCreateCounterPathList** muestra el cuadro de diálogo exploración de contadores de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento. Cada ruta de acceso de contador seleccionada se debe leer mediante la función [**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md) .

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

La función PdhVbCreateCounterPathList ( \_ ByVal DetailLevel as Long, \_ ByVal CaptionString As String \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores que se van a mostrar en el cuadro de diálogo. Use uno de los siguientes valores.



| Value                                                                                                                                                                               | Significado                                                                                                                                                 |
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

La función devuelve el número de rutas de acceso de contador que el usuario seleccionó.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>PDH. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




