---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'IRTC:: GetTotalStatistics (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677651"
---
# <a name="irtcgettotalstatistics-method"></a>IRTC:: GetTotalStatistics (método)

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

Puntero a una estructura de [estadísticas](statistics.md) que proporciona las estadísticas totales de la captura. Es responsabilidad del llamador asignar y liberar la memoria que usa la estructura de **estadísticas** .

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
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl> | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/> |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>  | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                     |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl> | NPP no está capturando datos. Llame a [IRTC:: Start](irtc-start.md) para empezar a capturar datos.<br/>                         |



 

## <a name="remarks"></a>Observaciones

Este método devuelve los datos solo mientras una captura está en curso, incluso mientras la captura está en pausa.

Monitor de red también almacena [*estadísticas de conversación*](c.md). Para recuperar las estadísticas de conversación, llame al método [IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetConversationStatistics](irtc-getconversationstatistics.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> <dt>

[¡](statistics.md)
</dt> </dl>

 

 




