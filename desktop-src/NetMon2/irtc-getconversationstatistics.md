---
description: El método GetConversationStatistics recupera información de la sesión y de la estación sobre la captura actual.
ms.assetid: 27f364cd-fee9-4262-b181-c5f15fb12e51
title: 'IRTC:: GetConversationStatistics (método) (Netmon. h)'
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
ms.openlocfilehash: 758488cb3c3f65922bbf6aac4f39774a5430fc92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908701"
---
# <a name="irtcgetconversationstatistics-method"></a>IRTC:: GetConversationStatistics (método)

El método **GetConversationStatistics** recupera información de la [*sesión*](s.md) y de la [*estación*](s.md) sobre la captura actual.

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

*nSessions* \[ enuncia\]
</dt> <dd>

Puntero a un valor DWORD que contiene el número de [*sesiones*](s.md) registradas para la captura actual.

</dd> <dt>

*lpSessionStats* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [SESSIONSTATS](sessionstats.md) .

</dd> <dt>

*nStations* \[ enuncia\]
</dt> <dd>

Puntero a un valor DWORD que contiene el número de [*estaciones*](s.md) registradas para la captura actual.

</dd> <dt>

*lpStationStats* \[ enuncia\]
</dt> <dd>

Puntero a una estructura [STATIONSTATS](stationstats.md) .

</dd> <dt>

*fClearAfterReading* \[ de\]
</dt> <dd>

Marca usada para indicar a Monitor de red que borre el almacenamiento interno de las estructuras [SESSIONSTATS](sessionstats.md) y [STATIONSTATS](stationstats.md) después de recuperar la información actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                                   | Descripción                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>          | NPP no está conectado a la red. Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.<br/>                                                                                                      |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>          | NPP no está capturando datos. Llame a [IRTC:: Start](irtc-start.md) para iniciar la captura.<br/>                                                                                                                                 |
| <dl> <dt>**NMERR \_ no es en \_ tiempo real**</dt> </dl>           | NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .<br/>                                                                                                                          |
| <dl> <dt>**NMERR \_ no \_ hay \_ estadísticas de conversación**</dt> </dl> | La configuración de esta conexión está establecida en no guardar estadísticas de conversación. Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y reinicie la captura.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo se puede llamar a este método mientras se capturan datos; Si llama a este método mientras la captura actual está en pausa, el método no se realizará correctamente. Para iniciar una captura, llame al método [IRTC:: Start](irtc-start.md) .

Para recuperar otros tipos de estadísticas, llame al método [IRTC:: GetTotalStatistics](irtc-gettotalstatistics.md) .

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

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IRTC:: Start](irtc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




