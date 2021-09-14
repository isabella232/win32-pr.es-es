---
description: La estructura NETWORKINFO describe una NIC.
ms.assetid: 40169409-7de5-44d1-8dff-dfa9f647edc9
title: Estructura NETWORKINFO (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245301"
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



## <a name="members"></a>Members

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

Otra dirección que admita esto (por ejemplo, IP, IPX).

</dd> <dt>

**LinkSpeed**
</dt> <dd>

Velocidad del vínculo, en Mbps.

</dd> <dt>

**MacType**
</dt> <dd>

Tipo de medio.

</dd> <dt>

**MaxFrameSize**
</dt> <dd>

Tamaño máximo de fotograma permitido.

</dd> <dt>

**Marcas**
</dt> <dd>

Este parámetro puede ser una de las siguientes marcas de información:



| Value                                                                                                                                                                                                                                       | Significado                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="NETWORKINFO_FLAGS_PMODE_NOT_SUPPORTED"></span><span id="networkinfo_flags_pmode_not_supported"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ PMODE \_ NOT \_ SUPPORTED**</dt> </dl>    | La tarjeta de red no admite el modo promiscuo, lo que significa que solo capturará el tráfico que se difunde por naturaleza o solo implica a la máquina local.<br/> |
| <span id="NETWORKINFO_FLAGS_RAS"></span><span id="networkinfo_flags_ras"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ RAS**</dt> </dl>                                                      | Se trata de una tarjeta de red virtual que es una conexión RAS (servidor de acceso remoto) a través de un módem u otra tarjeta de red.<br/>                                        |
| <span id="NETWORKINFO_FLAGS_REMOTE_CARD"></span><span id="networkinfo_flags_remote_card"></span><dl> <dt>**TARJETA REMOTA DE MARCAS \_ NETWORKINFO \_ \_**</dt> </dl>                             | La tarjeta de red no está en el equipo local, pero está capturando en un equipo remoto en el entorno del equipo local.<br/>                                      |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL"></span><span id="networkinfo_flags_remote_nal"></span><dl> <dt>**NETWORKINFO \_ FLAGS \_ REMOTE \_ NAL**</dt> </dl>                                | Obsoleto; no use.<br/>                                                                                                                                          |
| <span id="NETWORKINFO_FLAGS_REMOTE_NAL_CONNECTED"></span><span id="networkinfo_flags_remote_nal_connected"></span><dl> <dt>**NETWORKINFO \_ MARCA REMOTE \_ \_ NAL \_ CONNECTED**</dt> </dl> | Obsoleto; no use.<br/>                                                                                                                                          |



 

</dd> <dt>

**TimestampScaleFactor**
</dt> <dd>

Por ejemplo, un valor de 1 indica 1/1 ms, 10 indica 1/10 ms, 100 indica 1/100 ms, y así sucesivamente.

</dd> <dt>

**NodeName**
</dt> <dd>

Nombre de la estación de trabajo remota.

</dd> <dt>

**PModeSupported**
</dt> <dd>

Indicador de compatibilidad del modo P de NIC.

</dd> <dt>

**Comment**
</dt> <dd>

Campo de comentario del adaptador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




