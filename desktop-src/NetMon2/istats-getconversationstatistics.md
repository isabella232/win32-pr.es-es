---
description: Recupera información de la sesión y la estación sobre la captura actual.
ms.assetid: 7fc436fc-b569-402d-a1ea-c1bb65de8a9e
title: Método IStats::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8e76bad23d79e261a27df5b83a94d4e477b21cde5057bb2587ffb49c93382df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890345"
---
# <a name="istatsgetconversationstatistics-method"></a>Método IStats::GetConversationStatistics

El **método GetConversationStatistics** recupera información de sesión y estación sobre la captura actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE GetConversationStatistics(
  [out] DWORD          *nSessions,
  [out] LPSESSIONSTATS lpSessionStats,
  [out] DWORD          *nStations,
  [out] LPSTATIONSTATS lpStationStats,
  [in]  BOOL           fClearAfterReading
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nSessions* \[ out\]
</dt> <dd>

Puntero a un DWORD que contiene el número de [*sesiones*](s.md) registradas para la captura actual.

</dd> <dt>

*lpSessionStats* \[ out\]
</dt> <dd>

Puntero a una [**estructura SESSIONSTATS.**](sessionstats.md)

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Puntero a un DWORD que contiene el número de [*estaciones registradas*](s.md) para la captura actual.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Puntero a una [**estructura STATIONSTATS.**](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ En\]
</dt> <dd>

Marca usada para indicar Monitor de red borrar el almacenamiento interno de las estructuras [**SESSIONSTATS**](sessionstats.md) y [**STATIONSTATS**](stationstats.md) después de recuperar los datos actuales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                   | Descripción                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>          | El NPP no está conectado a la red. Llame [**a IStats::Conectar**](istats-connect.md) para conectar el NPP a la red.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>          | El NPP no captura datos. Llame [**a IStats::Start**](istats-start.md) para iniciar la captura.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NO \_ SOLO \_ ESTADÍSTICAS**</dt> </dl>        | El NPP está conectado a la red, pero no con el [**método IStats::Conectar.**](istats-connect.md)<br/>                                                                                                                         |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | La configuración de esta conexión se establece para no guardar las estadísticas de conversación. Para guardar las estadísticas de conversación, detenga la captura, establezca **NoConversationStats = YES** en el BLOB de configuración y reinicie la captura.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo se puede llamar a este método mientras la captura de datos está en curso; cuando la captura actual está en pausa, una llamada a este método no se realizará correctamente.

Para iniciar una captura, llame al [**método IStats::Start.**](istats-start.md) Para recuperar otros tipos de estadísticas, llame a [**IStats::GetTotalStatistics.**](istats-gettotalstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IStats**](istats.md)
</dt> <dt>

[**IStats::GetTotalStatistics**](istats-gettotalstatistics.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Conectar**](istats-connect.md)
</dt> <dt>

[**SESSIONSTATS**](sessionstats.md)
</dt> <dt>

[**STATIONSTATS**](stationstats.md)
</dt> </dl>

 

 




