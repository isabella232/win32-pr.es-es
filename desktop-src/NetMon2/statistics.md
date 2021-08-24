---
description: La estructura STATISTICS proporciona estadísticas para la captura. Algunas de estas estadísticas se generan mediante Monitor de red, mientras que otras las genera la NIC a la que está conectado el NPP.
ms.assetid: 5e30ae30-d8ad-4336-9e4d-fa10ceefc966
title: Estructura STATISTICS (Netmon.h)
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
ms.openlocfilehash: 273e6ba9e32337cc65b3dce979d2ff407b904595237b60025e42fc58e57d9823
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778285"
---
# <a name="statistics-structure"></a>ESTRUCTURA STATISTICS

La **estructura STATISTICS** proporciona estadísticas para la captura. Algunas de estas estadísticas se generan mediante Monitor de red, mientras que otras las genera la NIC a la que está conectado el NPP.

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

Número total de fotogramas almacenados actualmente. Este número está limitado por el tamaño del archivo de captura o búfer usado para almacenar los fotogramas.

</dd> <dt>

**TotalBytesCaptured**
</dt> <dd>

Número total de bytes almacenados actualmente. Este número está limitado por el tamaño del archivo de captura o búfer usado para almacenar los fotogramas.

</dd> <dt>

**TotalFramesFiltered**
</dt> <dd>

Número total de fotogramas que pasaron por el filtro de captura actual. Si no se usa un filtro, este valor es el mismo que **TotalFramesSeen.**

</dd> <dt>

**TotalBytesFiltered**
</dt> <dd>

Número total de fotogramas que pasaron por el filtro de captura actual. Si no se usa un filtro, este valor es el mismo que **TotalBytesSeen**.

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

Número total de fotogramas que controla la NIC.

</dd> <dt>

**TotalBytesSeen**
</dt> <dd>

Número total de bytes que controla la NIC.

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

Número total de fotogramas descartados (fotogramas que pasaron el filtro pero no se guardaron).

</dd> <dt>

**TotalFramesDroppedFromBuffer**
</dt> <dd>

Número de fotogramas eliminados del archivo o búfer de captura. Cuando el búfer está lleno, se quitan los fotogramas más antiguos para hacer espacio para los nuevos.

</dd> <dt>

**MacFramesReceived**
</dt> <dd>

Número de fotogramas que la NIC notifica haber recibido.

</dd> <dt>

**MacCRCErrors**
</dt> <dd>

Número de errores de CRC notificados por la NIC.

</dd> <dt>

**MacBytesReceivedEx**
</dt> <dd>

Número de bytes que la NIC notifica que ha recibido.

</dd> <dt>

**MacFramesDropped \_ NoBuffers**
</dt> <dd>

Número de fotogramas que la NIC notifica que se han eliminado debido a la falta de espacio en búfer.

</dd> <dt>

**MacMulticastsReceived**
</dt> <dd>

Número de multidifusión que notifica la NIC que ha recibido.

</dd> <dt>

**MacBroadcastsReceived**
</dt> <dd>

Número de difusión que han recibido los informes nic.

</dd> <dt>

**MacFramesDropped \_ HwError**
</dt> <dd>

Número de fotogramas que la NIC indica que se han eliminado debido a errores de hardware.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta estructura se usa para recuperar el [*total de estadísticas*](t.md)y para pausar o detener la captura actual.

No se pueden recuperar las estadísticas totales cuando se usa la interfaz de NPP de [IESP.](iesp.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IDelaydC::GetTotalStatistics](idelaydc-gettotalstatistics.md)
</dt> <dt>

[IRTC::GetTotalStatistics](irtc-gettotalstatistics.md)
</dt> <dt>

[IStats::GetTotalStatistics](istats-gettotalstatistics.md)
</dt> <dt>

[IDelaydC::P ause](idelaydc-pause.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IStats::P ause](istats-pause.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> <dt>

[IESP::Stop](iesp-stop.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> <dt>

[IStatsC::Stop](istats-stop.md)
</dt> </dl>

 

 




