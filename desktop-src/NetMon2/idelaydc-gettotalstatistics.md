---
description: 'Método IDelaydC::GetTotalStatistics: el método GetTotalStatistics recupera las estadísticas totales de la captura actual.'
ms.assetid: 904c7496-5603-41b9-8481-06fa31f6f112
title: Método IDelaydC::GetTotalStatistics (Netmon.h)
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
ms.openlocfilehash: e6b4d76b3035e156da1f1d4decf7a5c59b28bf0ca13bc2bdaa33e319422509af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037555"
---
# <a name="idelaydcgettotalstatistics-method"></a>Método IDelaydC::GetTotalStatistics

El **método GetTotalStatistics** recupera las [*estadísticas totales*](t.md) de la captura [*actual.*](c.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpStats* \[ out\]
</dt> <dd>

Puntero a una [estructura STATISTICS](statistics.md)que proporciona las estadísticas totales de la captura. Es responsabilidad del autor de la llamada asignar y liberar la memoria usada por la **estructura STATISTICS.**

</dd> <dt>

*fClearAfterReading* \[ En\]
</dt> <dd>

Marca que se usa para Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales. Una configuración **de TRUE** indica Monitor de red borrar el almacenamiento interno de las estadísticas totales después de recuperar la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red. Llame [a IDelaydC::Conectar](idelaydc-connect.md) para conectarse a la red.<br/> |
| <dl> <dt>**NMERR \_ NO \_ RETRASADO**</dt> </dl>   | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/>             |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl> | El NPP no captura datos. Llame [a IDelaydC::Start para](idelaydc-start.md) empezar a capturar datos.<br/>                 |



 

## <a name="remarks"></a>Comentarios

Este método devuelve datos solo mientras hay una captura en curso; cuando la captura está en pausa, las llamadas a este método no se realizará correctamente.

Monitor de red también almacena [*estadísticas*](c.md)de conversación, que se pueden recuperar llamando al método [IDelaydC::GetConversationStatistics.](idelaydc-getconversationstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::GetConversationStatistics](idelaydc-getconversationstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[Estadísticas](statistics.md)
</dt> </dl>

 

 




