---
description: La estructura NETWORKINFO describe una NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Estructura NETWORKINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8917966d2e090417a95a9ca20158c6c5935bda3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818531"
---
# <a name="networkinfo-structure"></a>Estructura NETWORKINFO

La estructura NETWORKINFO describe una NIC.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _NETWORKINFO {
  BYTE    PermanentAddr[6];
  BYTE    CurrentAddr[6];
  ADDRESS OtherAddress;
  DWORD   LinkSpeed;
  DWORD   MacType;
  DWORD   MaxFrameSize;
  DWORD   Flags;
  DWORD   TimestampScaleFactor;
  BYTE    NodeName[32];
  BOOL    PModeSupported;
  BYTE    Comment[ADAPTER_COMMENT_LENGTH];
} NETWORKINFO, *LPNETWORKINFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**PermanentAddr**
</dt> <dd>

Dirección MAC permanente.

</dd> <dt>

**CurrentAddr**
</dt> <dd>

Dirección MAC actual.

</dd> <dt>

**OtherAddress**
</dt> <dd>

Otra dirección que admite este (por ejemplo, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Velocidad de vínculo, en Mbps.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de medio.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Tamaño máximo de trama permitido.

</dd> <dt>

**Marcas**
</dt> <dd>

Este parámetro puede ser una de las siguientes marcas informativas:



| Value                                                                                                                                                                                                                                       | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**\_no se \_ \_ \_ admiten marcas NETWORKINFO PMODE**</dt> </dl>    | La tarjeta de red no es compatible con el modo promiscuo, lo que significa que solo capturará el tráfico que se difunde por naturaleza o solo implica el equipo local.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**NETWORKINFO \_ marca \_ ras**</dt> </dl>                                                      | Se trata de una tarjeta de red virtual que es una conexión RAS (servidor de acceso remoto) a través de un módem u otra tarjeta de red.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**\_ \_ tarjeta remota de marcas de NETWORKINFO \_**</dt> </dl>                             | La tarjeta de red no está en el equipo local, pero está realizando la captura en un equipo remoto en el Bequest del equipo local.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ marca \_ el \_ nal remoto**</dt> </dl>                                | Obsoleto No use.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ marcas de acceso \_ remoto de \_ nal \_ conectadas**</dt> </dl> | Obsoleto No use.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Por ejemplo, un valor de 1 indica 1/1 MS, 10 indica 1/10 ms, 100 indica 1/100 MS, etc.

</dd> <dt>

**NodeName**
</dt> <dd>

Nombre de la estación de trabajo remota.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicador de compatibilidad de modo P de NIC.

</dd> <dt>

**Comentario**
</dt> <dd>

Campo de comentario del adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




