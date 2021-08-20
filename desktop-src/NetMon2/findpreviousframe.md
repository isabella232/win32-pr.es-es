---
description: La función FindPreviousFrame busca el marco anterior en el contexto de captura actual que coincide con el filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Función FindPreviousFrame (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindPreviousFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a3bd6378691b63fc7f4db2455f713ffd0cf2a0281da2411dc494244ad3f00ba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117982532"
---
# <a name="findpreviousframe-function"></a>Función FindPreviousFrame

La **función FindPreviousFrame** busca el marco anterior en el contexto de captura actual que coincide con el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HFRAME WINAPI FindPreviousFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     LowestFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hCurrentFrame* 
</dt> <dd>

Identificador del marco.

</dd> <dt>

*ProtocolName* 
</dt> <dd>

Nombre del protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Dirección de destino del marco que se busca.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Dirección de origen del marco que se busca.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Puntero a una **palabra que** recibe el desplazamiento del protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto inicial de la búsqueda. De forma predeterminada, esta función busca hacia atrás 1000 fotogramas desde el *punto inicial OriginalFrameNumber.* Puede cambiar la distancia de búsqueda atrás agregando esta línea al archivo Nmapi.ini, que se encuentra en el \\ directorio Monitor de red búsqueda.

MAXLOOKBACK=<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Número de fotograma más bajo de la captura en la que se busca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador del marco anterior.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Comentarios

El filtro de captura se define principalmente mediante *ProtocolName*, que es la única entrada de filtro necesaria; Puede agregar información *de DestinationAddress* *y SourceAddress* para aumentar la velocidad de captura.

*ProtocolOffset* se devuelve al analizador de llamadas, que agrega este **DWORD** al puntero devuelto bloqueando el marco [(con ParserTemporaryLockFrame)](parsertemporarylockframe.md)para obtener el LPBYTE del protocolo que se está buscando. En la devolución, el HFRAME que pasó el filtro se da al analizador. Si el analizador encuentra que el marco no es el que se busca, el analizador puede devolver este HFRAME a la función **FindPreviousFrame** para recuperar el fotograma siguiente. Las direcciones de origen y destino, que no son necesarias, se pueden pasar como **NULL.** Cuando se usan, estas direcciones pueden ser de tipo ADDRESS \_ TYPE \_ IP, y así sucesivamente, no solo tipos MAC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




