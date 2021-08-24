---
description: La función PdhVbCreateCounterPathList muestra el cuadro de diálogo de exploración del contador de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento. A continuación, se debe leer cada ruta de acceso de contador seleccionada mediante la función PdhVbGetCounterPathFromList.
ms.assetid: 8dda528f-2e06-4726-89a0-095781a2f80d
title: Función PdhVbCreateCounterPathList
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
ms.openlocfilehash: 6471fe3baee14fa1853810b66a804974b05ca84d0db9bc4e7dd805085ad5c0c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775555"
---
# <a name="pdhvbcreatecounterpathlist-function"></a>Función PdhVbCreateCounterPathList

La **función PdhVbCreateCounterPathList** muestra el cuadro de diálogo de exploración del contador de rendimiento, que permite al usuario seleccionar varios contadores de rendimiento. A continuación, se debe leer cada ruta de acceso de contador seleccionada mediante [**la función PdhVbGetCounterPathFromList.**](pdhvbgetcounterpathfromlist.md)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Function PdhVbCreateCounterPathList( \_ ByVal DetailLevel As Long, \_ ByVal CaptionString As String \_ ) As Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores que se mostrarán en el cuadro de diálogo. Use uno de los siguientes valores.



| Value                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**DETALLES \_ AVANZADOS DE PERF \_**</dt> </dl> | Contadores que es probable que el usuario avanzado comprenda, además de los contadores de usuario principiante.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**PERF \_ DETAIL \_ EXPERT**</dt> </dl>       | Contadores que es probable que el usuario experto y el desarrollador de software entiendan, además de los contadores para los usuarios principiantes y avanzados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**PERF \_ DETAIL \_ NOVICE**</dt> </dl>       | Solo los contadores que es probable que el usuario principiante entienda.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**ASISTENTE PARA DETALLES \_ DE PERF \_**</dt> </dl>       | Todos los contadores del sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variable de cadena que contiene el texto que se mostrará en la barra de título del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de rutas de acceso de contador que seleccionó el usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




