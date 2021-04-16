---
description: Busca el siguiente fotograma en el contexto de captura actual que coincida con el filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Función FindNextFrame (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2e303f7f9031ad451ad19be8bc8cbcd3abae3f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540227"
---
# <a name="findnextframe-function"></a>FindNextFrame función)

La función **FindNextFrame** busca el siguiente fotograma en el contexto de captura actual que coincida con el filtro.

## <a name="syntax"></a>Sintaxis


```C++
HFRAME WINAPI FindNextFrame(
   HFRAME    hCurrentFrame,
   LPSTR     ProtocolName,
   LPADDRESS DestinationAddress,
   LPADDRESS SourceAddress,
   LPWORD    ProtocolOffset,
   DWORD     OriginalFrameNumber,
   DWORD     HighestFrame
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

El nombre del Protocolo, como TCP.

</dd> <dt>

*DestinationAddress* 
</dt> <dd>

Dirección de destino.

</dd> <dt>

*SourceAddress* 
</dt> <dd>

Dirección de origen.

</dd> <dt>

*ProtocolOffset* 
</dt> <dd>

Puntero a una **palabra** que recibirá el desplazamiento del protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto inicial de la búsqueda. De forma predeterminada, esta función realiza búsquedas hacia delante 1.000 fotogramas desde el punto de inicio *OriginalFrameNumber* . Para cambiar la distancia de búsqueda, agregue esta línea al archivo Nmapi.ini, situado en el \\ directorio monitor de red.

MAXLOOKBACK =<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

Número de fotograma más alto de la captura en el que se busca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un identificador del fotograma siguiente.

Si la función no es correcta, el valor devuelto es **null**.

## <a name="remarks"></a>Observaciones

El filtro de captura se define principalmente mediante el parámetro *ProtocolName* , que es la única entrada de filtro necesaria; puede agregar datos de *DestinationAddress* y *SourceAddress* para aumentar la velocidad de captura.

El puntero *ProtocolOffset* se devuelve al analizador que realiza la llamada, que agrega la **palabra** al puntero devuelto al bloquear el marco (con [ParserTemporaryLockFrame](parsertemporarylockframe.md)) para obtener el **LPBYTE** del protocolo que se busca. En la devolución, se proporciona al analizador el HFRAME que pasó el filtro. Si el analizador encuentra que este fotograma no es el que se busca, el analizador puede volver a HFRAME a la función **FindNextFrame** para obtener el fotograma siguiente. Las direcciones de origen y de destino no son necesarias y se pueden pasar como **null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




