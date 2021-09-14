---
description: El método QueryStations proporciona una lista de todos los equipos que actualmente usan Monitor de red para capturar datos.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: Método IDelaydC::QueryStations (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 5a45f5046dbd2e5714424baf42621e0c1d5539ac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171418"
---
# <a name="idelaydcquerystations-method"></a>IDelaydC::QueryStations (método)

El **método QueryStations** proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos.

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

En la salida, esta estructura devuelve el número de equipos que capturan datos y una [estructura STATIONQUERY](stationquery.md) para cada equipo encontrado. Tenga en cuenta que esta lista puede incluir equipos que usan versiones de Monitor de red anteriores a la versión 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es el código de error siguiente:



| Código devuelto                                                                                           | Descripción                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl> | No había memoria disponible para procesar esta consulta.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface.](createnppinterface.md) Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse Monitor de red espera a que los equipos remotos respondan a la consulta. Solo se pueden consultar los equipos de la subred local.

Es su responsabilidad asignar la memoria para la estructura [QUERYTABLE](querytable.md) y liberar esa memoria después de que la tabla ya no sea necesaria. Este requisito incluye la memoria necesaria para la [matriz STATIONQUERY](stationquery.md) usada en QUERYTABLE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[QUERYTABLE](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




