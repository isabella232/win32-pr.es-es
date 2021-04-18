---
description: La función PdhVbGetCounterPathFromList copia la ruta de acceso del contador a la que hace referencia el parámetro de índice de una lista de rutas de acceso de contador creada por el usuario a partir de la llamada más reciente a la función PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: PdhVbGetCounterPathFromList función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetCounterPathFromList
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 4c5ae4632ede898b7cd323723037ea68d53455b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667311"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>PdhVbGetCounterPathFromList función)

La función **PdhVbGetCounterPathFromList** copia la ruta de acceso del contador a la que hace referencia el parámetro de *Índice* de una lista de rutas de acceso de contador creada por el usuario a partir de la llamada más reciente a la función [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

> [!IMPORTANT]
> La función que se describe en este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda que use las funciones descritas en [funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetCounterPathFromList ( \_ ByVal index as Long, \_ ByVal buffer As String, \_ ByVal BufferLength as Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Índice de la ruta de acceso del contador que se va a recuperar. Debe ser un valor mayor o igual que 1 y menor o igual que el valor devuelto por la función [**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md) .

</dd> <dt>

*Buffer* 
</dt> <dd>

Cadena dimensionada e inicializada que recibirá la ruta de acceso del contador que corresponde al valor del parámetro de índice.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Número máximo de caracteres que caben en la cadena a la que hace referencia el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de caracteres copiados en el búfer.

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

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




