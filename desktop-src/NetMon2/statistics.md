---
description: La estructura STATISTICs proporciona estadísticas para la captura. Algunas de estas estadísticas las genera Monitor de red, mientras que otras las genera la NIC a la que está conectado el NPP.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: STATISTICs (estructura) (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- STATISTICS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a3798f32f7341722432441272eded7d7605cf8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677632"
---
# <a name="statistics-structure"></a>STATISTICs (estructura)

La estructura **Statistics** proporciona estadísticas para la captura. Algunas de estas estadísticas las genera Monitor de red, mientras que otras las genera la NIC a la que está conectado el NPP.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _STATISTICS {
  __int64 TimeElapsed;
  DWORD   TotalFramesCaptured;
  DWORD   TotalBytesCaptured;
  DWORD   TotalFramesFiltered;
  DWORD   TotalBytesFiltered;
  DWORD   TotalMulticastsFiltered;
  DWORD   TotalBroadcastsFiltered;
  DWORD   TotalFramesSeen;
  DWORD   TotalBytesSeen;
  DWORD   TotalMulticastsReceived;
  DWORD   TotalBroadcastsReceived;
  DWORD   TotalFramesDropped;
  DWORD   TotalFramesDroppedFromBuffer;
  DWORD   MacFramesReceived;
  DWORD   MacCRCErrors;
  __int64 MacBytesReceivedEx;
  DWORD   MacFramesDropped_NoBuffers;
  DWORD   MacMulticastsReceived;
  DWORD   MacBroadcastsReceived;
  DWORD   MacFramesDropped_HwError;
} STATISTICS, *LPSTATISTICS;
```



## <a name="members"></a>Miembros

<dl> <dt>

**TimeElapsed**
</dt> <dd>

Tiempo transcurrido, en microsegundos.

</dd> <dt>

**TotalFramesCaptured**
</dt> <dd>

Número total de Marcos almacenados actualmente. Este número está limitado por el tamaño del archivo o búfer de captura que se usa para almacenar los fotogramas.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Número total de bytes almacenados actualmente. Este número está limitado por el tamaño del archivo o búfer de captura que se usa para almacenar los fotogramas.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Número total de fotogramas que pasan a través del filtro de captura actual. Si no se usa un filtro, este valor es el mismo que el de **TotalFramesSeen**.

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Número total de fotogramas que pasan a través del filtro de captura actual. Si no se usa un filtro, este valor es el mismo que el de **TotalBytesSeen**.

</dd> <dt>

**TotalMulticastsFiltered**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**TotalBroadcastsFiltered**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**TotalFramesSeen**
</dt> <dd>

Número total de fotogramas administrados por la NIC.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Número total de bytes administrados por la NIC.

</dd> <dt>

**TotalMulticastsReceived**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**TotalBroadcastsReceived**
</dt> <dd>

Este miembro está obsoleto.

</dd> <dt>

**TotalFramesDropped**
</dt> <dd>

Número total de fotogramas quitados (fotogramas que pasaron el filtro pero no se guardaron).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Número de fotogramas quitados del búfer o archivo de captura. Cuando el búfer está lleno, se quitan los fotogramas más antiguos para dejar espacio a los nuevos.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Número de fotogramas que los informes de NIC han recibido.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Número de errores de CRC informados por la NIC.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Número de bytes que los informes de NIC han recibido.

</dd> <dt>

**MacFramesDropped \_ Nobuffers**
</dt> <dd>

Número de fotogramas que la NIC informa de que se han quitado debido a la falta de espacio en el búfer.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Número de multidifusiones que han recibido los informes de NIC.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Número de difusiones que los informes de NIC han recibido.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Número de fotogramas que la NIC informa de que se han quitado debido a errores de hardware.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta estructura se usa para recuperar [*Estadísticas totales*](t.md)y para pausar o detener la captura actual.

No se pueden recuperar las estadísticas totales cuando se usa la interfaz [iesp](iesp.md) NPP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStas:: GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStas::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> <dt>

[IESP:: Stop](iesp-stop.md)
</dt> <dt>

[IRTC:: Stop](irtc-stop.md)
</dt> <dt>

[IStatsC:: Stop](istats-stop.md)
</dt> </dl>

 

 




