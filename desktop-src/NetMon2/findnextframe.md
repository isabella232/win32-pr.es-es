---
description: Busca el siguiente fotograma en el contexto de captura actual que coincide con el filtro.
ms.assetid: cc99b4a0-b6b0-43b4-8121-0e402d024009
title: Función FindNextFrame (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253820"
---
# <a name="findnextframe-function"></a>Función FindNextFrame

La **función FindNextFrame** busca el siguiente fotograma en el contexto de captura actual que coincide con el filtro.

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

Nombre del protocolo, como TCP.

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

Puntero a una **palabra que** recibirá el desplazamiento del protocolo.

</dd> <dt>

*OriginalFrameNumber* 
</dt> <dd>

Punto inicial de la búsqueda. De forma predeterminada, esta función busca 1000 fotogramas hacia delante desde el punto inicial *OriginalFrameNumber.* Para cambiar la distancia de búsqueda hacia delante, agregue esta línea al archivo Nmapi.ini, que se encuentra en el \\ directorio Monitor de red búsqueda.

MAXLOOKBACK=<new lookforward distance>

</dd> <dt>

*HighestFrame* 
</dt> <dd>

Número de fotograma más alto de la captura en la que se busca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un identificador para el fotograma siguiente.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

El filtro de captura se define principalmente mediante el *parámetro ProtocolName,* que es la única entrada de filtro necesaria; Puede agregar los *datos DestinationAddress* y *SourceAddress* para aumentar la velocidad de captura.

El *puntero ProtocolOffset* se devuelve al analizador de llamadas, que agrega **la** palabra al puntero devuelto bloqueando el marco [(con ParserTemporaryLockFrame)](parsertemporarylockframe.md)para obtener el **LPBYTE** del protocolo que se busca. En la devolución, el HFRAME que pasó el filtro se da al analizador. Si el analizador descubre que este marco no es el que se busca, el analizador puede devolver el HFRAME a la función **FindNextFrame** para obtener el fotograma siguiente. Las direcciones de origen y destino no son necesarias y se pueden pasar como **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




