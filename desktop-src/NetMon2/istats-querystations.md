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
ms.openlocfilehash: 99c3be3926191c27ad038034373e411b5c22d9fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071541"
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

Puntero a una [estructura QUERYTABLE.](querytable.md) En la entrada, esta estructura debe contener el número máximo de equipos que Monitor de red devolver y una matriz de [estructuras STATIONQUERY.](stationquery.md)

En la salida, esta estructura devuelve el número de equipos que capturan datos y una [estructura STATIONQUERY](stationquery.md) para cada equipo encontrado. Tenga en cuenta que esta información puede incluir equipos que usan versiones de Monitor de red que son anteriores a la versión 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                           | Descripción                                                           |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl> | La memoria necesaria para procesar esta consulta no estaba disponible.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface.](createnppinterface.md) Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse a medida que Monitor de red espera a que los equipos remotos respondan a la consulta. Solo se pueden consultar los equipos de la subred local.

Es su responsabilidad asignar la memoria para la estructura [QUERYTABLE](querytable.md) y liberar esa memoria después de que la tabla ya no sea necesaria. Este requisito incluye la memoria necesaria para la [matriz STATIONQUERY](stationquery.md) usada en QUERYTABLE.

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

[QUERYTABLE](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




