---
description: La función PdhVbGetOneCounterPath muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador.
ms.assetid: a42406ef-70e0-464d-90f8-fef9e1c3471d
title: Función PdhVbGetOneCounterPath
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069187"
---
# <a name="pdhvbgetonecounterpath-function"></a>Función PdhVbGetOneCounterPath

La **función PdhVbGetOneCounterPath** muestra un cuadro de diálogo que permite al usuario examinar los contadores de rendimiento disponibles y seleccionar un contador. El contador seleccionado se devuelve en la variable *PathString.* La variable *PathString* se debe dimensionar e inicializar antes de llamar a esta función, y la variable *PathLength* debe indicar el tamaño dimensionado.

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetOneCounterPath( \_ ByVal PathString as String, \_ ByVal PathLength As Long, \_ ByVal DetailLevel as Long, \_ ByVal CaptionString as String \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*PathString* 
</dt> <dd>

Variable de cadena inicializada que se usa para recibir la ruta de acceso del contador seleccionada por el usuario.

</dd> <dt>

*PathLength* 
</dt> <dd>

Longitud del objeto PathString inicializado.

</dd> <dt>

*DetailLevel* 
</dt> <dd>

Tipos de contadores que se mostrarán en el cuadro de diálogo. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                               | Significado                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PERF_DETAIL_ADVANCED"></span><span id="perf_detail_advanced"></span><dl> <dt>**DETALLES \_ AVANZADOS DE PERF \_**</dt> </dl> | Contadores que es probable que el usuario avanzado comprenda, además de los contadores de usuario principiante.<br/>                                            |
| <span id="PERF_DETAIL_EXPERT"></span><span id="perf_detail_expert"></span><dl> <dt>**PERF \_ DETAIL \_ EXPERT**</dt> </dl>       | Contadores que es probable que el usuario experto y el desarrollador de software comprendan, además de los contadores para los usuarios principiantes y avanzados.<br/> |
| <span id="PERF_DETAIL_NOVICE"></span><span id="perf_detail_novice"></span><dl> <dt>**PERF \_ DETAIL \_ NOVICE**</dt> </dl>       | Solo los contadores que es probable que comprenda el usuario principiante.<br/>                                                                                  |
| <span id="PERF_DETAIL_WIZARD"></span><span id="perf_detail_wizard"></span><dl> <dt>**ASISTENTE PARA DETALLES \_ DE PERF \_**</dt> </dl>       | Todos los contadores del sistema.<br/>                                                                                                                  |



 

</dd> <dt>

*CaptionString* 
</dt> <dd>

Variable de cadena que contiene el texto que se mostrará en la barra de título del cuadro de diálogo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de caracteres escritos en el búfer *PathString.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetCounterPathFromList**](pdhvbgetcounterpathfromlist.md)
</dt> </dl>

 

 




