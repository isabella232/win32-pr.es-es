---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: 'IDelaydC:: GetTotalStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0d194426933532fcf7a1965ed59b099489eefcb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423679"
---
# <a name="idelaydcgettotalstatistics-method"></a>IDelaydC:: GetTotalStatistics (método)

El método **GetTotalStatistics** recupera las [*Estadísticas totales*](t.md) de la [*captura*](c.md)actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ enuncia\]
</dt> <dd>

Puntero a una estructura de [estadísticas](statistics.md)que proporciona las estadísticas totales de la captura. Es responsabilidad del autor de la llamada asignar y liberar la memoria que usa la estructura de **estadísticas** .

</dd> <dt>

*fClearAfterReading* \[ de\]
</dt> <dd>

Marca usada para indicar a Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales. Un valor **true** indica a monitor de red que borre el almacenamiento interno de las estadísticas totales una vez recuperada la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl> | NPP no está conectado a la red. Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectarse a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>   | NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>             |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl> | NPP no está capturando datos. Llame a [IDelaydC:: Start](idelaydc-start.md) para empezar a capturar datos.<br/>                 |



 

## <a name="remarks"></a>Observaciones

Este método devuelve los datos solo mientras una captura está en curso; Cuando se pausa la captura, las llamadas a este método no se realizarán correctamente.

Monitor de red también almacena [*estadísticas de conversación*](c.md), que se pueden recuperar llamando al método [IDelaydC:: GetConversationStatistics](idelaydc-getconversationstatistics.md) .

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

[IDelaydC:: Connect](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[¡](statistics.md)
</dt> </dl>

 

 




