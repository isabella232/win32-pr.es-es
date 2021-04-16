---
title: Método IsDbReachable de la clase Win32_SessionBrokerServiceProperties
description: Comprueba si la base de datos es accesible.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- Método IsDbReachable Servicios de Escritorio remoto
- Método IsDbReachable Servicios de Escritorio remoto, clase Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties de clase Servicios de Escritorio remoto, método IsDbReachable
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490582"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a>Método IsDbReachable de la \_ clase SessionBrokerServiceProperties de Win32

Comprueba si la base de datos es accesible.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*connStringToDb* \[ de\]
</dt> <dd>

La cadena de conexión a la base de datos.

</dd> <dt>

*connSecondaryStringToDb* \[ de\]
</dt> <dd>

Cadena de conexión secundaria a la base de datos central.

**Windows server 2012 R2 y Windows server 2012:** Este parámetro no está disponible antes de Windows Server 2016.

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

 

 





