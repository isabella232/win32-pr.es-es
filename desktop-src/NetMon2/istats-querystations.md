---
description: El método QueryStations proporciona una lista de todos los equipos que actualmente capturan datos mediante Monitor de red.
ms.assetid: feebcb28-914b-450e-95d4-10a60cbf1438
title: Método IStats::QueryStations (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2d4ead22b3e7308aee3c44b3ff6dff407591cbe675b09a3300f3e7a8720726c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742645"
---
# <a name="istatsquerystations-method"></a>Método IStats::QueryStations

El **método QueryStations** proporciona una lista de todos los equipos que actualmente capturan datos mediante Monitor de red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE QueryStations(
  [in, out] QUERYTABLE *lpQueryTable
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpQueryTable* \[ in, out\]
</dt> <dd>

Puntero a una [estructura QUERYTABLE.](querytable.md) En la entrada, esta estructura debe contener el número máximo de equipos que desea Monitor de red y una matriz de [estructuras STATIONQUERY.](stationquery.md)

En la salida, esta estructura devuelve el número de equipos que capturan datos y una [estructura STATIONQUERY](stationquery.md) para cada equipo encontrado. Tenga en cuenta que esta información puede incluir equipos que usan versiones de Monitor de red anteriores a la versión 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                           | Descripción                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl> | La memoria necesaria para procesar esta consulta no estaba disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface.](createnppinterface.md) Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse a medida Monitor de red espera a que los equipos remotos respondan a la consulta. Solo se pueden consultar los equipos de la subred local.

Es su responsabilidad asignar la memoria para la estructura [QUERYTABLE](querytable.md) y liberar esa memoria después de que la tabla ya no sea necesaria. Este requisito incluye la memoria necesaria para la [matriz STATIONQUERY](stationquery.md) utilizada en QUERYTABLE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[Querytable](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




