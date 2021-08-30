---
description: Proporciona una lista de todos los equipos que actualmente usan Monitor de red para capturar datos de red.
ms.assetid: 57e7b8e1-99b8-4194-b6dc-401235be4ef4
title: Método IRTC::QueryStations (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.QueryStations
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 951bdc096a432ae57004962f21c60d37f5fc44fec548a7e3364a5f8b28696da0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037255"
---
# <a name="irtcquerystations-method"></a>IrTC::QueryStations (método)

El **método QueryStations** proporciona una lista de todos los equipos que usan actualmente Monitor de red para capturar datos de red.

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

Puntero a una [**estructura QUERYTABLE.**](querytable.md) En la entrada, esta estructura debe contener el número máximo de equipos que desea Monitor de red y una matriz de [**estructuras STATIONQUERY.**](stationquery.md)

En la salida, esta estructura devuelve el número de equipos que capturan datos y una [**estructura STATIONQUERY**](stationquery.md) para cada equipo encontrado. Tenga en cuenta que esto puede incluir equipos que usan versiones de Monitor de red anteriores a la versión 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es **NMERR \_ SUCCESS**.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                           | Descripción                                                          |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**MEMORIA DE NMERR \_ \_ FUERA DE LA \_ MEMORIA**</dt> </dl> | La memoria necesaria para procesar esta consulta no está disponible.<br/> |



 

## <a name="remarks"></a>Comentarios

Se puede llamar a este método en cualquier momento después de llamar al método [**CreateNPPInterface.**](createnppinterface.md) Una llamada a este método es una llamada sincrónica, que puede tardar varios segundos en completarse mientras Monitor de red espera a que los equipos remotos respondan a la consulta. Solo se pueden consultar los equipos de la subred local.

El usuario debe asignar la memoria para la [**estructura QUERYTABLE**](querytable.md) y liberar esa memoria después de que la tabla ya no sea necesaria. Este requisito incluye la memoria necesaria para la [**matriz STATIONQUERY**](stationquery.md) utilizada en **QUERYTABLE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRTC**](irtc.md)
</dt> <dt>

[**Querytable**](querytable.md)
</dt> <dt>

[**STATIONQUERY**](stationquery.md)
</dt> </dl>

 

 




