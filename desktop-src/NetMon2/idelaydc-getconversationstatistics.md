---
description: 'Método IDelaydC::GetConversationStatistics: el método GetConversationStatistics recupera información de sesión y estación sobre la captura actual.'
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: Método IDelaydC::GetConversationStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.GetConversationStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 60fc768a1b93a752a91d431e79fb3e875416ac2b82b2bad5603e3d4cddaccbaf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910575"
---
# <a name="idelaydcgetconversationstatistics-method"></a>Método IDelaydC::GetConversationStatistics

El **método GetConversationStatistics** recupera información [*de*](s.md) sesión [*y estación*](s.md) sobre la captura actual.

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

Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                   | Descripción                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl>          | El NPP no está conectado a la red. Llame [a IDelaydC::Conectar](idelaydc-connect.md) para conectar el NPP a la red.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ NO \_ CAPTURA**</dt> </dl>          | El NPP no captura datos. Llame [a IDelaydC::Start para](idelaydc-start.md) iniciar la captura.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ NO \_ RETRASADO**</dt> </dl>            | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ NO \_ CONVERSATION \_ STATS**</dt> </dl> | La configuración de esta conexión se establece para no guardar las estadísticas de conversación. Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y reinicie la captura.<br/> |



 

## <a name="remarks"></a>Comentarios

Solo se puede llamar a este método mientras la captura de datos está en curso; cuando la captura actual está en pausa, las llamadas a este método no se realizará correctamente. Para iniciar una captura, llame al [método IDelaydC::Start.](idelaydc-start.md)

Para recuperar otros tipos de estadísticas, llame a [IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md).

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

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




