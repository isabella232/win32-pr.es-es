---
title: CB_TARGET_INFO estructura (Cbclient. h)
description: Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Estructura de CB_TARGET_INFO Servicios de Escritorio remoto
- PCB_TARGET_INFO puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422089"
---
# <a name="cb_target_info-structure"></a>Estructura de información del \_ destino CB \_

Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes. Esta estructura se usa con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ServerName**
</dt> <dd>

Representa el nombre de dominio completo del servidor de destino. En un escenario de virtualización de Escritorio remoto (RDV), este miembro es **null**. En un escenario de host de sesión Escritorio remoto (RDSH), este miembro contiene el nombre del servidor al que se redirige la conexión entrante.

</dd> <dt>

**AddressCount**
</dt> <dd>

El número de entradas válidas en la matriz **Addresses** .

</dd> <dt>

**Direcciones**
</dt> <dd>

Matriz de cadenas que contienen las direcciones IP a las que se redirigen las conexiones entrantes. El número de elementos válidos en esta matriz se especifica en el miembro **AddressCount** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





