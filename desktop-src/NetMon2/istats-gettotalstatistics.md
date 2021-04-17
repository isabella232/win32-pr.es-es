---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: 'IStas:: GetTotalStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 51cdbfdcc796aa7d8091e8da5837809efaa63379
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678182"
---
# <a name="istatsgettotalstatistics-method"></a>IStas:: GetTotalStatistics (método)

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

Marca usada para indicar a Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales. Un valor TRUE indica a Monitor de red que borre el almacenamiento interno de las estadísticas totales una vez recuperada la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                            | Descripción                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>   | NPP no está conectado a la red. Llame al método [istas:: Connect](istats-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no \_ solo estadísticas \_**</dt> </dl> | NPP está conectado a la red, pero no con el método [istas:: Connect](istats-connect.md) .<br/>                                |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>   | NPP no está capturando datos. Llame al método [istas:: Start](istats-start.md) para empezar a capturar datos.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Este método devuelve los datos solo mientras una captura está en curso, incluso mientras la captura está en pausa.

Monitor de red también almacena [*estadísticas de conversación*](c.md), que se pueden recuperar llamando al método [istas:: GetConversationStatistics](istats-getconversationstatistics.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IStas](istats.md)
</dt> <dt>

[ISta:: Connect](istats-connect.md)
</dt> <dt>

[IStas:: GetConversationStatistics](istats-getconversationstatistics.md)
</dt> <dt>

[IStas:: Start,](istats-start.md)
</dt> <dt>

[¡](statistics.md)
</dt> </dl>

 

 




