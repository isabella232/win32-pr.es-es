---
title: Método SetBrokerHAMode de la Win32_SessionBrokerServiceProperties clase
description: Migra datos de una base de datos WID local a la nueva base SQL base de datos basada en servidor. También configura el servidor de agente para que use el servidor SQL central.
ms.assetid: 8f14590d-3042-403c-a1cb-a3b257866284
ms.tgt_platform: multiple
keywords:
- Método SetBrokerHAMode Servicios de Escritorio remoto
- Método SetBrokerHAMode Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , método SetBrokerHAMode
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
ms.openlocfilehash: 17b72233b51686911e4b1d0a661f4e46fa9bcaa813bb6ccc973b2f8a5b12da24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604554"
---
# <a name="setbrokerhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetBrokerHAMode de la clase SessionBrokerServiceProperties de Win32 \_

Migra datos de una base de datos WID local a la nueva base SQL base de datos basada en servidor. También configura el servidor de agente para que use el servidor SQL central.

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

*connStringToCentralDBRdcms* \[ En\]
</dt> <dd>

Cadena de conexión a la base de datos central.

</dd> <dt>

*secondaryConnStringToCentralDBRdcms* \[ En\]
</dt> <dd>

Cadena de conexión secundaria a la base de datos central.

**Windows Server 2012 R2 y Windows Server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> <dt>

*brokerDnsRRName* \[ En\]
</dt> <dd>

Nombre DNS del agente.

</dd> <dt>

*activeBrokerName* \[ En\]
</dt> <dd>

Nombre del agente activo.

**Windows Server 2012 R2 y Windows Server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionBrokerServiceProperties de Win32 \_**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





