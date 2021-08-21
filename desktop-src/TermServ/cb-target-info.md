---
title: CB_TARGET_INFO estructura (Cbclient.h)
description: Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO estructura Servicios de Escritorio remoto
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
ms.openlocfilehash: 1e7c00e1997ee36b42b21b833942597d9b43f393b2bcdfcee1aa0ee18e3a4548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001613"
---
# <a name="cb_target_info-structure"></a>Estructura CB \_ TARGET \_ INFO

Contiene información sobre el equipo de destino y las direcciones IP donde se deben redirigir las conexiones entrantes. Esta estructura se usa con [**el método IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

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

Representa el nombre de dominio completo del servidor de destino. Para un escenario Escritorio remoto virtualización de datos (RDV), este miembro es **NULL.** Para un Escritorio remoto host de sesión de sesión (RDSH), este miembro contiene el nombre del servidor donde se redirige la conexión entrante.

</dd> <dt>

**AddressCount**
</dt> <dd>

Número de entradas válidas en la matriz **Addresses.**

</dd> <dt>

**Direcciones**
</dt> <dd>

Matriz de cadenas que contienen las direcciones IP a las que se redirigen las conexiones entrantes. El número de elementos válidos de esta matriz se especifica en el **miembro AddressCount.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





