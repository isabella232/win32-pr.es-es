---
title: CB_CONNECTION_INFO estructura (Cbclient.h)
description: Contiene información sobre una solicitud de conexión entrante.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- CB_CONNECTION_INFO estructura Servicios de Escritorio remoto
- PCB_CONNECTION_INFO puntero de estructura Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_CONNECTION_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd433f668c178973a4e3690ea130d01d75fab79e739610f77ac00619b9e326c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575045"
---
# <a name="cb_connection_info-structure"></a>Estructura CB \_ CONNECTION \_ INFO

Contiene información sobre una solicitud de conexión entrante. Esta estructura se usa con el [**método IConnectionBrokerClient::GetTargetInfo.**](iconnectionbrokerclient-gettargetinfo.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  WCHAR            UserName[CB_USERNAME_LENGTH];
  WCHAR            Domain[CB_DOMAINNAME_LENGTH];
  WCHAR            InitialProgram[CB_INITAPP_LENGTH];
  CB_RESOURCE_TYPE Resource;
  WCHAR            PluginName[CB_PLUGINNAME_LENGTH];
  WCHAR            FarmName[CB_FARMNAME_LENGTH];
  DWORD            dwVendorInfoLength;
  PBYTE            pVendorSpecificInfo;
} CB_CONNECTION_INFO, *PCB_CONNECTION_INFO;
```



## <a name="members"></a>Miembros

<dl> <dt>

**UserName**
</dt> <dd>

Nombre del usuario que solicita una sesión.

</dd> <dt>

**Dominio**
</dt> <dd>

Nombre del dominio del que es miembro **UserName.**

</dd> <dt>

**InitialProgram**
</dt> <dd>

Ruta de acceso completa y nombre de archivo del programa inicial que se inicia cuando se inicia la sesión. Establezca este miembro en una cadena vacía si no se debe iniciar ningún programa inicial.

</dd> <dt>

**Recurso**
</dt> <dd>

Valor de la [**enumeración CB \_ RESOURCE \_ TYPE**](cb-resource-type.md) que especifica el tipo de recurso al que se conecta la conexión entrante. Si el **miembro PluginName** es **NULL,** el agente de Conexión a Escritorio remoto usa este miembro para determinar qué complemento se va a invocar para determinar el equipo de destino.

</dd> <dt>

**PluginName**
</dt> <dd>

Nombre del complemento que se invocará para determinar el equipo de destino. Si este parámetro es **NULL,** el **miembro Resource** se usa para determinar qué complemento se va a invocar.

</dd> <dt>

**FarmName**
</dt> <dd>

Nombre de la granja de servidores que contiene los equipos, uno de los cuales será el equipo de destino donde se redirigirá la conexión.

</dd> <dt>

**dwVendorInfoLength**
</dt> <dd>

Este miembro se reserva para uso futuro.

</dd> <dt>

**pVendorSpecificInfo**
</dt> <dd>

Este miembro se reserva para uso futuro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Header<br/>                   | <dl> <dt>Cbclient.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





