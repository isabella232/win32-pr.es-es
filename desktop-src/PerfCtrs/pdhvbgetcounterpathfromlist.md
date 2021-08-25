---
description: La función PdhVbGetCounterPathFromList copia la ruta de acceso del contador a la que hace referencia el parámetro Index de una lista de rutas de acceso de contador creada por el usuario desde la llamada más reciente a la función PdhVbCreateCounterPathList.
ms.assetid: e77a022d-42f2-4c48-acb7-36cb013730dd
title: Función PdhVbGetCounterPathFromList
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
ms.openlocfilehash: 85760bbcdcc81204340004304be1f0c14bf9bcbbbd7a5b59eebf47a25f7b15c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033785"
---
# <a name="pdhvbgetcounterpathfromlist-function"></a>Función PdhVbGetCounterPathFromList

La función **PdhVbGetCounterPathFromList** copia la ruta de acceso del contador a la que hace referencia el parámetro *Index* de una lista de rutas de acceso de contador creada por el usuario desde la llamada más reciente a la función [**PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

> [!IMPORTANT]
> La función que describe este tema puede modificarse o no estar disponible en el futuro. En su lugar, Microsoft recomienda usar las funciones descritas en [Funciones de contadores de rendimiento](performance-counters-functions.md).

Función PdhVbGetCounterPathFromList( \_ ByVal Index As Long, \_ ByVal Buffer as String, \_ ByVal BufferLength As Long \_ ) as Long

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Index* 
</dt> <dd>

Índice de la ruta de acceso del contador que se recuperará. Debe ser un valor mayor o igual que 1 y menor o igual que el valor devuelto por la [**función PdhVbCreateCounterPathList.**](pdhvbcreatecounterpathlist.md)

</dd> <dt>

*Buffer* 
</dt> <dd>

Cadena dimensionada e inicializada que recibirá la ruta de acceso del contador que corresponde al valor del parámetro Index.

</dd> <dt>

*BufferLength* 
</dt> <dd>

Número máximo de caracteres que caben en la cadena a la que hace referencia Buffer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve el número de caracteres copiados en Buffer.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                               |
| Biblioteca<br/>                  | <dl> <dt>Pdh.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PdhVbCreateCounterPathList**](pdhvbcreatecounterpathlist.md)
</dt> <dt>

[**PdhVbGetCounterPathElements**](pdhvbgetcounterpathelements.md)
</dt> <dt>

[**PdhVbGetOneCounterPath**](pdhvbgetonecounterpath.md)
</dt> </dl>

 

 




