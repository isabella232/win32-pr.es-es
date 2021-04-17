---
title: Estructura DOSwarmStats (Deliveryoptimization. h)
description: Contiene campos para las estadísticas de descarga y carga de un archivo.
ms.assetid: 66B2498A-38E0-44E4-96C1-F778BD9AA593
keywords:
- Estructura DOSwarmStats
topic_type:
- apiref
api_name:
- DOSwarmStats
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53d1702c25716ffe90c35727a258134311d5f427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714646"
---
# <a name="doswarmstats-structure"></a>Estructura DOSwarmStats

Contiene campos para las estadísticas de descarga y carga de un archivo.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _DOSwarmStats {
  LPWSTR       fileId;
  LPWSTR       sourceURL;
  UINT64       fileSize;
  UINT64       totalBytesDownloaded;
  UINT64       bytesFromLanPeers;
  UINT64       bytesFromGroupPeers;
  UINT64       bytesFromInternetPeers;
  UINT64       bytesFromHttp;
  UINT64       bytesFromDoinc;
  UINT64       bytesToLanPeers;
  UINT64       bytesToGroupPeers;
  UINT64       bytesToInternetPeers;
  UINT         httpConnectionCount;
  UINT         doincConnectionCount;
  UINT         lanConnectionCount;
  UINT         groupConnectionCount;
  UINT         internetConnectionCount;
  UINT         downloadDuration;
  DownloadMode downloadMode;
  SwarmStatus  status;
  BOOL         isBackground;
} DOSwarmStats;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ID**
</dt> <dd>

Cadena terminada en null que se especificó con la llamada a **AddFileWithRanges** .

</dd> <dt>

**sourceURL**
</dt> <dd>

Cadena terminada en null que contiene el nombre del archivo en el servidor (por ejemplo, https:// &lt; ruta de acceso del servidor &gt; / &lt; &gt; /file.ext).

</dd> <dt>

**fileSize**
</dt> <dd>

Tamaño del archivo en bytes.

</dd> <dt>

**totalBytesDownloaded**
</dt> <dd>

Número total de bytes transferidos.

</dd> <dt>

**bytesFromLanPeers**
</dt> <dd>

Número de bytes transferidos desde los pares de LAN.

</dd> <dt>

**bytesFromGroupPeers**
</dt> <dd>

Número de bytes transferidos desde grupos del mismo nivel.

</dd> <dt>

**bytesFromInternetPeers**
</dt> <dd>

Número de bytes transferidos desde los pares de Internet.

</dd> <dt>

**bytesFromHttp**
</dt> <dd>

Número de bytes transferidos desde http.

</dd> <dt>

**bytesFromDoinc**
</dt> <dd>

Solo para uso interno.

</dd> <dt>

**bytesToLanPeers**
</dt> <dd>

Número de bytes transferidos a los pares de LAN.

</dd> <dt>

**bytesToGroupPeers**
</dt> <dd>

Número de bytes transferidos al grupo del mismo nivel.

</dd> <dt>

**bytesToInternetPeers**
</dt> <dd>

Número de bytes transferidos a los pares de Internet.

</dd> <dt>

**httpConnectionCount**
</dt> <dd>

Recuento de conexiones http.

</dd> <dt>

**doincConnectionCount**
</dt> <dd>

Solo para uso interno.

</dd> <dt>

**lanConnectionCount**
</dt> <dd>

Recuento de conexiones LAN.

</dd> <dt>

**groupConnectionCount**
</dt> <dd>

Recuento de conexiones de grupo.

</dd> <dt>

**internetConnectionCount**
</dt> <dd>

Recuento de conexiones a Internet.

</dd> <dt>

**downloadDuration**
</dt> <dd>

Duración de la transferencia de archivo en milisegundos.

</dd> <dt>

**downloadMode**
</dt> <dd>

El modo de descarga usado, vea [**DownloadMode**](downloadmode.md).

</dd> <dt>

**status**
</dt> <dd>

El estado de una transferencia de archivos, vea [**SwarmStatus**](swarmstatus.md).

</dd> <dt>

**isBackground**
</dt> <dd>

True, si se trata de una transferencia en segundo plano.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





