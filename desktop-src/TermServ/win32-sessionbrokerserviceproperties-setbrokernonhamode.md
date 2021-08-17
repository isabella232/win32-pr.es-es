---
title: Método SetBrokerNonHAMode de la Win32_SessionBrokerServiceProperties clase
description: Migra datos del centro de SQL Server a una base de datos local. También configura el servidor de agente para que use la base de datos local.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- Método SetBrokerNonHAMode Servicios de Escritorio remoto
- Método SetBrokerNonHAMode Servicios de Escritorio remoto , Win32_SessionBrokerServiceProperties clase
- Win32_SessionBrokerServiceProperties clase Servicios de Escritorio remoto , método SetBrokerNonHAMode
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34daa0817056975a6b15164dd29edcbcc86cd7cd9475f753e91500845ce089a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058420"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método SetBrokerNonHAMode de la clase \_ SessionBrokerServiceProperties de Win32

Migra datos del centro de SQL Server a una base de datos local. También configura el servidor de agente para que use la base de datos local.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToCentralDBRdcms* \[ En\]
</dt> <dd>

Cadena de conexión a la base de datos central.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SessionBrokerServiceProperties de Win32 \_**](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





