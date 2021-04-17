---
description: El método GetConversationStatistics recupera información de la sesión y de la estación sobre la captura actual.
ms.assetid: 0164fa0e-90f2-4b97-be9d-55d172f8112d
title: 'IDelaydC:: GetConversationStatistics (método) (Netmon. h)'
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
ms.openlocfilehash: aaba5ccfbab48639f53395519f001f5f8e85e483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686567"
---
# <a name="idelaydcgetconversationstatistics-method"></a>IDelaydC:: GetConversationStatistics (método)

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



| Código devuelto                                                                                                   | Descripción                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ no \_ conectado**</dt> </dl>          | NPP no está conectado a la red. Llame a [IDelaydC:: Connect](idelaydc-connect.md) para conectar el NPP a la red.<br/>                                                                                                  |
| <dl> <dt>**NMERR \_ no se \_ captura**</dt> </dl>          | NPP no está capturando datos. Llame a [IDelaydC:: Start](idelaydc-start.md) para iniciar la captura.<br/>                                                                                                                             |
| <dl> <dt>**NMERR \_ no \_ retrasado**</dt> </dl>            | NPP está conectado a la red, pero no con el método [IDelaydC:: Connect](idelaydc-connect.md) .<br/>                                                                                                                      |
| <dl> <dt>**NMERR \_ no \_ hay \_ estadísticas de conversación**</dt> </dl> | La configuración de esta conexión está establecida en no guardar estadísticas de conversación. Para guardar las estadísticas de conversación, detenga la captura, establezca NoConversationStats = YES en el BLOB de configuración y, a continuación, reinicie la captura.<br/> |



 

## <a name="remarks"></a>Observaciones

Solo se puede llamar a este método cuando la captura de datos está en curso; Cuando la captura actual se pausa, las llamadas a este método no se realizarán correctamente. Para iniciar una captura, llame al método [IDelaydC:: Start](idelaydc-start.md) .

Para recuperar otros tipos de estadísticas, llame a [IDelaydC:: GetTotalStatistics](idelaydc-gettotalstatistics.md).

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

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IDelaydC:: Start](idelaydc-start.md)
</dt> <dt>

[SESSIONSTATS](sessionstats.md)
</dt> <dt>

[STATIONSTATS](stationstats.md)
</dt> </dl>

 

 




