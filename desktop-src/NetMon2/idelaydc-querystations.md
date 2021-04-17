---
description: El método QueryStations proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos.
ms.assetid: 8e578f50-685e-4799-90ca-5da8810ec2a3
title: 'IDelaydC:: QueryStations (método) (Netmon. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686565"
---
# <a name="idelaydcquerystations-method"></a>IDelaydC:: QueryStations (método)

El método **QueryStations** proporciona una lista de todos los equipos que usan actualmente monitor de red para capturar datos.

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

Puntero a una estructura de [QUERYTABLE](querytable.md) . En la entrada, esta estructura debe contener el número máximo de equipos que desea que devuelva Monitor de red y una matriz de estructuras [STATIONQUERY](stationquery.md) .

En la salida, esta estructura devuelve el número de equipos que capturan datos y una estructura [STATIONQUERY](stationquery.md) para cada equipo encontrado. Tenga en cuenta que esta lista puede incluir equipos con versiones de Monitor de red esa versión previa 2,0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es el siguiente código de error:



| Código devuelto                                                                                           | Descripción                                               |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**NMERR \_ \_ de \_ memoria insuficiente**</dt> </dl> | No había memoria disponible para procesar esta consulta.<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a este método en cualquier momento después de llamar a [CreateNPPInterface](createnppinterface.md) . Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse como Monitor de red espera a que los equipos remotos respondan a la consulta. Solo se pueden consultar los equipos de la subred local.

Es su responsabilidad asignar la memoria para [la estructura de la tabla de](querytable.md) paginación y liberar esa memoria después de que la tabla ya no se necesite. Este requisito incluye la memoria necesaria para la matriz [STATIONQUERY](stationquery.md) utilizada en la tabla de cambios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[QUERYTABLE](querytable.md)
</dt> <dt>

[STATIONQUERY](stationquery.md)
</dt> </dl>

 

 




