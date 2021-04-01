---
title: Método SetBrokerHAMode de la clase Win32_SessionBrokerServiceProperties
description: Migra datos de una base de datos WID local a la nueva base de datos basada en SQL Server. También configura el servidor de agente para usar SQL Server central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Método SetBrokerHAMode Servicios de Escritorio remoto
- Método SetBrokerHAMode Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método SetBrokerHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4526f8ded96086ccf223b3c8e5aad72d9e0262cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150283"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetBrokerHAMode de la \_ clase SessionBrokerServiceProperties de Win32

Migra datos de una base de datos WID local a la nueva base de datos basada en SQL Server. También configura el servidor de agente para usar SQL Server central.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetBrokerHAMode(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms,
  [in] string brokerDnsRRName,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToCentralDBRdcms* \[ de\]
</dt> <dd>

Cadena de conexión a la base de datos central.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ de\]
</dt> <dd>

Cadena de conexión secundaria a la base de datos central.

**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ de\]
</dt> <dd>

Nombre DNS del agente.

</dd> <dt>

*activeBrokerName* \[ de\]
</dt> <dd>

Nombre del agente activo.

**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionBrokerServiceProperties**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





