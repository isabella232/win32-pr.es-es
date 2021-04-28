---
description: 'Método IRTC::GetConversationStatistics: el método GetConversationStatistics recupera información de sesión y estación sobre la captura actual.'
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: Método IRTC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 4d2476f4eb33d7e74d0de8363fa88d5e688a2e73
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110703"
---
# <a name="irtcgetconversationstatistics-method"></a>IrTC::GetConversationStatistics (método)

El **método GetConversationStatistics** recupera información [*de*](s.md) sesión y [*estación*](s.md) sobre la captura actual.

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

Puntero a una [estructura SESSIONSTATS.](sessionstats.md)

</dd> <dt>

*nStations* \[ out\]
</dt> <dd>

Puntero a un DWORD que contiene el número de [*estaciones*](s.md) registradas para la captura actual.

</dd> <dt>

*lpStationStats* \[ out\]
</dt> <dd>

Puntero a una [estructura STATIONSTATS.](stationstats.md)

</dd> <dt>

*fClearAfterReading* \[ En\]
</dt> <dd>

Marca que se usa para Monitor de red borrar el almacenamiento interno de las estructuras [SESSIONSTATS](sessionstats.md) y [STATIONSTATS](stationstats.md) después de recuperar la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                   | Descripción                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>          | El NPP no está conectado a la red. Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>          | El NPP no captura datos. Llame [a IRTC::Start](irtc-start.md) para iniciar la captura.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>           | El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | La configuración de esta conexión se establece para no guardar las estadísticas de conversación. Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y reinicie la captura.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo se puede llamar a este método mientras se capturan datos; Si llama a este método mientras la captura actual está en pausa, el método no se realizará correctamente. Para iniciar una captura, llame al [método IRTC::Start.](irtc-start.md)

Para recuperar otros tipos de estadísticas, llame al [método IRTC::GetTotalStatistics.](irtc-gettotalstatistics.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Connect](irtc-connect.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




