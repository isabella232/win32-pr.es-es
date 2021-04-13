---
title: CB_CONNECTION_INFO estructura (Cbclient. h)
description: Contiene información sobre una solicitud de conexión entrante.
ms.assetid: BA908425-3B68-40AA-B1E3-153D6873EF2C
ms.tgt_platform: multiple
keywords:
- Estructura de CB_CONNECTION_INFO Servicios de Escritorio remoto
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
ms.openlocfilehash: 36370a4faa823f509d1f3356768add0ece9a6904
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422090"
---
# <a name="cb_connection_info-structure"></a>Estructura de información de \_ conexión CB \_

Contiene información sobre una solicitud de conexión entrante. Esta estructura se usa con el método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

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

Nombre del dominio del que es miembro el nombre de **usuario** .

</dd> <dt>

**InitialProgram**
</dt> <dd>

La ruta de acceso completa y el nombre de archivo del programa inicial que se inicia cuando se inicia la sesión. Establezca este miembro en una cadena vacía si no se debe iniciar ningún programa inicial.

</dd> <dt>

**Recurso**
</dt> <dd>

Valor de la enumeración del [**\_ \_ tipo de recurso CB**](cb-resource-type.md) que especifica el tipo de recurso al que se está conectando la conexión entrante. Si el miembro **plugInName** es **null**, el agente de conexión a escritorio remoto usa este miembro para determinar el complemento que se debe invocar para determinar el equipo de destino.

</dd> <dt>

**PluginName**
</dt> <dd>

Nombre del complemento que se va a invocar para determinar el equipo de destino. Si este parámetro es **null**, el miembro de **recurso** se utiliza para determinar el complemento que se va a invocar.

</dd> <dt>

**FarmName**
</dt> <dd>

El nombre de la granja que contiene los equipos, uno de los cuales será el equipo de destino al que se redirigirá la conexión.

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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





