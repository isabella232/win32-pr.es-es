---
description: La función FindPreviousFrame busca el fotograma anterior en el contexto de captura actual que coincida con el filtro.
ms.assetid: 16c5b981-a9f4-41e5-bb97-2caa3e9d8512
title: Función FindPreviousFrame (Netmon. h)
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
ms.openlocfilehash: deabf10702ca41c23101c5f60c9459e094e567fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000939"
---
# <a name="findpreviousframe-function"></a>FindPreviousFrame función)

La función **FindPreviousFrame** busca el fotograma anterior en el contexto de captura actual que coincida con el filtro.

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

Nombre del Protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Dirección de destino del fotograma que se busca.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Dirección de origen del marco que se busca.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Puntero a una **palabra** que recibe el desplazamiento del protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto de inicio de la búsqueda. De forma predeterminada, esta función busca fotogramas hacia atrás 1.000 desde el punto inicial de *OriginalFrameNumber* . Puede cambiar la distancia de la búsqueda mediante la adición de esta línea al archivo Nmapi.ini, que se encuentra en el \\ directorio monitor de red.

MAXLOOKBACK =<new lookback distance>

</dd> <dt>

*LowestFrame* 
</dt> <dd>

Número de fotograma más bajo de la captura en el que se busca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un identificador del fotograma anterior.

Si la función no es correcta, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

El filtro de captura se define principalmente mediante *ProtocolName*, que es la única entrada de filtro necesaria; puede agregar información de *DestinationAddress* y *SourceAddress* para aumentar la velocidad de captura.

*ProtocolOffset* se devuelve al analizador que realiza la llamada, que agrega este **valor DWORD** al puntero devuelto al bloquear el marco (con [PARSERTEMPORARYLOCKFRAME](parsertemporarylockframe.md)) para obtener el LPBYTE del protocolo que se está buscando. En la devolución, se proporciona al analizador el HFRAME que pasó el filtro. Si el analizador encuentra que el fotograma no es el que se está buscando, el analizador puede volver a HFRAME a la función **FindPreviousFrame** para recuperar el fotograma siguiente. Las direcciones de origen y de destino, que no son necesarias, se pueden pasar como **null**. Cuando se utiliza, estas direcciones pueden ser de tipo \_ dirección \_ IP, etc., no solo tipos Mac.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




